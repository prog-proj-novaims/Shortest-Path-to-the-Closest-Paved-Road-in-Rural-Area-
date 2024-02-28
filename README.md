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
Certainly! Here's an improved version of the text:

# ETL Process
The Extract, Transform, Load (ETL) process plays a pivotal role in preparing and processing OpenStreetMap (OSM) data for route calculations. Let's delve into the key components of this process:

1. **Data Extraction and Initial Processing**:
    - Initially, raw OSM data is downloaded in PBF (Protobuf Binary Format) format.
    - The 'osmconvert' tool is then used to extract relevant road network information from this data.
    - The extracted data includes road segments, intersections, and geographic coordinates.

2. **Data Transformation and Loading**:
    - The processed data is imported into a PostgreSQL database using the **'osm2pgrouting'** tool.
    - This step optimizes the data for efficient routing operations.
    - Additionally, an ETL process extracts surface information for road segments within predefined grid cells.
    - Considering road surface data enhances the accuracy of route planning.

# Database Utilization:
- A PostgreSQL database serves as the central repository for storing and managing the extracted OSM data.
- The database is meticulously designed with a well-defined schema.
- It efficiently organizes road network information, farm locations, and route results.
- This relational database management system supports CRUD (Create, Read, Update, Delete) operations, ensuring data integrity and consistency throughout the routing process.

# Backend (API, Database):
- The backend of the system is powered by a Flask-based API.
- It handles HTTP requests related to route calculations and farm location management.
- Integrated with the PostgreSQL database, the API efficiently retrieves and inserts routing information.
- This seamless interaction between the backend and frontend ensures dynamic route visualization and calculation.

# Frontend:
- The frontend web application provides an intuitive user interface for interacting with the routing system.
- Built using HTML, CSS, and JavaScript, it leverages the Leaflet.js library for map visualization.
- Users can input farm location IDs, calculate distances, and visualize route information.
- The frontend bridges the gap between users and the underlying routing functionality..
