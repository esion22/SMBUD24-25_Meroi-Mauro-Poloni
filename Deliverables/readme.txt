The delivery folder is so organized:

- root directory -> this readme.txt file explaining how the folder is organized and the .pdf document describing the work done.

- dump -> contains the two dataset used for this project. "California.HousePricing.json" is the one used for the MongoDB part, instead "neo4j.dump" is the one for Neo4J as the name suggests. These dumps can be directly loaded into a DataBase; we recommend using MongoDBCompass and Neo4jDesktop to import them.

- Extra (Python notebook) -> for the extra we developed two python notebook, one for each technology used in this project. In order to run these notebooks the followings are necessary:
	- Jupiter: necessary to run any kind of notebook locally
	- a running mongoDB DataBase that you can connect to with the dataset already imported (we recommend using MongoDBCompass)
	- a running Neo4j DataBase that you can connect to with the datset already imported (we recommend using Neo4jDesktop).

- Pictures -> A folder with high-resolution pictures of all the pictures included in the delivery document.