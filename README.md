# Retail-Sales-Data-Analysis

### Link of Dataset: https://www.myonlinetraininghub.com/workbook-downloads

### Period of time: 2016 Q3 to 2018 Q1

### DataSet: Australia retail store's sales data

## Data Preparation:

Create 5 Tables in Excel and import to PowerBI: 

Buyers: Buyers with varies categories(Kids,Women,Men,Accessories)

Dates: Monthly dates from 2016/1/1 to 2018/8/1

Managers: Sales Managers from different suburbs in Australia with postcodes

Regions: List of suburbs belongs to different states in Australia with postcodes

Sales: Sales detailed information including sales price,cost price,total units,category,supply chain and postcodes

## Data Transformation in Power Query:

Add custom column: "Sales" = [Sale Price]*[Total Units]

Add custom column: "Cost" = [Cost Price]*[Total Units]

Add custom column: "Gross Profit" = [Sales]-[Cost]

Set abve three columns to 'Decimal Number' and format as '%' with 0 decimal place

## Table Relationships check & Change inital Summarization,Category:

Create relationship between Sales table and Dates table

Change Summarization of Postcode and FY Month to 'Do not Summarize'

State categorized as 'State or Province',Suburbs categorized as 'Place',Postcode categorized as 'Postcode'

## Visulization of Dataset:

Add New Measure: GP % = SUM(Sales[Gross Profit])/SUM(Sales[Sales])

Add New column: State,Country = Regions[State]&", Australia" (categorized as 'State or Province')

Add New column: Postcode,Suburb,Country = Regions[Postcode]&", "&Regions[Suburb]&", Australia" (categorized as 'Postcode')

Summary Sheet: 
               
               breakout sales by date,chain,state,category

               identify relationship between sales and gross profit across querter
               
               charts using (KPI,Cluster Column,Pie,Fill Map,Bar Chart,Bubble Chart)
               
Region & Chain Sheet: 
                      
               NSW take the highest proportion of sales and "Ready Wear" chain as main source in all states except TAS.

               charts using (Map,Bar Chart,Area Chart,Multi-row Card,Column Chart,Custom Sparkline Chart)
