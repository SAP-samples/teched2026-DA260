# Create the seamless planning model in SAP Analytics Cloud
In this exercise, we will use the `V_PLANNING_SOURCE` view from SAP Datasphere and use it to build a seamless planning model. 

> [!TIP]  
> We will use the live version feature for seamless planning. Should you need more information, find it in the [SAP Community](https://community.sap.com/t5/technology-blog-posts-by-sap/unlocking-the-next-chapter-of-seamless-planning-in-sap-business-data-cloud/ba-p/14243864).
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

13. Edit the account dimension.
![](../images/ex1.2_17.png)

14. Toggle grid view.
![](../images/ex1.2_18.png)

15. Paste master data from this [Excel file]([../files/DA260_Account.xlsx](https://github.com/Sygyzmundovych/teched2026-DA260/raw/refs/heads/main/exercises/files/DA260_Account.xlsx)). Download it, open it and copy paste using keyboard shortcuts (CTRL+C / CTRL+V). 
![](../images/ex1.2_28.png)

For lines marked as base members in column D, only paste descriptions and hierarchy nodes. These account already exist in the dimension table in SAP Analytics Cloud. For all other accounts, copy, ID, description and hierarchy node.

The final result should look as follows:

![](../images/ex1.2_19.png)

16. Save the model

![](../images/ex1.2_23.png)
![](../images/ex1.2_24.png)

18. Expose the model's fact data in the data builder of SAP Datasphere. Call the table 'T_PLANNING_FACTS'.
![](../images/ex1.2_20.png)
![](../images/ex1.2_21.png)

17. Add a budget version by editing the 'Version' dimension table.
![](../images/ex1.2_25.png)
![](../images/ex1.2_26.png)

18. Extend the model's date range. Click on the token of the 'Date' dimension and set the range from 2024 to 2027.
![](../images/ex1.2_27.png)

19. Review the model structure and the data preview. Note the live connection of the 'Actual' version to the source view that we based our model on.
![](../images/ex1.2_22.png)

20. Save the model. Call it 'DA260_MODEL'.
![](../images/ex1.2_23.png)

> [!NOTE]  
> Number of records (as displayed in the data preview), overall sums and values can differ between the screenshots in this exercise and what you see in your models, stories, and previews. This can be due to recently added filters, standard data updates in the source etc. The transactional data does not matter too much in this workshop. So don't worry.

Continue to [exercise 1.3](ex1.3_load_budget_data.md).
