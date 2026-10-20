# Create the seamless planning model in SAP Analytics Cloud
In this exercise, we will use the `V_PLANNING_SOURCE` view from SAP Datasphere and use it to build a seamless planning model. 

> [!TIP]  
> We will use the live version feature for seamless planning. Find more information [here](https://community.sap.com/t5/technology-blog-posts-by-sap/unlocking-the-next-chapter-of-seamless-planning-in-sap-business-data-cloud/ba-p/14243864).
> More basic information on seamless planning can be found in [this blogpost](https://community.sap.com/t5/technology-blog-posts-by-sap/seamless-planning-integration-between-sap-analytics-cloud-and-sap/ba-p/13877679) and in the [SAP help](https://help.sap.com/docs/SAP_ANALYTICS_CLOUD/00f68c2e08b941f081002fd3691d86a7/6d81dcce234b417e8afb8450abab785e.html). 

1. Go to the modeler in [SAP Analytics Cloud](https://trial-bdc-sac-3.eu10.sapanalytics.cloud/sap/fpa/ui/app.html#/home)
![](../images/ex1.2_1.png)

2. Create new model. We start with data.
![](../images/ex1.2_2.png)
![](../images/ex1.2_3.png)

3. Select SAP Datasphere and your user's space as data storage location. Selecting SAP Datasphere as data storage location means that you will use seamless planning. You will see your space name <mark>`AC382806Uxx`</mark>. Use this space. 
![](../images/ex1.2_4.png)

4. Now you select the datasource for your model. We select *SAP Datasphere*. By that, we will directly create a live connection to our source view via a live version.
![](../images/ex1.2_5.png)

5. Select the view that you created in [exercise 1.1](../ex1_create_planning_model/ex1.1_create_DSP_view.md).
![](../images/ex1.2_6.png)

6. You now see the columns that you saw in the SAP Datasphere view. Start grouping columns by adding the 'CompanyCodeDescription' column as the description of the 'CompanyCode' column. 
![](../images/ex1.2_7.png)
![](../images/ex1.2_8.png)

7. Do the same for the product dimension.
![](../images/ex1.2_9.png)
![](../images/ex1.2_10.png)

8. Convert 'ProductGroup' and 'ProductHierarchy' to text properties of the 'Produt' dimension.
![](../images/ex1.2_11.png)
![](../images/ex1.2_12.png)

9. Create a level-based hierarchy.
![](../images/ex1.2_13.png)

10. Name the hierarchy. Set 'ProductHierarchy' as level 1 and 'ProductGroup' as level 2.
![](../images/ex1.2_14.png)

11. Create an account dimension from the 'Account' column.
![](../images/ex1.2_15.png)
![](../images/ex1.2_16.png)

13. 

> [!NOTE]  
> Number of records (as displayed in the data preview), overall sums and values can differ between the screenshots in this exercise and what you see in your models, stories, and previews. This can be due to recently added filters, standard data updates in the source etc. The transactional data does not matter too much in this workshop. So don't worry.
