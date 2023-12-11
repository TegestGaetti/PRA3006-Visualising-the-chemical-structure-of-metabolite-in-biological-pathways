# Visualizing the Chemical Structure of Metabolites in Biological Pathways

This repository contains an HTML file presenting a webpage with a table of metabolites from a given pathway.

## Table of Contents
- [Project's Purpose](#projects-purpose)
- [Project's Explanation](#projects-explanation)
- [Code Structure](#code-structure)
- [Author](#author)
- [License](#license)

## Project's Purpose
The objective is to develop a website that displays a table with metabolites from a specific pathway sourced from WikiPathways. The CDK Depict service is used to show the 2D chemical structure of these metabolites.

## Project's Explanation
The project addresses the need for visualizing 2D chemical structures of metabolites in biological pathways. The webpage fetches data from WikiPathways using the SPARQL endpoint and utilizes the CDK Depict service.

SPARQL endpoint: [Wikidata Query Service & WikiPathways Snorql UI](https://sparql.wikipathways.org/sparql/)

## Code Structure
### Style (head)
The "style" sectionof the HTML code for the aestetics of the webpage: the font of the webpage, the color, fontsize, alligmnet and paddiing of the caption, rows and colums of the table and the layout of the table.

### Search Tab Structured
With "div" the code introduces a serach tab, which whill have a input type that os "text" and the name of the serach tab "Search" is displyed on the left of the tab and writte ìn in bolad. 

### Table (body)
In the body of the HTML file, the table is created with two colums: one for the *name* of the metabolites and the other for the *structure* of the molecules. The cation of the table is also introcued. 

The body of the table is empty, its ID is used in another section of the code to fill the table.

### Script
It contains the JavaScript code to fill the table and introcude the graphics of the webpage.

#### SPARQL Query
This section inserts the SPARQL query created with the SPARQL WIKIPATHWAYS endpoint: https://sparql.wikipathways.org/sparql/.
It select the metabolites of the chosen pathway and it SMILES structure. SMILES is app that provides images of the desired molecule, given the required molecular struture in the correct SMILES form.

#### AJAX
The function AJAX request the the two elements form the SPARQL endpoint and stores them in the variables *molecules* and *smilesURL*.
*smilesURL* contains the URL to fetch the webpage with the image of each molecule.
The two variables are collected in the array list named *sparqlData*.

#### Build Table
The function buldtalable takes the elemts form the *sparqlData* and form each elemnt creates a row with two cells that relate to the name and strucure of the molecules dierectly. (the Structure element is conevted into image first.) The rows are appenend to the table sequentually.

#### Search Tab
This section deals with the input provided in the serach tab and provides a table with all the elemnts containing the letters input.

#### Sort by Column
This part of the code handles events in which the headline of the columns is clicked on. According to the order, the molecules are listed; each click will allow displaying the table in ascending or descending alphabetical order of the name of the metabolites.



## Author
- [Tegest Gaetti (@TegestGaetti)]()


## License 
- [MIT LICENSE](LICENSE)