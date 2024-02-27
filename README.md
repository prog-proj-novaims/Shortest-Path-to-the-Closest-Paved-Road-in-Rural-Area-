# Paved Road Finder
The "Paved Road Finder" is a Python-based application designed to efficiently locate the shortest path to the nearest paved road from a given parcel ID. It addresses the critical need for accurate road surface information, crucial for various scenarios such as emergency response planning and outdoor recreation. Leveraging road network data from sources like OpenStreetMap (OSM) and Overpass Turbo, the application collects details on road geometry and attributes, including whether roads are paved or unpaved. 
Through a user-friendly interface, users input the Parcel ID, and the application dynamically calculates the optimal route to the nearest paved road based on the collected data. The identified path is then visualized on an interactive map interface, providing users with a clear understanding of the route. 
![image](https://github.com/prog-proj-novaims/Shortest-Path-to-the-Closest-Paved-Road-in-Rural-Area-/assets/158604785/f8ada662-0fec-48ff-9383-c440fdf7e922)
# Requirements
Set up python environment using:
conda create -n routing_project
conda activate routing_project
Install packages outlined in #requirements.txt using 
conda install --file requirements.txt -c conda-forge
