# UFO Sightseeing

## Overview

The purpose of this analysis is to show Dana's webpage which includes a dynamic table that updates the information about UFOs sightseeings and allowing users to filter for multiple criteria at the same time, including date, city, state, country and shape filters.

For this we used JavaScript to listen for the user's input and rebuild the table with the filtered data.

### Resources

- Data source: Table raw info is proivded in the file *'data.js'*.

- Software use to perform the analysis: Google Chrome 99.0.4844.51, JavaScript 1.7 Brower dependent, Visual Studio 1.65.0


## Results

### Webpage display and coding

- The webpage is displayed throught the *index.html* file, so anyone entering the root directory of the server where the page is stored should be directed to the page.

    ![Webpage Overview](/static/images/webpage.png)


- The code used is simple HMTL with CSS styling. We used bootstrap 4.0 and a css style sheet for the background color and jumbotron backround image and font.

    |**HTML Code**                             |**style.css**                              |
    |:----------------------------------------:|:-----------------------------------------:|
    |![HTML Code](/static/images/html_code.png)|![CSS styles](/static/images/style_css.png)|

- Each time the page is loaded, the script of *app.js* is called.

### Structure

- The webpage is divided into four main sections. The navbar has a link to return to the homepage if in the future more sections are added.

    ![Webpage Overview](/static/images/structure.png)

### Javascript table

- The first table displayed shows all unfiltered values from the *data.js* file. Data is loaded according to the order in the file.

    ![Unfiltered table](/static/images/nofilt_table.png)

- Then the user may enter the values for each of the filters displayed: date, city, state, country and shape. The filter can be applied to one or more fields at the same time.  When the user presses enter, the new filtered table will be displayed. In the next example, we use filter for date:'1/1/2010'; state:'ca' and country:'us'.

    ![Filtered table](/static/images/filt_table.png)

- If the user wants to eliminate one or more criteria from the filters, he/she has to delete the values from the input fields.

- After grabing each of the filter inputs, we assing them to an object in the code and then use the following code to loop into the code and filter the data for each of these filters.  Then we send the filtered data to a function (buildTable) that shows the filtered data in the webpage.

    ![Code to filter](/static/images/code_filter.png)

## Summary

- JavaScript allows Dana's webpage to be dynamic.  However, the main drawback of her page is that the data source is static, meaning that it needs to have additional code to update data, maybe scraping it from other webpages or through APIs.  It also has only one webpage, so it would be good to add more pages regarding other themes related to the subject.

### Recommendations

- The first recommendation is regarding the filters. Users have to scroll through the entire table to look for the available values for each filter.  It would be recommended to have drop menus that show the availabe options.  In the case of dates, add filters for range of dates.

- A second recommendation is to add column filters for ascending or descending order.

- A third recommendation is to include input validation to the filters so the user knows if the format or the values do not match.

- A fourth recommendation is to include a "clear all" button if the user wants to clear the criteria from all input fields.
