# Paved Road Finder
The "Paved Road Finder" is a Python-based application designed to efficiently locate the shortest path to the nearest paved road from a given parcel ID. It addresses the critical need for accurate road surface information, crucial for various scenarios such as emergency response planning and outdoor recreation. Leveraging road network data from sources like OpenStreetMap (OSM) and Overpass Turbo, the application collects details on road geometry and attributes, including whether roads are paved or unpaved. 
Through a user-friendly interface, users input the Parcel ID, and the application dynamically calculates the optimal route to the nearest paved road based on the collected data. The identified path is then visualized on an interactive map interface, providing users with a clear understanding of the route. 
![image](https://github.com/prog-proj-novaims/Shortest-Path-to-the-Closest-Paved-Road-in-Rural-Area-/assets/158604785/f8ada662-0fec-48ff-9383-c440fdf7e922)
# Requirements
Set up python environment using:  
**conda create -n routing_project**  
**conda activate routing_project**  
Install packages outlined in #requirements.txt using   
**conda install --file requirements.txt -c conda-forge**
# Data Sources
This project relies on two main data sources: OSM geometry and OSM attributes. The OSM geometry data, available for download from the provided URL, contains detailed information about road networks, including road segments, intersections, and geographic coordinates. Complementing this, OSM attributes, obtained through the Overpass API, offer additional insights into road classifications, surface conditions, and other relevant attributes. By combining these datasets, the project ensures comprehensive coverage of road network data necessary for effective route planning.  
**OSM Geometry:**  
    http://download.geofabrik.de/  

**OSM attributes:**   
   https://overpass.kumi.systems/api/interpreter
