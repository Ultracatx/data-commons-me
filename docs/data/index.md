[Data Commons](../../)

# UN Goal Timelines - Data Pull

Cool: [Data Commons Sheets add-on](https://docs.datacommons.org/api/sheets/)

Two Colabs:

1. [Map Filter Colab](https://colab.research.google.com/drive/1riRnKUGNGkJZOU6qJoznAxjySInQjnFQ?usp=sharing) outputs for one year for our [Map Nav](#geoview=country). It includes Population, CO2 and Methane.

2. [UN Goals Timelines CoLab](https://colab.research.google.com/drive/1LZC8ot8skRMtD4DnokDjYXH6B73WinYP?usp=sharing) and DCIDs from our <a href="https://docs.google.com/spreadsheets/d/1IGyvcMV5wkGaIWM5dyB-vQIXXZFJUMV3WRf_UmyLkRk/edit?usp=sharing" target="googleUnGoals">Google Sheet UN goal tabs</a>

TO DO: Update our UN Goals Colab to pull DCID's from our <a href="https://docs.google.com/spreadsheets/d/1IGyvcMV5wkGaIWM5dyB-vQIXXZFJUMV3WRf_UmyLkRk/edit?usp=sharing" target="googleUnGoals">Google Sheet Goal tabs</a> - Priyanka, Alexandra, everyone

<!--
[Our Run Models Colab](https://colab.research.google.com/drive/1zu0WcCiIJ5X3iN1Hd1KSW4dGn0JuodB8?usp=sharing#scrollTo=Z12cWU4y09on) already includes a process for saving CSV files to GitHub. The relevant part happens around saving the integrated dataset to the repo.
-->

<!--
Abhishek L may also have .ipynb files that generate .csv files locally. The output .csv could be sent to a fork of [data-commons](https://github.com/ModelEarth/data-commons) in a folder added at data-common/docs/data.
-->

TO DO: Update our [Google Sheet UN Goal tabs](https://docs.google.com/spreadsheets/d/1IGyvcMV5wkGaIWM5dyB-vQIXXZFJUMV3WRf_UmyLkRk/edit?usp=sharing) with additional DCID values that we'll pull for our Python .csv file generation. - Everyone <!--Pratyush-->

<!--
TO DO: Also update our [Data Commons Timelines CoLab](https://colab.research.google.com/drive/1PF8wojIOHxDCdmadsAdkpHnb-An1ymEh?usp=sharing)
-->

TO DO: In the UN Goals Colab, the [country.csv timeline output Abhishek created](https://github.com/ModelEarth/community-data/blob/master/locations/datacommons/country.csv) can be output to data-commons/docs/data/air/[dcid].csv.  
Then delete the country.csv file

TO DO: Update earthscape.js to also display <a href="/data-pipeline/timelines/earthscape/datacommons.html#country=IN,CN,US">countries and states</a>. Eliminate datacommons.html after adding to the current page.

TO DO: The DCID value for the water UN Goal topics is: `dc/g/SDG_6`  
Fix the following so we can update [/feed/view/#feed=water](/feed/view#feed=water) to pull the water nav DCID  

	https://api.datacommons.org/v2/observation?key=AIzaSyCTI4Xz-UW_G2Q2RfknhcfdAnTHq5X5XuI&entity.dcids=dc/g/SDG_6



**UN Goals CoLab Specs**

In the [UN Goals Timelines CoLab](https://colab.research.google.com/drive/1LZC8ot8skRMtD4DnokDjYXH6B73WinYP?usp=sharing) create a function called timelineGeneration that generates the timeline csv files. Pass it a string containing DCID files pulled from our Google Sheet UN Goal tabs.

Pass the earthColab function the column **Scope** as: Country, State, County

Convert from 3 to 2-char country codes.

Send rules in the function's parameters to identify which locations to omit (like which countries lack emissions data).

Pull the valid year range from the Google Sheet row in **StartYear** and **EndYear**


We'll send our .csv output to UN Goal subfolders at [data-commons/docs/data](https://github.com/ModelEarth/data-commons/tree/main/docs/data)

