# FDA-Inspect
Mapping web portal for FDA inspection data.

##Functional Specs / User Stories
Recreate functionality in Andrew's app: http://gis.truthinitiative.org/tobaccoviewer/ 
From the Truth Initiative Tobacco Viewer About section:  

>This application was developed as a tool that allows for the examination of changes in FDA compliance check inspections over time.
>The tool is integrated with Truth Initiative’s GIS portal, which allows users to explore how compliance check inspections may be
>associated with a range of other factors. Users can quickly zoom to their local area and bookmark their preferences as they overlay
>various data sources and visualize the results.

User Stories Format: "As a **type of user**, I want **some goal** so that **some reason**." 

###Data Layers 
>As a researcher, I want to have the ability to toggle on/off and zoom in/out on the following layers projected over a basemap so that >I can make visualize spatial comparisons/correlations between FDA violations and smoking behavior.":

   * [FDA Civil Money Penalties (10/12/10-2/28/15)](http://gis.truthinitiative.org/arcgis/rest/services/FDA/FDA_Civil_Money_Penalties_Complete/MapServer/0)
   * [FDA Warning Letters (10/12/10 - 2/28/15)](http://gis.truthinitiative.org/arcgis/rest/services/FDA/FDA_Warning_Letters_Complete/MapServer/0)
   * [FDA Civil Money Penalties (10/12/10-7/31/13)](http://gis.truthinitiative.org/arcgis/rest/services/FDA/FDA_Civil_Money_Penalties/MapServer/0)
   * [FDA Warning Letters (10/12/10 - 7/31/13)](http://gis.truthinitiative.org/arcgis/rest/services/FDA/FDA_Warning_Letters_Complete/MapServer/0)
   * [FDA State Contracts](http://gis.truthinitiative.org/arcgis/rest/services/FDA/FDA_State_Contracts/MapServer)
   * [State Synar Rates](http://gis.truthinitiative.org/arcgis/rest/services/FDA/State_Synar_Rates/MapServer)
   * [Smokefree Indoor Laws](http://gis.truthinitiative.org/arcgis/rest/services/WebApp/Smokefree_Indoor_Laws/MapServer)
   * [State Excise Tax 2013](http://gis.truthinitiative.org/arcgis/rest/services/WebApp/State_Excise_Tax_2013/MapServer)
   * [Youth Smoking Prevelance](http://gis.truthinitiative.org/arcgis/rest/services/WebApp/Youth_Smoking_Prevelance/MapServer)
   * [Adult Smoking Prevelance](http://gis.truthinitiative.org/arcgis/rest/services/WebApp/Adult_Smoking_Prevelance/MapServer)

###Search Functionality 
**Select Features**
>As a researcher, I want to be able to click on a **Search Compliance Checks** button that provides a dropdown list of layers (see >above) and allows feature selection by multiple selection tool types (point, line, freehand, rectangle, circle, polygon, freehand >polygon).

<img src="/images/select_search.png" width="400"> 

**Select by Attribute**
>As a researcher, I want to be able to click on a **Search Compliance Checks** button that provides a dropdown list of layers (see >above) and allows me to search by a query against the attributes in the layer that has been selected in the dropdown list. **Knowledge >of data and query string format is required*

<img src="/images/street_search.png" width="400"> 

**Layers to Search:**  
* [FDA Civil Money Penalties (10/12/10-7/31/13)](http://gis.truthinitiative.org/arcgis/rest/services/FDA/FDA_Civil_Money_Penalties/MapServer/0)
* [FDA Civil Money Penalties (10/12/10-2/28/15)](http://gis.truthinitiative.org/arcgis/rest/services/FDA/FDA_Civil_Money_Penalties_Complete/MapServer/0)
* [FDA Warning Letters (10/12/10 - 7/31/13)](http://gis.truthinitiative.org/arcgis/rest/services/FDA/FDA_Warning_Letters_Complete/MapServer/0)
* [FDA Warning Letters (10/12/10 - 2/28/15)](http://gis.truthinitiative.org/arcgis/rest/services/FDA/FDA_Warning_Letters_Complete/MapServer/0)  
<img src="/images/layers.png" width="400">   


**Legend**




###Technical Specs
