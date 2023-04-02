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
    
   
![Tableau to HYDRA](https://user-images.githubusercontent.com/129688085/229379169-68f355d7-aa2b-498a-9db6-3de293f28b51.png)

Congratulations! You've connected Hydra with Tableau! What next?
![Data Loaded](https://user-images.githubusercontent.com/129688085/229379193-949f5118-935c-4dad-8983-a829f341f5c8.png)

Now that your data is connected, you're able to utilize your Hydra tables and create insights using Tableau visualization. Let's experiment with creating the below dashboard showcasing some important KPI's relating to customer interaction and orders.

1. Create a worksheet and pull in the Eclickrate column. Edit the dimension to append the column name into the AVG() adaptor. Change the Show ME visual choice from bar chart to text tables and hide the title.
![AVG ClickRate](https://user-images.githubusercontent.com/129688085/229379200-8fb3c67c-3ebd-4653-9a33-7e4071b288bb.png)


2. Create a worksheet and pull in the Ordfreq column. Edit the dimension to append the column name into the AVG() adaptor. Change the Show ME visual choice from bar chart to text tables and hide the title.

![AVG Ordfreq](https://user-images.githubusercontent.com/129688085/229379205-4fc390d0-560f-4e96-98cf-5268ea75afca.png)

3. Create a worksheet and pull in the avgorder column. Edit the dimension to append the column name into the AVG() adaptor. Change the Show ME visual choice from bar chart to text tables and hide the title.

![AVG Order](https://user-images.githubusercontent.com/129688085/229379209-18f53d9a-7312-4cc4-845f-6ae1329de513.png)

4. Open the Dashboard 1 tab. From this dash you can drag and positions the seperate statistics. 
![DASH](https://user-images.githubusercontent.com/129688085/229379215-e47b28f6-fc0a-4e9a-98f8-90e69b5fd7b3.png)


### You're now done! Congratulations on creating your first Hydra x Tableau KPI dashboard!


   
 

