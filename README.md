# Mapping Walking & Cycling Access in Gouda, NL
Let's say you're a prospective homeowner looking to relocate to the compact, historic city of Gouda in the Netherlands. Or, let's say you're a city administrator who wants to know where a new bike path should be installed. Or maybe you're a researcher analyzing urban inequality on a neighborhood level.

This tool can help!

Using data collected from the [Gouda in Cijfers public databank](https://gouda.incijfers.nl/), I've created an interactive map tool that shows the walkability and bikeability of each neighborhood in Gouda.

## The Maps
![Screenshot of Walkability & Bikeability maps](https://github.com/user-attachments/assets/1a7287d5-5954-4ec6-b9cb-4c077574f101)

These maps visualize which neighborhoods in Gouda are most walkable and bikeable. These qualities are represented with index that measures how easy it is to get to various ammenities (such as grocery stores and schools) by walking or biking. A score of 100 for the walkability or bikeability index means you can reach all of your daily needs within a five-minute journey.

As you can see, while the entire city is quite bikeable, not all neighborhoods have great access to ammenities on foot.

If you want to see individual scores, head over to the [interactive maps on Tableau Public](https://public.tableau.com/views/GoudaWalkabilityandBikeability/GoudaAccessibilityIndices?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link). There you can hover over a neighborhood to see its score and compare it to surrounding areas.

![Screenshot of Walkability Index Map showing interactive elements](https://github.com/user-attachments/assets/e8f9d4e6-6642-4720-be37-4735d9c0c068)

## Methodology
The city of Gouda publishes [data](https://gouda.incijfers.nl/) on the average distance to various types of urban ammenities among residents of each neighborhood. I converted these distances into walkability and bikeability scores ranging from 0 to 100. 

A 100 means that the average resident of that neighborhood can reach an ammenity using that travel mode within five minutes. This is based on an average walking speed of 0.06 km per minute, and an average biking speed of 0.25 km per minute.

A 0 means that the average resident of that neighborhood has to travel for more than thirty minutes to reach their destination!

After calculating index scores for each ammenity, the scores were assigned weights to more accurately reflect how important each type of trip is for the average neighborhood resident. For example, access to a grocery store was weighed three times as much as access to a cinema.

Once the weighed results were calculated, the scores of each neighborhood were averaged to get the final walkability and bikeability index result.

Data cleaning and transformations were performed using Python code in a Jupyter Notebook instance hosted on [Kaggle](https://www.kaggle.com/). The code, as well as the datasets used in this analysis, can be downloaded above. The data visualization was generated using Tableau Public. The visualization, as well as the Tableau workbook file, can be downloaded from the [visualization page](https://public.tableau.com/views/GoudaWalkabilityandBikeability/GoudaAccessibilityIndices?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link). The geographic data used to generate the interactive map was downloaded from the city of Gouda's [Kaarten en Open Data](https://gis.gouda.nl/portal/page/kaarten-en-open-data;jsessionid=3CF4B18E2D748B2B707DF3DDB388ABC4) page.
