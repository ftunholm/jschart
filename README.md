# jschart
Javascript chart library


1. Create a settings object, if the fields is left blank, default colors will be used.

	var settings = {
		"backgroundColor": "", 
		"chartColor": "",
		"chartLinesColor": "",
		"textColor": ""
		};

"backgroundColor" - sets the background of all rectangles as well as the canvas element.
"chartColor" - sets the color of the x-axis and the y-axis.
"chartLinesColor" - sets the color of the background lines in the chart.
"textColor" - sets the color of all the text.



2. Create a data object to store the information about the chart as well as the data to be drawn.

	var data = {
		"xName": "",
		"yName": "",
		"cols": [],
		"data": [{ "name": "", "values": [] }]
		};

"xName" - sets the name of the columns shown on x-axis.
"yName" - sets the name of the values shown on y-axis.
"cols" - sets the list of column names to be shown along the x-axis.
"data" - sets the list of data objects, containing a name (that would be the name of the line that is drawn to the chart) and a list of values for that line.



3. include the javascript file to your HTML and call the chartify() method passing the canvas element as first parameter, data object as the second parameter and settings object as the last parameter.



The following example shows how to use the chart:



<body>
	<canvas id="canvas" width="800" height="400" style="padding: 10px;">
		Canvas not supported!
	</canvas>

	<script type="text/javascript" src="chart.js"></script>	
	<script type="text/javascript">
		var canvas = document.getElementById("canvas");
		var settings = {
				"backgroundColor": "",
				"chartColor": "",
				"chartLinesColor": "",
				"textColor": ""
				};

		var data = {
			"xName": "Month",
			"yName": "Users",
			"cols": ["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sep", "Oct", "Nov", "Dec"],
			"data": [{ "name": "2016", "values": [6, 21, 60, 654, 323, 265, 282, 876, 111, 345, 899, 145] }]
			};

		chartify(canvas, data, settings);		
	</script>
</body>

