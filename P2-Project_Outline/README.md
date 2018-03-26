### Overview
I am employed at an environmental laboratory.  Our customers send us environmental samples and ask us to test for various toxins and pollutants.  We analyze the provided samples and then report the results back to the customer.  Our laboratory information management software (LIMS) is quite old.  The architecture and network infrastructure have not changed significantly in the past 15 years.

A chemist analyzes samples on an instrument and the raw results are stored on a locally connected PC in one of several proprietary formats which varies by instrument type.  The analyst then runs a legacy piece of software that is referred to as a "Data Transfer (DT)" program which takes the raw data, performs many calculations and produces a data file which can be imported into our central LIMS database.

These Data Transfer programs are standalone Microsoft Access programs which must be loaded on each instrument PC individually.  They were written many years ago and are very brittle and difficult to maintain.  My project idea is to take one of these DT programs, reverse engineer it and convert it into a web app.

### Features

* Import Batch: A user will be able to import a batch of analytical results from a file using a proprietary format.  The batch of analytical results will be stored in one or more database tables accessible to the server.

* Update Batch and Calculate Final Results:  A user will be able to update information associated with a Batch as well as calculate and edit Final Results.

* Export Batch Results:  A user will be able to export the Final Results for a Batch to a common file format which can be subsequently imported into the central LIMS database.

* Edit Configuration Data:  Users who have been granted administrative privileges will be able to create, edit or delete configuration data for the system which will be stored in the database.

### Technologies

* Python
* Flask
* MySQL or Oracle
* SQLAlchemy
* Jinja2 templates

### What I'll Have to Learn

The Data Transfer program that I will be replacing was designed to be displayed on a specific size of PC monitor.  The application windows are instantiated full screen and cannot be resized.  Much of the data is presented in very wide tabular form.  Many tables have twenty or more columns and heavily rely on horizontal scrolling.  In general, the web apps that I am familiar with were designed for vertical scrolling only.  I don't have any intention of making a fully responsive application, but I do plan on making the windows resizable and will have to explore different techniques for mitigating my extreme width problem perhaps using overflow areas or multiline records.
