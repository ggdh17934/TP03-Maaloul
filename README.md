The [TP03 Power BI report](https://github.com/ggdh17934/TP03-Maaloul/releases/tag/v1.0.0) imports the same TP02 HIGGS CSV; inspection confirmed 11,000,000 rows, 29 numeric columns and no missing values ([import screenshot](imported_table.png)).  
Power Query removes 278,698 exact duplicate rows, leaving 10,721,302 records, renames the original columns and adds event-class and lepton-pT-bin fields.  
Basic DAX measures calculate the event count and the mean lepton pT, missing energy and m_wwbb values.  
The [final dashboard](dashboard.png) contains the five required visuals: one KPI card, two bar charts, one column chart and one line chart, plus two slicers.  
Both slicers were tested: selecting Signal gives 5,829,123 events, while limiting the lepton pT bin to 1.00 gives 8,113,169; the charts and KPI update together, and the saved PBIX was reopened successfully.  
Signal accounts for 5,829,123 events (54.37%), compared with 4,892,179 background events (45.63%) after cleaning.  
Mean lepton pT is 0.966 for signal versus 1.021 for background, and mean missing energy is 0.942 versus 1.062, in dataset units.  
In the 4+ lepton pT bin, mean m_wwbb is 1.390 for signal and 1.726 for background, showing a separation between the two classes in this part of the data.  
