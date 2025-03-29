# StarCCM-Aneurysm-Automation
These macro are designed to hep automate your STAR-CCM post-processes. This repository contains macros which sets the required prerequisites for the simulation. Once pre-processing of mesh file completed, run the supplied python file to complete pre-processing and post-processing by generating a presentation with all scenes and plots labelled. Deeply useful for aneurysms, medical imaging, and other projects which require documentation of multiple simulations. 

NOTE: You should be able to customize this project using the .java file.

Files included:

a1continua.java: This is the inital macro to be used in STAR-CCM. This creates the cotinua with the properties of blood

a2inletvel.java: Second macro to be used, sets the varying velocity profile by attaching the required .csv file

--NOTE: Ensure file directory same (saved in P-drive)

a3velocityprobe.java: Sets a velocity probe at inlet and plots a velocity-time graph

a4monitors.java: Creates monitors of of mean WSS and sum of WSS (i/j/k components)

a5fieldfunctions.java: Creates custom field functions of OSI, TA-WSS, and RRT

a6mesheroperations.java: Creates mesh operation of approx. 1,000,000 cells

a7stoppingcrit.java: Creates stopping criteria of 2 cardiac cycles (1.9 seconds)

a8views.java: Saves isometric views (front and back)

a9outlet.java: Sets Outlet Split Factor as 0.5

a10scenes.java: Creates scalar scenes of WSS, TA-WSS, OSI, RRT, Streamlines

unsteadyinlet.csv: CSV file of velocity-time used by a2inletvel.java macro

--NOTE: Values in .csv file are that of a normal cardiac cycle and from 



STEPS TO RUN:

Go to your active simulation file in STAR-CCM. Hit File --> Macro --> Play Macro --> Select macros in order of number
Wait for the macro to finish. It will generate the required output
Once macro is completed, run the next macro depending on preference.
Macros are currently split into 10 sections, to give the user independence on creating 


PATCH NOTES:

V 1.0 -->
Created base program
Generates plots and scenes

V 1.1 (work in progress)-->
Fixed Velocity probe error if mesh file imported at different angle.
All images are now auto labelled with image names.
Created mega compiled macro, that runs all sub macros




