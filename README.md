# Systems and Methods for Big and Unstructured Data (SMBUD) - Course Project

This repository contains the project developed for the Systems and Methods for Big and Unstructured Data (SMBUD) course at Politecnico di Milano during the Academic Year 2024-2025.

**Group Number**: 41  
**Group Members**: Lorenzo Meroi, Simone Mauro, Francesco Poloni  
**Evaluation**: 2/2.5

## Project Overview

The project is split into two main sections focusing on different NoSQL technologies: MongoDB (a document-oriented database) and Neo4j (a graph-oriented database). It includes data modeling, injection, query optimization, and programmatic analysis using Python notebooks.

### 1. MongoDB - California Housing Price Analysis
This part of the project models and analyzes data from the 1990 California census concerning housing values.
* **Dataset**: California Housing Prices (originating from Kaggle/OpenML), representing indices like housing price, location, median age, income, and proximity to the ocean.
* **Database Modeling**: The data was structured into embedded documents (Block, Housing, Population & Income) to design a single, efficient MongoDB document layout per geographic block.
* **Python Notebook**: `Deliverables/Extra (Python notebook)/MongoDB.ipynb` performs statistical analysis and data visualization. It displays graphs of house prices relative to block location and population density, and details the correlation between the various dataset variables.

### 2. Neo4j - London Transport Routing
This part of the project models and queries the London transportation network (metro lines, train stations, and bus stops).
* **Dataset**: TfL Bus Stop Locations and Routes (London Datastore), representing the London transport network from 2010.
* **Database Modeling**: Modeled as a graph where Metro/Train stations and Bus stops are nodes, and connections are relationships (`CONNECTED_BY` for stations, `NEXT_STOP` for buses).
* **Python Notebook**: `Deliverables/Extra (Python notebook)/Neo4j.ipynb` visualizes the network and implements a custom pathfinding algorithm to route journeys from one stop/station to another. It includes the ability to transition between stops by foot when they are within a specific geographic distance (calculated using coordinates).

---

## Repository Structure

* `Deliverables/`
  * `Extra (Python notebook)/`
    * `MongoDB.ipynb` - Statistical analysis and visualization for the California housing dataset.
    * `Neo4j.ipynb` - Network routing and visualization for the London transport network.
  * `dump/`
    * `California.HousePricing.json` - JSON dump for MongoDB collection.
    * `neo4j.dump` - Database dump for Neo4j.
  * `Pictures/` - High-resolution diagrams used in the project report.
  * `readme.txt` - Deliverables directory description.
* `LaTeX/` - LaTeX source files and assets used to compile the project report.
  * `Project.tex` - Main LaTeX file containing the project report.
* `README.md` - Main repository README file.

---

## Prerequisites and Execution

To run the notebooks locally, you will need:
1. **Jupyter Notebook**: A running Jupyter environment (e.g., via VS Code, PyCharm, or Jupyter Lab).
2. **MongoDB**: A running MongoDB instance (localhost:27017) with the `California.HousePricing.json` dataset imported.
3. **Neo4j**: A running Neo4j instance (localhost:7687) with the `neo4j.dump` database dump loaded.
4. **Python Dependencies**: PyMongo, Neo4j Python Driver, Py2neo, Pandas, Matplotlib, Seaborn, and other standard libraries as imported in the notebooks.