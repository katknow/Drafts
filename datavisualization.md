# Data Visualization
The Data Visualization module allows site administrators are able to generate datasets and render diagrams that reflect their data. Once activated on the modules tab of the admin dashboard, Data Visualization is managed on a site by site basis. 

## Creating Data Visualizations
If the Data Visualization module is active, a tab for Data Visualization will appear in the menu for individual sites. Clicking this tab will take you to a list of all visualizations created for the site. You can sort the visualizations by either date or title in ascending or descending order.

![dataVis_sort](https://user-images.githubusercontent.com/84726696/131051672-0cc212d5-3020-4c0b-ada2-4674cde88f58.png)

## Adding a Data Visualization
After navigating to the Data Visualization tab, you can create a new visualization by clicking the *Add new visualization* button.

![dataVis_add](https://user-images.githubusercontent.com/84726696/131051829-a3e631ab-a6e0-4698-8295-cad73aaea921.png)

You will then have the option select what you would like to visualize. The five options include:
1. Count of items in item set, which visualizes the count of items that are assigned to selected item sets;
2. Count of items with classes, which visualizes the count of items that are instances of selected resource classes;
3. Count of items with properties, which visualizes the count of items that have selected properties;
4. Count of items with property values, which visualizes the count of items that have selected values of a selected property; 
5. County of property values, which visualizes the count of values of a selected property.

Once you select what you would like to visualize, click the *Next* button. This will take you to the "Add visualization" page. 

![dataVis_next](https://user-images.githubusercontent.com/84726696/131052131-57d44997-10ef-42e1-a9f8-f5742735e6c0.png)

The title field is required, but the description will be included below the title of your visualization on the public facing page if you wish to include it. Including a search query will help narrow down the items that will be used in your data set. If you choose to leave this blank, the visualization will incorporate all items assigned to that site.

To input a search query, select either the *Edit* button or the *Advanced edit* button. 

![dataVis_searchquery](https://user-images.githubusercontent.com/84726696/131052416-983ad158-ca29-484a-a8f8-9894471a3474.png)

If you select *Edit*, the drawer will open and allow you to search full-text, search by value, search by class, search by template, search by item set, or search by owner. You can either *Preview*, *Reset*, or *Apply* your search by selecting the corresponding button at the bottom of the drawer. 

![dataVis_edit](https://user-images.githubusercontent.com/84726696/131052323-b067f4b5-4fc7-41da-bd41-cd1bbe4846e8.png)

If you select *Advanced edit*, you will only need to fill in the provided textbook. To save your search query click *Apply*, or you can *Cancel* your search.

![dataVis_advedit](https://user-images.githubusercontent.com/84726696/131052357-7be0ae20-b594-4605-9a0e-149da737dae1.png)

### Data configuration
The options under "Dataset configuration" will reflect your selection of one of the five visualization options from the previous page. The first field will be "Dataset type," which indicates whether you selected count of item in item sets, count of items with classes, count of items with properties, count of items with property values, or count of property values.

#### Count of items in item sets
+ Click inside the "Item sets" field.
+ Select the item sets from the dropdown menu.
+ If you do not complete this step, you will receive an error when generating your data set.

![dataVis_itemsetconfig](https://user-images.githubusercontent.com/84726696/131908661-39540a21-2cd7-43e2-a8fe-ecc4c87a5697.png)

#### Count of items with classes
+ Click inside the "Classes" field.
+ Select the class from the dropdown menu.
+ If you do not complete this step, you will receive an error when generating your data set.

![dataVis_classesconfig](https://user-images.githubusercontent.com/84726696/131052578-41fd5082-ec8f-4e1e-9fd2-71b8509a7cc0.png)

#### Count of items with properties
+ Click insde the "Property" field.
+ Select the property from the dropdown menu.
+ If you do not complete this step, you will receive an error when generating your data set.

![dataVis_propertiesconfig](https://user-images.githubusercontent.com/84726696/131052664-ef7de140-d0b5-4bb2-ba12-bc619383b8a3.png)

#### Count of items with property values
+ Click insde the "Value property" field.
+ Select the value property from the dropdown menu.
+ Enter the specific values, separated by new lines, into the text box.
+ If you fail to fill out either of these fields, you will receive an error when generating your data set.

![dataVis_it prop valconfig](https://user-images.githubusercontent.com/84726696/131052839-f734ef05-cf1b-4a73-8133-b5be463f0796.png)

#### Count of property values
+ Click inside the "Value property" field.
+ Select the value property from the dropdown menu.
+ If you do not complete this step, you will receive an error when generating your data set.
+ Optional: either click inside the "Minimum count" field and enter the desired count or adjust the number via the arrows.
+ Optional: either click inside the "Maximum count" field and enter the desired count or adjust the number via the arrows.

![dataVis_prop val config](https://user-images.githubusercontent.com/84726696/131052950-0aced7dd-5889-4569-99db-663c9b5d8ddb.png)

### Diagram configuration
Under "Diagram configuration", you will be able to select the kind of diagram you would like to produce for your visualization. Options include bar chart, column chart, and pie chart. 

If you select bar chart or column chart, you will be asked to input the:
+ width
+ height
+ top margin
+ right margin
+ bottom margin
+ left margin

Additionally, you will be able to use a dropdown menu to order your data by value (ascending), by value (descending), by label (ascending), or by label (descending).

If you select pie chart, you will only be asked to input the width, height, and margin.

If you edit your visualization to change the Diagram Configuration after your initial visualization is produced, you will lose your current diagram configuration.

## Generating your visualization
Once you've configured your visualization, click the *Save and...* button. Then, select the box to "Generate dataset" and click "Stay on this visualization." 

![dataVis_saveand](https://user-images.githubusercontent.com/84726696/131053762-56ac93cf-b95c-43ab-8048-9d2fd35cd140.png)

Once your visualization is complete, you can click the *View...* button and select "Dataset" or "Diagram."

![dataVis_view](https://user-images.githubusercontent.com/84726696/131053960-06e2efbd-d5a8-4cb0-929a-9bbc9c003cd7.png)

If you select "Dataset," a new window will open that contains your dataset.

If you select "Diagram," a new tab will open containing your diagram. Diagrams will only generate in the context of a public site.

If the text is cramped in the axes of your graph, you will need to go back and adjust the margins.

## Publishing your visualization
To add your visualization to the public site, add a new "Data visualization" block to the page on which you would like it to appear. 

![dataVis_addblock](https://user-images.githubusercontent.com/84726696/131054312-eb985bda-0f5b-43c7-842b-60a7e4b4a0be.png)

In the new block, use the dropdown menu to select the visualization you would like to add to the page. 

![dataVis_addvis](https://user-images.githubusercontent.com/84726696/131054630-c3531350-c452-43ef-a3dd-47ee56d9b16b.png)

Then, click save. To remove the block, click the trash can icon.
