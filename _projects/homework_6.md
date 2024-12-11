---
name: Homework 6
tools: [Python, HTML, vega-lite, Altair]
image: assets/pngs/cars.png
description: This visualizes data from the Building Inventory dataset.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Visualization 1: Distribution of Building Types


<vegachart schema-url="{{ site.baseurl }}/assets/json/jsonbuilding_inventory_distribution.json" style="width: 100%"></vegachart>

This visualization shows the distribution of building types and the number of buildings. It was altered from homework 5, where it was originally created using streamlit. Each building type has a unique color. This choice adds clarity, allowing viewers to easily identify different building types and distinguish them in tooltips. When users hover over a bar, they can see the building type and its count. This interactivity makes the chart more engaging and informative by providing precise data without cluttering the main visualization. As for the encoding types, on the x-axis quantitative encoding is used for the count of buildings. On the y-axis, nominal encoding is used for building types, and the color on the visualization represends the building types.

# Visualization 2: Buildings Constructed Over Time by Agency


<vegachart schema-url="{{ site.baseurl }}/assets/json/jsonbuilding_inventory.json" style="width: 100%"></vegachart>

This visualization is a multi-line chart that depicts the number of buildings constructed over time, grouped by agency. It allows for an analysis of construction trends across agencies and highlights how construction activities vary over the years. The x-axis uses quantitative encoding for the construction year formatted as integers, the y-axis also uses quantitative encoding for the count of buildings constructed in a given year. The color represents encoding for the agency name. A multi-select legend allows users to filter the chart dynamically, focusing on specific agencies. Tooltips provides detailed information (year, building count, and agency) on hover. The year constructed column to numeric values, coercing invalid entries into NaN for better handling. rows with missing or invalid values for Year Constructed and Agency Name were dropped. 
## Search The Data & Methods

Below is where we can put some links to both the data and the analysis code as buttons:


<!-- these are written in a combo of html and liquid --> 

<div class="left">
<a class="m-1 btn btn-outline-primary btn-2 " href="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv">
  The Data
</a>
</div>

<a class="m-1 btn btn-outline-primary btn-2 " href="https://github.com/esbeidagarcia/esbeidagarcia.github.io/blob/d53777b0a1aa83316f6d66065524e00649e79546/python_notebooks/homework6.ipynb">
  The Analysis
</a>
