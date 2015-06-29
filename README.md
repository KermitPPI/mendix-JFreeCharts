# mendix-JFreeCharts
This package allows you to visualize the data in your application by generating various charts.  It also provides you with the ability to view the charts in pdf form as well as the data.  

#Charts Available
#Multi-series
Bar Chart	
Line Chart

#Single-series
Ring Chart (Adaptation of pie chart)
	

#Contributing
For more information on contributing to this repository please visit Contributing to a GitHub repository!  This package was created using the JFreeCharts library, more information can be found on the JFreeCharts site, http://www.jfree.org/jfreechart/api/javadoc/index.html 

#Configuration
Implementation of this chart generator consists of the following steps:

1.	For the line and bar chart, a microflow is invoked which passes in a list of objects, an image object, a chart title, and a title for the x and y axis. 
2.	For the ring chart, a microflow is invoked that passes in a list of objects, an image object, and a chart title.  
3.	The list of objects are passed in by association (with a corresponding report).  
4.	A chart image is created and stored in an image object, the chart image can be viewed using an image viewer.  
5.	A pdf report is generated using a button which invokes a microflow.  The pdf document allows you to view the charts associated with each report as well as the data.

#1)	Data Source
The data source for the charts in this module consists of the list of parameters below:

•	List of Objects

•	Image Object

•	Chart Title

•	X-axis Title (Applies to Bar and Line Charts)

•	Y-axis Title (Applies to Bar and Line Charts)

#2)	Data Set
At least one dataset object should be associated with each report entity object.  The attributes for each dataset object are explained below: 

#Ring Chart
•	Report – Attribute that represents the report the data is associated with.

•	X-Value – Attribute in which the key values are used to plot the data in the chart, it is also used to generate the labels on the chart.

•	Y-Value – Attribute in which the values are the numerical values of the keys in the chart.

•	R, G, B Values – Attributes in which the values will be used to set the fill color of the ring chart sector in RGB format.

#Bar Chart

•	Report – Attribute that represents the report the data is associated with.

•	X-Value – Attribute in which the category values are used to plot the data in the chart.

•	Y-Value – Attribute in which the values are the numerical values of the corresponding series and category in the chart.

•	Series – Attribute in which the values are used to represent a series in the chart, it is also used to generate the legend of the chart.

•	R, G, B Values – Attributes in which the values will be used to set the fill color of the bars in RGB format.

#Line Chart

•	Report – Attribute that represents the report the data is associated with.

•	Series – Attribute in which the values are used to represent a series in the chart, it is also used to generate the legend of the chart.

•	X-Value – Attribute in which the values are the x numerical values of a data point for the corresponding series.  

•	Y-Value – Attribute in which the values are the y numerical values of a data point for the corresponding series.  

•	R,G,B Values – Attributes in which the values will be used to set the fill color of the lines for each series in RGB format.

#Behavior
Onclick microflow button

The microflow buttons trigger corresponding microflows which generates the charts for a set of data.  This is also done for pdf report generation. 

#Chart Settings
#Color
The module contains attributes which allow you to modify the fill color of the charts.  
**Note—Fill colors for the series in the bar and line charts should be consistent (please input the same RGB color for each series), if not, the module applies the first RGB color instance for that series to the chart.  

#Optional Customization  
Additional customization of the charts can be performed by adjusting some of the properties below:

#Background Color
The graphs can be customized by altering the background color.

#Show legend 
An option to display a legend is provided for each chart.  

#Size
The width and height of the chart image can be specified for display in the image viewer and in the pdf reports.    

For more information on customizing chart settings, please review the API documentation on the jfreecharts website at http://www.jfree.org/jfreechart/api/javadoc/index.html

#Help us improve
Feel free to suggest content or report issues on our github.  Thank you!



