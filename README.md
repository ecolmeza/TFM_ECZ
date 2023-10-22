# TFM_ECZ
# title: "Temporary series: TFM sales forecast"
# author: "Eduardo Colmenares"
# Project summary: 

This model predicts the volume of shipments based on historical data of a business.

# Software:

RSTUDIO is used to model the temporary series is RSTUDIO 
   List of packages need it in the model ( knitr, ggplot2, patchwork, tidyverse, dslabs
       lubridate, purrr, pdftools, fracdiff, fpp2, tseries, TTR, seasonal, zoo, xts, greybox
       smooth, Metrics, gridExtra, prophet)
   
POWERBI is used to data visualization, to explain the real data and deviation of the forecast. 

# Data files:

- Historical Data from business ERP - Prod_factVT2.csv
- Summarized services - Service_type.csv
- Labor days - DIAS LAB.csv


# How to run the model:

1 - Updated historical data from business production ERP

Extract in a monthly basis the “camara” information from the business ERP in the menu allow to that purpose, make sure that the invoicing process is finished. 

Copy and paste the information in last row of the file Prod_factVT2.csv 
   
Data detail of the file 
  
-	Date – Date of the invoicing process (Camara). 
-	Client – Internal client code.
-	Service – Codification of the business services.
-	Country 
-	C – Country code 
-	Shipments – Number of shipments 
-	Import – Amount invoice to the client   
-	Discount – Discount applied to the client.


2 - Update new services 

If a new service code is implemented in the business, is necessary to include that code in the File Service_type.csv and assigned the service in the following categories:

-	PREM – High quality services 
-	19H – Standard courier service 
-	PPACK – Pluspack services  
-	ECOM – Ecommerce clients service
-	I – International servicesOT – Other services 

3 - Update Labor days  

Every time is need it update labor dates for including the forecast months of the model.

The period of forecasting is 17 months  

4 - Run the RSTUDIO MODEL 

The files model and the 3 files of data need to be in the same directory 

Then run the RSTUDIO file name Sales_TimeSeries_TFMV4.Rmd until the forecast excel is updated with the new information 
(file predictionsServicesEXCEL.csv)


# FRONT END 

Open the PowerBI file FORECASTDATA.pbix
Update the information in powerbi desktop.
 


NOTE: For analytical process only update real date and POWERBI until the next forecast process is need it. 



# Output: 

Shipments evolution of the business, with service detail 
Predictions of future production - file predictionsServicesEXCEL.csv
- 17 months forecast of services groups (Excel Columns FS_xxxservice) 
Deviation analysis of the predictions with POWERBI 


