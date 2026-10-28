# Submitted report — text edition

Extracted from the original Semester 2 report. Cover sheets, student identifiers and empty image positions are omitted. Original narrative, spelling and values are retained. Embedded dashboards are available in `assets/`. This historical analysis does not establish causation.

Introduction
ASEAN is a list of 11 countries (Brunei, Cambodia, Indonesia, Laos, Malaysia, Myanmar, Philippines, Singapore, Thailand, Vietnam & Timor) is a political and economic association of the southeast region. It is one of the fastest growing regions from one of the world’s poorest regions in 1970s to the 5th largest economy with a GDP of around $4 trillion dollars due to its strategic geopolitical position and a very young and active population of over 600 million.

Due to its fast growth, the momentum opens doors to the vulnerability of the effects of climate change. Rising temperatures, extreme weather events, and environmental degradation pose significant threats to urban systems, economic activities, and natural ecosystems. By 2050, it is estimated that over 35% of ASEAN GDP will be exposed to the risks of losses caused by climate change.

In this assignment, I will explore environment sustainability issues across the region, using data-driven proposals that positively contribute to achieving the United Nations – Sustainable Development Goals (UN-SDGs) 11, 12, 13, 14 & 15 comparing Singapore with the rest of ASEAN.

Project Objectives

To provide a structured analysis, the SDGs are consolidated into three overarching themes: Urban Infrastructure, Economic Sustainability, and Environmental Impact. These themes allow for a focused examination of how urban development, consumption patterns, and environmental pressures interact within rapidly developing ASEAN economies, and how Singapore’s performance compares with regional trends. I will be focusing more on energy transition and its environmental consequences, with a main focus on SDG 13 (Climate Action).

Based on the topics, the potential questions that were identified included the following:

Theme 1: Energy Use & Transition (SDG 13)
How has electricity consumption per capita changed over time among ASEAN countries, and how does Singapore compare with regional trends?
To what extent are ASEAN countries adopting renewable energy, and how does Singapore’s renewable energy share compare?
Does increasing electricity demand outpace the growth of renewable energy in ASEAN?
How does the electricity generation mix reflect continued dependence on fossil fuels?

Theme 2: Carbon Emissions (SDG 13)
How have CO₂ emissions per capita changed over time among ASEAN countries, and how does Singapore’s trend compare with the region?
Do higher-income ASEAN countries tend to have higher CO₂ emissions per capita?
How does Singapore’s reduction in CO₂ emissions relate to changes in energy efficiency and fuel sources?
Are countries with rising energy use also experiencing increasing carbon emissions?

Theme 3: Environmental Impact (SDG 12, 13 & 15)
How have environmental indicators such as forest coverage, surface temperature change, and waste composition evolved across ASEAN?
Do rising emissions and energy consumption correspond with increasing environmental pressures?
How does Singapore’s environmental impact profile compare with other ASEAN countries?
What patterns suggest growing environmental stress in the region over time?

Data Preparation

The raw datasets were not fully ready. Most indicators had consistent country and year coverage, several datasets contained missing values, especially in recent years due to reporting lag. Column names, formats, and units also varied across sources, requiring standardisation before comparison could be made. Overall, a moderate amount of data cleaning was needed.
Data preparation was carried out using Power Query and the Power BI data model. Countries were filtered to include Singapore and selected ASEAN countries with sufficient data coverage to ensure fair comparisons. Column names were standardised, and data types were corrected Unnecessary data columns were removed, and several datasets were reshaped using unpivoting to convert wide tables into a consistent Country–Year–Value structure. Similar datasets were combined together to make the analysis easier and to avoid repeating the same type of information, the raw datasets for this merged queries where hidden. Finally,were created using shared keys such as Country and Year to enable cross-indicator analysis across dashboards.

Firstly Before doing anything I renamed the Datatsets ive collected to clean readable formats


CO2 Emission Per Capita,GDP Per Capita,Population, Share of Renewable Energey, Electricty Generated Per Capita, Land Covered by Forest datasets where all taken from same website data sources so cleaning was similar and easy. Firstly I rpomoted First Line to headers and renamed columns for better readability. Also changed Some Data Types like GDP to fixed decimal type.


Later I merged similar queries that are used for specific dashboared together. Didn’t merge all the datas I have only ones that had similar structure. Merged Population, GDP Per Capita & CO2 Emissions Per Capita  CO2 Dashboared 2 and Ahare of Renewable Energey & Electricity Generated  Dashboared 1 Energy. After Merging, the orfinal Datasets where hidden from laoding so as not to Clutter PowerbI during Vizualisation Phase after Loading.


For the Asean Electricity Mix by Source which I used For Dashboared 1, I firstly Promoted to header. There was many unwanted data in this dataset so I had to remove many columns.Later I renamed some columns for better readability.


For Surface Temperature Change which I used in Dashboared 3, I first Promoted First Line to header.This Dataset conatined all Countries so I Filtered rows to just the Asean Countries.I removed some unwated columns to unclutetr and renamed some of the remaining.Years was pivoted and each column was a year so I unpivoted the years columns. The years stretched form way back to 1970s so I had to filter to more recent years.Changed the name for the year column.


For the Land Covered by Forest Dataset which I used in Dashbaored 3, was similar to the ones from step 1 as same website was used to collect the data so similar steps where applied. Reason I was not ables to combine it With other Dashboared 3 datasets was cause it was either no time series or some data was unavailable.


7.For the waste dataset I used in Dashboared 3, I firstly promoted first line to headers.Then filtered countries to asean since it was showing all countries.I removed unwanted columns and only kept the composition of waste for each material coulms.I then unpivoted these columns so that compositon of waste for each material all appeared in 1 column.Then for that column, I cahnged the values, for example "composition_glass_percent” to “Glass” for better readability.


8.For Data Modal, I created the Country Dimension and Year Dimension Myself and connected the erst of the datas to it so I can make interactive slicers.Waste Dataset only connected to country cause its only 1 year snapshot and  Asean Electricty mix is connected to nothing is 1 year snapshot and whole of Asean.


9.Created Dax measures with the Help of ChatGPT for average of asean and Singapore which changes with slicer movemnt.


Exploratory Data Analysis
UNIVARIATE ANALYSIS
Line Chart – CO₂ Emissions Over Time (ASEAN Average or All Countries)
Insight:This shows that emissions are rising in developing ASEAN countries as they industrialise, while Singapore’s stabilisation suggests a shift towards more efficient or cleaner energy use.

Line Chart – Electricity Generation Per Capita Over Time
Insight:Energy production is increasing across the region, reflecting growing economic activity and higher electricity demand in ASEAN economies.

Line Chart – Renewable Energy Share Over Time

Insight:Although renewable energy is increasing, it remains a small part of the energy mix, indicating ASEAN’s energy transition is progressing slowly.

Bar Chart – Latest Year CO₂ Per Capita by Country
Insight:Large differences in emissions per capita suggest unequal levels of industrialisation, energy consumption, and dependence on fossil fuels across ASEAN.





Bar Chart – Latest Year Renewable % by Country

Insight:Renewable adoption is uneven, showing that while some countries are advancing, o Singapore face land size limits.




Mulivariate Analysis
Scatter Plot – GDP per Capita vs CO₂ per Capita

Insight:Economic growth in ASEAN is still strongly linked to higher carbon emissions per person, indicating that many countries are developing using carbon-intensive energy sources.

Scatter Plot – Renewable Energy Share vs CO₂ Emissions
.Insight: Countries relying more on renewables tend to have lower carbon intensity, but economic structure and energy demand also influence emissions levels.

Dual Axis Chart – Electricity Generation vs CO₂

Insight:Although more electricity is being produced per person, emissions are not increasing at the same rate, indicating possible improvements in energy efficiency or gradual shifts toward cleaner energy sources.

Conclusion
Line charts showed that electricity generation per capita increased steadily for most countries from 1998 to 2023, reflecting rising energy demand alongside economic growth. Although renewable energy share also increased over time, the overall percentages remain relatively low for most countries, indicating that fossil fuels still dominate the energy mix. Trends in CO₂ emissions per capita varied: developing economies such as Vietnam and Indonesia displayed rising emissions, while Singapore showed a gradual long-term decline despite continued energy use.

To examine relationships between variables, scatter plots were used to compare GDP per capita and CO₂ emissions. A general positive relationship was observed, where higher-income countries produced more emissions per person. However, Singapore stands out as an outlier, with high GDP but declining emissions, suggesting improvements in efficiency or cleaner energy use. Further analysis comparing renewable energy share and CO₂ emissions suggests that countries with higher renewable adoption tend to have relatively lower or slower emissions, although the transition away from fossil fuels remains uneven across the region.




Visualisations
Line Chart – Electricity Generation Per Capita Trend

Electricity generation per capita increased steadily across all selected ASEAN countries from 2000 to 2023.
Singapore and Malaysia consistently recorded the highest electricity generation per person, reflecting their more developed and high energy economies.
Developing countries such as Vietnam, Thailand and Indonesia showed gradual increases, indicating rising energy demand as their economies grow.
Insight:Energy demand across ASEAN is growing alongside economic development, suggesting increasing pressure on the region’s energy systems.

 Line Chart – Renewable Energy Share (% of Total Energy Use)

Renewable energy share increased over time in most ASEAN countries, though growth rates differ.
Vietnam and Thailand showed more noticeable increases in renewable adoption in recent years.
Malaysia and Indonesia displayed moderate growth, while Singapore’s renewable share remained extremely low throughout the period even though it somewhat doubled.
Insight:Although renewable energy adoption is improving, the overall share of renewables remains relatively small in most ASEAN countries, indicating that the energy transition is still in early stages.

 Stacked Area Chart – Electricity Generation Mix Over Time

Fossil fuels continue to dominate the electricity mix in ASEAN.
Coal’s share has generally increased over time, particularly in developing economies.
Renewable sources such as hydro, solar, and wind are growing but still make up a smaller proportion compared to fossil fuels.
Insight:Despite growth in renewables, ASEAN’s electricity system remains heavily dependent on fossil fuels, which slows the region’s progress in reducing carbon emissions.

 KPI Card – Singapore Renewable Energy Percentage (Latest Year)

Singapore’s renewable energy share in the latest year is below 1%, significantly lower than other ASEAN countries.
This reflects Singapore’s land and natural resource constraints, which limit large-scale renewable deployment such as hydro or wind.
Insight:Singapore faces limitations in renewable energy expansion and may need to rely more on regional energy cooperation and clean energy imports to hekp with its transition.

 Line Chart – CO₂ Emissions Per Capita Trend

CO₂ emissions per capita show different patterns across ASEAN countries over time.
Vietnam, Indonesia, and Malaysia display an overall upward trend, indicating increasing emissions as industrial and economic activity increase.
Singapore shows a gradual decline in emissions per capita suggesting improvements in carbon efficiency and cleaner energy use.
Thailand and the Philippines show moderate growth, remaining below Singapore and Malaysia in per capita emissions.
Insight:While many ASEAN countries are experiencing rising emissions due to development, Singapore stands out for managing to reduce emissions intensity over time.

KPI Card – Singapore CO₂ Per Capita Change

Singapore’s CO₂ emissions per capita decreased by 27% from 1998-2023.
Insight:This highlights Singapore’s relative success in decoupling economic growth from carbon emissions compared to regional peers.

Bar Chart – Average Annual CO₂ Emissions Growth Rate by Country

Vietnam shows the highest average annual growth rate in emissions, followed by Indonesia.
Malaysia and the Philippines record moderate growth rates.
Thailand shows slower growth.
Singapore is the only country with a negative growth rate, indicating a consistent decline in emissions per capita.
Insight:Rapidly developing economies are experiencing faster emissions growth, while Singapore’s negative growth rate suggests more advanced energy efficiency and emissions management.

Scatter Plot – GDP per Capita vs CO₂ Emissions per Capita (Latest Year)

A general positive relationship is observed: countries with higher GDP per capita tend to have higher CO₂ emissions per person.
Malaysia and Singapore are positioned toward higher income and higher emissions compared to lower-income ASEAN countries.
However, Singapore’s emissions level is not as high as might be expected for its income level, placing it below the trend of some peers.
Insight:Economic development is linked to higher emissions in ASEAN, but Singapore demonstrates that higher income does not necessarily mean proportionally higher carbon emissions.
 Line Chart – % of Land Covered by Forest Over Time

Forest area trends differ across ASEAN countries.
Malaysia and Indonesia maintain relatively high forest coverage, though both show slight long-term declines.
Vietnam shows a gradual increase in forest cover, indicating reforestation or conservation efforts.
Thailand and the Philippines remain at moderate levels with small fluctuations.
Singapore maintains a stable forest proportion, though its total land area is small.
Insight:While some countries are improving forest management, overall forest coverage in the region is under pressure shwoing small recent declines.

Donut Chart – Forest Area Share by Country (Latest Year)

Malaysia and Indonesia hold the largest shares of forest-covered land among the selected countries.
Singapore has the smallest share due to its limited land area and high urban density.
Insight:Forest resources are unevenly distributed across ASEAN which suggest that they bear greater responsibility for overall sustainability and climate change.

KPI Card – ASEAN Average Temperature Increase

1998-2023 shows an average temperature increase of +0.20°C across ASEAN.
Insight:Even a small regional temperature rise is significant, confirming that ASEAN is experiencing measurable warming due to climate change.

Line Chart – Surface Temperature Change Over Time

Surface temperatures show an overall upward trend across all ASEAN countries.
Temperature spikes become more noticeable in recent years.
Long term direction is increasing.
Insight:Rising temperatures align with increasing emissions shwoing  growing climate risks for ASEAN countries.

Stacked Bar Chart – Waste Composition by Country

Organic and food waste form a large proportion of total waste in most ASEAN countries.
Singapore shows a higher share of recyclable materials such as plastics, paper, and metals showing types of consumption.
Insight:Waste composition differs clearly between countries shwoing difference in consumption needs
Dashboard
Dashboard 1: CO₂ Emissions & Economy
Shows how emissions changed over time and how they relate to economic growth.Most ASEAN countries have rising CO₂ per capita, while Singapore shows a gradual decline. Higher GDP generally links to higher emissions, but Singapore is an exception.


Dashboard 2: Energy Use & Transition
Shows rising electricity generation across all countries, meaning energy demand is increasing. Renewable energy is growing but still forms a small share, with fossil fuels dominating the mix. Singapore has the lowest renewable share due to land limits.



Dashboard 3: Environmental Impact
Shows increasing temperatures across ASEAN, confirming climate change effects. Forest coverage is under pressure in some countries, and waste patterns show growing environmental strain.



Recommendation Summary
According to my analysis.ASEAN countries need to shift toward cleaner energy to manage rising election .Expanding solar,wind and rgeional renwable energy trade can help reduce fossil duel usgae while being able to meet the growing electricity need.

For land constrained Singapore, solar Pannels or green spaces can be installed ontop of buildings and they can also import renwable energy or make investments in renwable energy sources from other countries which may be more pratical that relying on domestic renwables.They could also install offshore windmills thatdo not take up space like china.

Better Enironmental management is also recommended. Protecting forest areas, reforestation, imrpoving recycling ssytems, reducing waste can all help reduce environmental pressure.

Togetehr ASEAN can transition toward a more sustainable development pathway.


Conclusion
I have analysed energy use, carbon emissions and environmental impacts across selected ASEAN Countries for this assignment.The anlysis showed that electricity generation per capita has incerased a lot reflecting growth in economy and risinge nergy demand.Although renwable soruces of energy are incerasing fossil fuel still dominates most of the energy mix.

CO2 Emissions trends change from country to country with developing countries economies such as Vietnam and Indonesia shwoing rise in emissions while stable economies like Singapore show that emissions can stabilise or decline despite high enegy use.Increasing temeprature and pressure on land resoruces confirm that climate change impacts and very visible in the region.

Overall, the findings show ASEAN;s sustainability future depends on how effectively the region can change to cleaner forms of energy while managing environmental pressures linked to economic growth.

Citation References
Data Sources
Our World in Data. (n.d.). Global sustainability and climate-related datasets. Retrieved from https://ourworldindata.org/
Ember. (n.d.). Electricity Data Explorer. Retrieved from https://ember-energy.org/data/electricity-data-explorer/
World Bank. (n.d.). World Wide Governance Indicators Dataset (Data360). Retrieved from https://data360.worldbank.org/en/dataset/WB_WWGD
International Monetary Fund. (n.d.). Climate Change Indicators Dashboard. Retrieved from https://climatedata.imf.org/datasets/4063314923d74187be9596f10d034914_0/about

Background Information Sources
Ernst & Young. (2022). ASEAN sustainability: Challenges and opportunities. EY. Retrieved from https://www.ey.com/en_jp/insights/sustainability/asean-sustainability
YouTube. (2022). Why climate change matters for ASEAN. [Video]. Retrieved from https://www.youtube.com/watch?v=JLSBUgPbZog
YouTube. (2021). Explaining climate action and sustainable development. [Video]. Retrieved from https://www.youtube.com/watch?v=JjJEmeSPssU
