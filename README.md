# Paved Road Finder
The **Paved Road Finder** is a Python-based application meticulously designed to efficiently locate the shortest path to the nearest paved road from a given parcel ID. Its purpose is to address the critical need for accurate road surface information, which plays a pivotal role in various scenarios such as emergency response planning and outdoor recreation.

Here are the key features of the **Paved Road Finder**:

1. **Data Collection and Processing**:
    - The application leverages road network data from reliable sources such as **OpenStreetMap (OSM)** and **Overpass Turbo**.
    - It collects essential details about road geometry and attributes, including whether roads are paved or unpaved.

2. **User-Friendly Interface**:
    - Users input the Parcel ID into the application.
    - The application dynamically calculates the optimal route to the nearest paved road based on the collected data.

3. **Route Visualization**:
    - The identified path is visualized on an interactive map interface.
    - This visualization provides users with a clear understanding of the route, making it easier to plan and navigate.

![Paved Road Finder](https://github.com/prog-proj-novaims/Shortest-Path-to-the-Closest-Paved-Road-in-Rural-Area-/assets/158604785/f8ada662-0fec-48ff-9383-c440fdf7e922)

## Requirements
To set up the Python environment for this project:
1. Create a new environment: `conda create -n routing_project`
2. Activate the environment: `conda activate routing_project`
3. Install the required packages listed in `requirements.txt`: `conda install --file requirements.txt -c conda-forge`

## Data Sources
The **Paved Road Finder** relies on two primary data sources:

1. **OSM Geometry Data**:
    - Available for download from [Geofabrik](http://download.geofabrik.de/).
    - Contains detailed information about road networks, including road segments, intersections, and geographic coordinates.

2. **OSM Attributes**:
    - Obtained through the [Overpass API](https://overpass.kumi.systems/api/interpreter).
    - Provides additional insights into road classifications, surface conditions, and other relevant attributes.

By combining these datasets, the project ensures comprehensive coverage of road network data necessary for effective route planning.
# ETL Process
The Extract, Transform, Load (ETL) process plays a crucial role in preparing and processing OSM data for route calculations. Initially, the data is downloaded in PBF format and filtered using 'osmconvert' to extract relevant road network information. Subsequently, the **'osm2pgrouting'** tool is employed to import the processed data into the PostgreSQL database, optimizing it for routing operations. Additionally, an ETL process extracts surface information for road segments within predefined grid cells, enhancing the accuracy of route planning by considering road surface data.
# Database Utilization:
A PostgreSQL database serves as the central repository for storing and managing the extracted OSM data. With a carefully designed schema, the database efficiently organizes road network information, farm locations, and route results. This relational database management system allowing to conduct CRUD (Get, Post, Update, Delete) operation, manipulation of data, ensuring data integrity and consistency throughout the routing process.
# Backend (API, Database):
A Flask-based backend API is used which provides the core functionality for handling HTTP requests in the form of GET and POST related to route calculations and farm location management. Integrated with the PostgreSQL database, the API allows to efficiently retrieves and insert routing information, ensuring seamless interaction with the frontend web application. By implementing robust API endpoints, the backend facilitates data exchange between the database and the frontend, enabling dynamic route visualization and calculation.
# Frontend:
The frontend web application offers an intuitive user interface for interacting with the routing system. It is built using HTML, CSS, and JavaScript, which leverages the Leaflet.js library for map visualization.This allows users to make get request by inserting the id of farm locations , then it calculates distances, and visualize route information dynamically. The frontend also seamlessly communicates with the backend API to retrieve routing data and update the user interface in real-time.
![image](https://github.com/prog-proj-novaims/Shortest-Path-to-the-Closest-Paved-Road-in-Rural-Area-/assets/158604785/7542db2d-bcfc-4b9f-9b86-b11c9a0b61e0)

# Future Directions and challenges:
The were two main challenges we faced in this project, the first is allowing user to draw their own polygons representing the location from where the shortest path is calculated. And we are looking forword to resolve this issue to make the application more interactive and also to host a interesting database from places in which people whould have interest in know this kind of information. The second was related to nodes that were close to the origin but the path to them was longer than to the next node from a paved road. It can be a bit difficult to explain and to understand, but as an image can talk for one tousant words, this fugure ilustrate that [figures/example.png](https://github.com/prog-proj-novaims/paved-roads-routes/blob/276c08518d6e47d991b6e5c098a4762db80e6f84/figures/example.png)

Future enhancements to the project may include integrating real-time traffic data for dynamic route adjustments, implementing alternative route suggestions based on user preferences, and optimizing route planning algorithms for faster computation. Additionally, improvements in user interface design and deployment on scalable cloud platforms can enhance accessibility and performance, catering to a broader user base and supporting larger datasets.
# Conclusion:
In conclusion, the "Paved Roads Routes" project addresses the critical need for efficient route planning in agricultural contexts. By harnessing the power of OSM data, database management, ETL processes, and web technologies, the project provides a valuable tool for farmers to optimize transportation logistics and enhance productivity. With continued development and enhancements, the project holds significant potential to contribute to agricultural infrastructure planning and management, ultimately benefiting farming communities worldwide.
