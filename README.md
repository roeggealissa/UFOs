# UFOs

# Using JavaScript and HTML to build an interactable webpage

### Introduction

The purpose of the project is to create a webpage to contain an article about UFOs as well as a searchable table of information about different UFO sightings. The table in particular should be searchable via an entry form for filters.

### Data Analysis

##### Data

The data is handed to us as a single JavaScript file containing dictionaries of sightings. The information included for each sighting is the date of the sighting,  the city state and country the sighting took place in, the shape of the UFO spotted, as well as any additional comments about the sighting from an unknown source. The software used for this project includes E6+, HTML, CSS, Bootstrap, and D3.

##### Analysis

The first step is the creation of an app that will let us build a table from the data JavaScript file as well as filter the data live on the webpage. After selecting the data from the data.js file, we create a function to build a table that is human readable on the website. The function takes each object in the data.js file and creates a row in the table and populates the cells with the information from the object. From there, we create two additional functions to hold the user input filter information and to create a new table based on the filters. The ability to have the user input their own text into a submission form will be done on the html side. The updateFilters function allows the user to put in multiple filters, such as state and date, and have the webpage use both of them to filter rather than only one. It also saves a few pieces of information, mainly the element, value, and ID of the filter used. The filterTable function filters the full table data based on the filters stored in the updateFilters function and displays that in the place of the full table on the webpage. A small line of code at the bottom allows us to update the table based on input into the user form without having a user press button to apply the filter specifically.

The html contains several parts. The first is the page header, a simple link back to the homepage (if we had other pages) with the text stating "UFO Sightings". Under this is a banner of an image of the Earth from the ISS with the title "The Truth is Out There" displayed over it. Scrolling down from that, Dana's article is under the banner. The title and subtitle of the article are on the left, and the article text is on the right. Directly under this is the table. The filter forms are on the left side of the screen, and the full table which will automatically update once we add filters is on the right.

### Website Results

![](https://github.com/roeggealissa/UFOs/blob/292a17facd92c554d438436bc00de62cc85326a5/images/webpage_snapshot.png)

### Website Issues and Recommendations 

The issues with this website and possible recommendations go hand in hand. First, allow javascript to access and display the contents of the paragraph rather than putting it into the html file directly. Placing it into the html file directly could get messy if the user wants to add additional articles or other pieces of text to the main webpage over time. Also, users most likely will not want to mess with the webpage code directly, so allowing them to place her text into a .js file that can then read the elements into the paragraph tags would possibly be her prefered way of adding additional content. In addition, we don't know how this webpage would handle more data. For now we only have just over 100 entries, but if we had thousands the page could slow adding them all in. In addition, and this might only matter if we had more columns or columns that could more easily be confused for one another, but we lose our filter form and our headers. One way around this is to periodically repeat the headers and have the form div move when tracking the scrolltop property. In the future with some outside/premade help, we can use jquery and datatables (datatables.net) to have an easily searchable table that won't affect performance.
