# ODM2APP
ODM2 APP is a software ecosystem for the management of the Observations Data Model (<a href="https://github.com/ODM2">ODM2</a>).
ODM2 is an information data model for feature-based earth observations, designed to facilitate interoperability across scientific disciplines and domain cyberinfrastructures. The ODM2 data model is supported by the Open Geospatial Consortium's (OGC).
ODM APP exposes an environment to insert and manage O&M data. Namely Update, Insert and Delete operations are possible. PostgreSQL/PostGIS is the RDBMS engine that hosts the physical implementation of the ODM2. 
# Objectives
The ODM2 App's goal is to provide an information system to connect to the ODM2 data model. The APP exposes an environment to insert and manage O&M data. The physical ODM2 tables exploited by the App comprises Core, Sampling features, Provenance, Results. ODM2 App is a modular ecosystem that can be further developed and extended to manage the spatially-discrete, feature-based earth observations.
# The App / Project
The App has been developed using the <a href="http://www.altoframework.com/">Alto framework</a>, namely Alto. This is a full-stack, modular, development framework to design and develop professional Web information systems, services, and dynamic applications for advanced analysis and reporting. 
Alto exposes:
a user friendly web editor with a powerful GUI.
a fast and flexible processing system for application development.
a suite of widget engines to create complex HTML objects such as GIS maps, tables, graphs, search emgines, forms, etc.
a distributed Collaborative Working Environment where large communities can cooperatively create Web applications.
Alto transparently combines, in one space, technologies to access, query and process complex data infrastructures, thus increasing the interoperability between applications.
# Variations to the ODM2 schema
A few important changes have been applied to the ODM2 schema:
1. all tables have 2 new fields: 
i) <b>active</b>: a boolean field used for delete operations or change operations. No real delete/edit operation will be applied to the data, but a 0 will be applied to the row that is updated or deleted. In case of update operation a new row will be created and  the "active" field will be set to 1. 
ii) <b>data_ins</b>: each operation will be saved with tha date (yyyy,mm,dd, hh:mm) of the data entry.
2. All tables within the physical schema have small letters.
# Contributors
This project is actively supported by:
<br> Pierluigi Cau 
<br> Davide Muroni
<br> Carlo Milesi

