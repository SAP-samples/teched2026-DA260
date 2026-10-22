# Load budget data
In this exercise, you will add budget data to your model via a data import job. 

1. Download this [Excel file](https://github.com/SAP-samples/teched2026-DA260/raw/refs/heads/main/exercises/files/AM_DA260_BASE_BUD.xlsx) to your computer. 

2. Navigate to Data Management.

![](../images/ex1.3_1.png)

3. Import data
![](../images/ex1.3_2.png)

4. Select the Excel file you just downloaded.

   ![](../images/ex1.3_3.png)

6. Set up the import.
   ![](../images/ex1.3_4.png)

7. Open the Company Code column etails and set the column as String. If it is String already, move on. 
![](../images/ex1.3_14.png)
![](../images/ex1.3_6.png)

8. Set 'Account' and 'AccountParent' as String. You can do so by clicking on the column header names in the grids.
![](../images/ex1.3_6a.png)
![](../images/ex1.3_6b.png)

9. Click 'Next'.
 ![](../images/ex1.3_7.png)

10. Set 'Public.Budget' as default version.
 ![](../images/ex1.3_8.png)
 ![](../images/ex1.3_9.png)

11. Map 'CompanyCodeDescription', 'ProductDescription', 'ProductGroup', 'ProductHierarchy' as per the image below. Then click next.
 ![](../images/ex1.3_10.png)

12. Map 'AccountParent'
 ![](../images/ex1.3_13.png)

13. Click 'Next', 'Run Import' and 'Finish'
 ![](../images/ex1.3_11.png)
 ![](../images/ex1.3_12.png)

Move on to [exercise 2](../ex2_create_planning_story/ex2_create_planning_story.md) to create a story and plan. 
