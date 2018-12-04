## Building A Dashboard D3.JS: Upstream Oil & Gas Data

In this tutorial I will attempt to build a dashboard to explore upstream oil and gas data (by upstream I mean each row of data contains all the information for a specific well).

Database is comprised of more than 23K wells located in [Eagle Ford](https://en.wikipedia.org/wiki/Eagle_Ford_Group) Shale in South West Texas. 
Data is scraped from public data web page of [Texas Railroad Commission](http://www.rrc.state.tx.us/about-us/resource-center/research/online-research-queries/), web scraping scripts are not included here.
The aim of this study is to create dashboards to explore data on the web. 

I created a csv data containing upstream data.
**Here are the description of each column in the csv data:**

1.	Completion_FluidVolume: fluid volume pumped during hydraulic fracturing process (gal)
2.	Completion_LateralLength: horizontal lateral length of wellbore (all wellbores are horizontally drilled) (ft)
3.	Completion_ProppantMass: total proppant mass pumped during hydraulic fracturing process (bbl)
4.	CompletionDate: Date of the well completion 
5.	Date_DrillingEnd: Drilling end date
6.	Date_SpudDate: Drilling start date
7.	Date_StartDate: Production start date
8.	Info_API: Unique API code identifier for this well
9.	Info_Name: Well name
10.	Info_Operator: Operator company name
11.	Info_ServiceCompany: Service company name
12.	Location_BLatitude: Bottomhole coordinate, Latitude
13.	Location_BLongitude: Bottomhole coordinate, Longitude
14.	Location_County: County name that well is located 
15.	Location_SLatitude: Surface coordinate, Latitude
16.	Location_SLongitude: Surface coordinate, Longitude
17.	Location_TVD: True Vertical Depth (ft) of wellbore 
18.	Prod_BOE12Month: First 12 month BOE production for each well (STB)
19.	Prod_BOE3Month: First 3 month BOE production for each well (STB)
20.	Prod_BOE6Month: First 6 month BOE production for each well (STB)
21.	Prod_Type: Type of fluid that this well produces (oil, gas,...)

I am not using all of the listed data column in this study. However, I am planning to use the rest of the data in future and expand this case study.

I used D3.js and Javascript to build this case study. If you have problem in loading data with Google Chrome, try to activate Internet Information Services (IIS) for Windows Server and load UpStream_DashBoard_EFStudy.html with Microsoft Edge.
Dashboard has 4 panels:
* Panel 1. (Top Left) Texas counties with more than 400 wells
* Panel 2. (Top Right) Surface locations of the wells color coded with respect to the producing fluid
* Panel 3. (Bottom Left) Average 6 month BOE Production (Oil + Oil equivalent production from gas) for each prdoucing year
* Panel 4. (Bottom Right) Top producing operator year by year (operator with highest average 6 month BOE with atleast 20 wells)

Once all files are loaded and complied, you should be able to see the following dashboard. You can zoom in the map and look for more details in the map:
![alt text](https://github.com/anejad/Upstream-Oil-Gas-Dashboard-With-D3.JS/blob/master/Dashboard.JPG)

