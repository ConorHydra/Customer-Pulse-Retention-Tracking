---

  

description: Tableau is a powerful and fastest growing data visualization tool used in the Business Intelligence Industry.



---


# Integrating Hydra with [Tableau](https://www.tableau.com/))

  
## Scope

The focus of this guide is to showcase the ease of integrating Hydra with Tableau in order to track customer outreach and order actiity.

This Kaggle dataset can be used to understand marketing strategy based on consumer behaviour that can be adopted to increase customer retention of a retail store:
* Clickthrough rate (card)
* Orderfrequency (card)
* Daily order concentration (time-series line chart)

While simple, this will serve as a foundation for the development of more customer sales metrics.
  

## Setup

  

  

- Ensure you have the details of your Hydra instance handy.

  

- Sign up for a free trial at [Tableau](https://www.tableau.com/products/trial).

  

  

### Building the Table with Hydra


1. We will use sample sales data from [Kaggle](https://www.kaggle.com/datasets/uttamp/store-data?resource=download)). Download the CSV file.

  

2. Connect to your Hydra database and upload the .csv. If you're unfamiliar with the process of connecting via. psql and creating/populating a table, please follow this [guide](https://docs.hydra.so/centralize-data/load/from-local-csv-file).

    * The following code is used to create the store_data table:



      ```
      CREATE TABLE store_data (
          custid	CHAR
          retained	INT
          created	DATE
          firstorder	DATE
          lastorder	DATE
          esent	INT
          eopenrate	FLOAT
          eclickrate	FLOAT
          avgorder	FLOAT
          ordfreq	FLOAT
          paperless	INT
          refill	INT
          doorstep	INT
          favday	CHAR
          city CHAR

          )
      ```

  

3. You should now have a sales-oriented table populated with approximately 30,000 rows.

### Connecting Tableau with Hydra

  

  

Now we can configure Tableau to access our sample data in Hydra.

  

  

1. As mentioned earlier, create a [trial account][Tableau](https://www.tableau.com/products/trial).

  

2. Create a new workbook

  

3. Select Data and open the new data tab.

  

4. Click the connectors tab and select PostgreSQL 

  

5. Retrieve your database credentials from your Hydra dashboard. You will need Hostname, User, Password, and Database. Keep all other options unchanged. Once all the information has been entered, select **Sign in**.
    
   // ![Step_2](https://user-images.githubusercontent.com/71795488/227726544-8070700a-1525-4cb6-8ed3-24d0ab62155f.png)
   

Congratulations! You've connected Hydra with Tableau! What next?

Now that your data is connected, you're able to utilize your Hydra tables and create insights using Tableau visualization. Let's experiment with creating the below dashboard showcasing some important KPI's relating to customer interaction and orders.


   
 

