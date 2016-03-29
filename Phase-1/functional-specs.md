##Functional Specs / User Stories

User Stories Format: "As a **type of user**, I want **some goal** so that **some reason**." 

###Data Layers / ID Tool 
> As a researcher, I want to have the ability to toggle on/off and zoom in/out on the following layers projected over a basemap so that I can make visualize spatial comparisons/correlations between FDA violations and smoking behavior.":

*Bug: ID Tool is not working on points with multiple points - must zoom into single points.* 

   * [FDA Civil Money Penalties (10/12/10-2/28/15)](http://gis.truthinitiative.org/arcgis/rest/services/FDA/FDA_Civil_Money_Penalties_Complete/MapServer/0)    
   Example of linked doc URL: http://www.fda.gov/downloads/tobaccoproducts/guidancecomplianceregulatoryinformation/ucm428068.pdf    
   <img src="/images/civil_money_2015.png" width="200">

   * [FDA Warning Letters (10/12/10 - 2/28/15)](http://gis.truthinitiative.org/arcgis/rest/services/FDA/FDA_Warning_Letters_Complete/MapServer/0)   
   Example of linked doc URL: http://www.fda.gov/ICECI/EnforcementActions/WarningLetters/tobacco/ucm374485.htm    
   **Bug:** Link to document is not working.  
   <img src="/images/warning2015.png" width="200"> 

   * [FDA Civil Money Penalties (10/12/10-7/31/13)](http://gis.truthinitiative.org/arcgis/rest/services/FDA/FDA_Civil_Money_Penalties/MapServer/0) 
    Example of linked doc URL: http://www.fda.gov/downloads/tobaccoproducts/guidancecomplianceregulatoryinformation/ucm315938.pdf  
   <img src="/images/civil_money_2015.png" width="200"> 

   * [FDA Warning Letters (10/12/10 - 7/31/13)](http://gis.truthinitiative.org/arcgis/rest/services/FDA/FDA_Warning_Letters_Complete/MapServer/0)    
   Example of linked doc URL: http://www.fda.gov/ICECI/EnforcementActions/WarningLetters/tobacco/ucm302669.htm    
   **Bug:** Link to document is not working.  
   <img src="/images/civil_money_2015.png" width="200"> 
   
   * [FDA State Contracts](http://gis.truthinitiative.org/arcgis/rest/services/FDA/FDA_State_Contracts/MapServer) - Total Awards  
   2010 - 2015 awards and ammount and total listed      
   <img src="/images/state_contracts.png" width="200">  
   
   * [State Synar Rates](http://gis.truthinitiative.org/arcgis/rest/services/FDA/State_Synar_Rates/MapServer) - 2012 Quantiles; 2011 Quantiles  
   <img src="/images/synar.png" width="200">
   
   * [Smokefree Indoor Laws](http://gis.truthinitiative.org/arcgis/rest/services/WebApp/Smokefree_Indoor_Laws/MapServer) - Restaurants; Bars; Resturants & Bars; Workplaces; Restaurants, Bars & Workplaces  
   <img src="/images/bars.png" width="200">  

   * [State Excise Tax 2013](http://gis.truthinitiative.org/arcgis/rest/services/WebApp/State_Excise_Tax_2013/MapServer)  
   Shows taxes 2013 - 1995  
   <img src="/images/excise.png" width="200">  

   * [Youth Smoking Prevelance](http://gis.truthinitiative.org/arcgis/rest/services/WebApp/Youth_Smoking_Prevelance/MapServer) - 2011 Quanitles; 2009 Quantiles  
   <img src="/images/youth.png" width="200"> 
   
   * [Adult Smoking Prevelance](http://gis.truthinitiative.org/arcgis/rest/services/WebApp/Adult_Smoking_Prevelance/MapServer) - 2012 Quanitles; 2011 Quantiles; 2010 Quantiles  
   <img src="/images/adult.png" width="200"> 

###Search Functionality 
**Select Features**
**Bug**:*This functionality may not be currently working.*
> As a researcher, I want to be able to click on a **Search Compliance Checks** button that provides a dropdown list of layers (see above) and allows feature selection by multiple selection tool types (point, line, freehand, rectangle, circle, polygon, freehand polygon).

<img src="/images/select_search.png" width="400"> 

**Select by Attribute**
*This functionality may not be currently working. Knowledge of data and query string format is required.*  
> As a researcher, I want to be able to click on a **Search Compliance Checks** button that provides a dropdown list of layers (see above) and allows me to search by a query against the attributes in the layer that has been selected in the dropdown list. 

<img src="/images/street_search.png" width="400"> 

**Select by Block Group**
*This functionality may not be currently working.*  
> As a researcher, I want to be able to click on a **Search Compliance Checks** button, enter a blockgroup code (e.g. census_search.png) and return all layers' records in the selected block group. 

<img src="/images/census_search.png" width="400"> 




**Layers to Search:**  
* [FDA Civil Money Penalties (10/12/10-7/31/13)](http://gis.truthinitiative.org/arcgis/rest/services/FDA/FDA_Civil_Money_Penalties/MapServer/0)
* [FDA Civil Money Penalties (10/12/10-2/28/15)](http://gis.truthinitiative.org/arcgis/rest/services/FDA/FDA_Civil_Money_Penalties_Complete/MapServer/0)
* [FDA Warning Letters (10/12/10 - 7/31/13)](http://gis.truthinitiative.org/arcgis/rest/services/FDA/FDA_Warning_Letters_Complete/MapServer/0)
* [FDA Warning Letters (10/12/10 - 2/28/15)](http://gis.truthinitiative.org/arcgis/rest/services/FDA/FDA_Warning_Letters_Complete/MapServer/0)  
<img src="/images/layers.png" width="400">   


###Legend
Create a dynamic legend that responds to toggle on/off visiblity of layers.
<img src="/images/legend.png" width="400">


###Address Locator
Search by address:  
<img src="/images/address.png" width="300">

Search by lat/long:  
<img src="/images/latlong.png" width="300">

###Print Map  
Prints a PDF of map with title and subtitle.  

###Draw and Measure
<img src="/images/draw.png" width="300">
