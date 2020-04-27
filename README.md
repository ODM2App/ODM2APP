# ODM2APP
ODM2 APP is a software ecosystem for the management of  <b>Observations & Measurements (O&M)</b>, based on the Observation Data Model 2 (<a href="https://github.com/ODM2">ODM2</a>).
This is an information data model for feature-based earth observations, designed to facilitate interoperability across scientific disciplines and domain cyberinfrastructures (read more <a href="https://www.sciencedirect.com/science/article/pii/S1364815216300093">here</a>). The Open Geospatial Consortium also published a conceptual model (ISO Observations and Measurements (O&M) conceptual model O&M, published also as ISO/DIS 19156).
ODM2APP exposes an environment to insert and manage O&M data, based on a physical implementation of the <a href="https://github.com/ODM2">ODM2</a>. Namely Update, Insert and Delete operations are possible. PostgreSQL/PostGIS is the RDBMS engine that hosts the physical implementation of the database. 
# Objectives
The ODM2 App's goal is to ease the use and maintanance of O&M data, based on the ODM2 data model. ODM2APP is a web-based information system that exposes an environment to insert, manage the O&M data and ease the report production mechanism. The physical ODM2 tables exploited by the App comprises Core, Sampling features, Provenance, Results. ODM2 App is a modular ecosystem that can be further developed and extended to manage any spatially-discrete, feature-based earth observations.
# The App / Project
The App has been developed using the <a href="http://www.altoframework.com/">Alto framework</a>, namely Alto. This is an enterprise, full-stack, modular, low code development framework to design and develop professional Web information systems, services, and dynamic applications for advanced analysis and reporting. 
Alto exposes:
i) a user friendly web editor with a powerful GUI;
ii) a fast and flexible processing system for application development;
iii) a suite of widget engines to create complex HTML objects such as GIS maps, tables, graphs, search emgines, forms, etc.;
iv) a distributed Collaborative Working Environment where large communities can cooperatively create Web applications.
The project is distributed as: 
<ol>
  <li> a Json file (this can be loaded to Alto for further development or customization);</li>
  <li> a WAR file (this can be directly deployed to the web application container (e.g. Tomcat or JBOSS));</li>
  <li> a Docker (this is a ready to use VM) to be exposed on the web. </li>
</ol>  

# Variations to the ODM2 schema
A few important changes have been applied to the ODM2 schema:
1. all tables have new fields: 
<br> i) <b>active</b>: a boolean field used for delete operations or change operations. No real delete/edit operation will be applied to the data, but a 0 will be applied to the row that is updated or deleted. In case of update operation a new row will be created and the "active" field will be set to 1. 
<br> ii) <b> date_ins</b>: each operation will be saved with the date (yyyy,mm,dd, hh:mm) of the data entry.
<br> iii) <b> id_user_ins</b> this field is used to record the user that has done the change/insert operation.
<br> The changes were made necessary to meet the needs of enterprise organizations deputed to the characterization and monitoring of various media (air, soil, water, etc.), crops cycle, etc. A key question that we are addressing is to guarantee quality. The quality procedure is the heart and soul of our data management system. The APP quality procedures establish processes that make sure everything is performed according expectations and that at any moment it is possibe to view what, when and who performed the changes to the O&M data. 
2. All tables within the physical schema have small letters.

# Contributors
This project is actively supported by:
<br> Pierluigi Cau 
<br> Davide Muroni
<br> Carlo Milesi
<br> Amin Hammami
<br> Paweł Wcisło 

# License
Licensed under the <a href="https://github.com/snapappointments/bootstrap-select/blob/v1.13.0-dev/"> the MIT LICENSE</a>.
