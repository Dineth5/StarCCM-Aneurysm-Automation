# StarCCM-Aneurysm-Automation

These macros are designed to help automate your **STAR-CCM+** post-processing workflows. This repository is especially useful for projects involving aneurysms, medical imaging, and other simulations that require consistent documentation across multiple runs.

Once the pre-processing of the mesh file is complete, the included Python file can be run to finalize both pre- and post-processing. This includes auto-generating a presentation with all scenes and plots labeled and ready for reporting.

---

> 📌 **Note:**  
> You can customize most of the behavior and parameters using the `.java` macro files included in this repository.

---

## 📂 Files Included

1. **`a1continua.java`**  
   - Sets up the continua with blood properties.

2. **`a2inletvel.java`**  
   - Applies a varying velocity profile using the `unsteadyinlet.csv` file.  
   - ⚠ Ensure the file directory remains the same (e.g., P-drive).

3. **`a3velocityprobe.java`**  
   - Places a velocity probe at the inlet.  
   - Generates a velocity-time graph.

4. **`a4monitors.java`**  
   - Creates monitors for:  
     - Mean Wall Shear Stress (WSS)  
     - Sum of WSS (i, j, k components)

5. **`a5fieldfunctions.java`**  
   - Defines custom field functions:  
     - OSI (Oscillatory Shear Index)  
     - TA-WSS (Time-Averaged WSS)  
     - RRT (Relative Residence Time)

6. **`a6mesheroperations.java`**  
   - Sets up mesh operations targeting ~1 million cells.

7. **`a7stoppingcrit.java`**  
   - Sets stopping criteria for 2 cardiac cycles (approx. 1.9 seconds).

8. **`a8views.java`**  
   - Saves isometric screenshots (front and back views).

9. **`a9outlet.java`**  
   - Sets outlet split factor to 0.5.

10. **`a10scenes.java`**  
    - Creates scalar scenes for:  
      - WSS  
      - TA-WSS  
      - OSI  
      - RRT  
      - Streamlines

11. **`unsteadyinlet.csv`**  
    - Contains velocity-time data for a normal cardiac cycle.  
    - Used by `a2inletvel.java`.

---

## ▶️ How to Run

1. Open your active simulation in **STAR-CCM+**.
2. Navigate to:  
   `File → Macro → Play Macro`
3. Run each macro **in numerical order**:  
   Start with `a1continua.java`, then `a2inletvel.java`, and so on.
4. Allow each macro to finish before proceeding to the next.
5. Macros are modular — feel free to skip or customize as needed depending on your workflow.

---

## 🛠 Patch Notes

### 📌 Version 1.0
- Initial release.
- Added base macros for setup, monitoring, field functions, and visualization.
- Generates labeled plots and scenes.

### 📌 Version 1.1 *(Work in Progress)*
- Fixed velocity probe error (angle-based mesh import issue).
- All scene images now auto-labeled.
- Added a "mega" macro to run all sub-macros in sequence.

---

## 📬 Contact

For queries:

**Dineth Ilapperuma**  
- [LinkedIn](https://www.linkedin.com/in/ilapperuma/)  
- 📧 dineth.ilapperuma@gmail.com

---

✨ Happy simulating!

