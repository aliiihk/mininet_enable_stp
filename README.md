# Enable STP Automatically on Mininet Switches (compatible with MiniEdit)
While experimenting different types of virtualized networks in Mininet, I noticed that if you create a network with redundant paths, connectivity between hosts would fail although Spanning-tree is on by default. 
As a result, I wrote a script to go through a .py file exported from MiniEdit and enable Spanning-tree on all the switches
- Run Miniedit as per usual and setup the network as per usual
- Right click on the controller, click on properties and change the controller type to Remote Controller
- Export and save as L2 script in the same directory as where the "enableSTP.py" script is being stored
- Run the enableSTP.py script and when prompted, enter the name of the script exported from Miniedit (the .py file)
- After the script is done running, it will tell you the name of the new pyton script to run, run this as you would normally (controller will start automatically as well)

