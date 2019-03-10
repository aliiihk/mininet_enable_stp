# Enable STP on Mininet OpenFlow Switches
Mininet is a Linux-based program which allows you to run virtualized hosts which support the OpenFlow protocol for Software-Defined Networking (SDN).

While experimenting different types of virtualized networks, I noticed that if you create a network with redundant paths, connectivity between hosts would fail as Spanning-tree would be disabled.

To address this issue, a script was wriitten which examines a .py file exported from MiniEdit and enable Spanning-tree on all the switches. The steps are below:

- Run Miniedit and setup the network topology to your preference
- Right click on the controller, click on properties and change the controller type to Remote Controller
- Export and save as Level 2 script in the same directory as where the "enableSTP.py" script is being stored (downloaded from this project)
- Run the enableSTP.py script and when prompted, enter the name of the script exported from Miniedit (the .py file)
- After the script is done running, it will tell you the name of the new pyton script to run, run this as you would normally (controller will start automatically as well)

Some Points to be Noted
- It is assumed Mininet is already downloaded. For more information on the installtion of Mininet and MiniEdit, please visit http://mininet.org/download/ and http://www.brianlinkletter.com/how-to-use-miniedit-mininets-graphical-user-interface/
- There are multiple different methods to ensure connectivity between hosts such as using a different controller, this is just one method
