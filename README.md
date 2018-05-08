# Thinkful_1.2.3_Drill
Aggregates &amp; Group By Lesson

## Drills

1. What was the hottest day in our data set? Where was that?

select max(MaxTemperatureF ), date,  zip from weather

```
hottest day (date): 2015-11-17
location (zip): 94063
```

2. How many trips started at each station?

select count(start_station), start_station from trips group by start_station

|TripCount| Station Name                                    | 
|---------|-------------------------------------------------| 
| "7464"  | "2nd at Folsom"                                 | 
| "7722"  | "2nd at South Park"                             | 
| "14099" | "2nd at Townsend"                               | 
| "19"    | "5th S at E. San Salvador St"                   | 
| "1"     | "5th St at E. San Salvador St"                  | 
| "173"   | "5th St at Folsom St"                           | 
| "5436"  | "5th at Howard"                                 | 
| "789"   | "Adobe on Almaden"                              | 
| "547"   | "Arena Green / SAP Center"                      | 
| "7373"  | "Beale at Market"                               | 
| "5695"  | "Broadway St at Battery St"                     | 
| "392"   | "California Ave Caltrain Station"               | 
| "1014"  | "Castro Street and El Camino Real"              | 
| "343"   | "Charleston Park/ North Bayshore Area"          | 
| "5043"  | "Civic Center BART (7th at Market)"             | 
| "4357"  | "Clay at Battery"                               | 
| "4969"  | "Commercial at Montgomery"                      | 
| "788"   | "Cowper at University"                          | 
| "69"    | "Cyril Magnin St at Ellis St"                   | 
| "5240"  | "Davis at Jackson"                              | 
| "7714"  | "Embarcadero at Bryant"                         | 
| "7820"  | "Embarcadero at Folsom"                         | 
| "13424" | "Embarcadero at Sansome"                        | 
| "4710"  | "Embarcadero at Vallejo"                        | 
| "71"    | "Evelyn Park and Ride"                          | 
| "2"     | "Franklin at Maple"                             | 
| "3309"  | "Golden Gate at Polk"                           | 
| "6735"  | "Grant Avenue at Columbus Avenue"               | 
| "16128" | "Harry Bridges Plaza (Ferry Building)"          | 
| "7583"  | "Howard at 2nd"                                 | 
| "945"   | "Japantown"                                     | 
| "147"   | "Kaiser Hospital"                               | 
| "630"   | "MLK Library"                                   | 
| "9937"  | "Market at 10th"                                | 
| "7337"  | "Market at 4th"                                 | 
| "10970" | "Market at Sansome"                             | 
| "5613"  | "Mechanics Plaza (Market at Battery)"           | 
| "119"   | "Mezes"                                         | 
| "7"     | "Mezes Park"                                    | 
| "66"    | "Middlefield Light Rail Station"                | 
| "2515"  | "Mountain View Caltrain Station"                | 
| "1291"  | "Mountain View City Hall"                       | 
| "1170"  | "Palo Alto Caltrain Station"                    | 
| "276"   | "Park at Olive"                                 | 
| "833"   | "Paseo de San Antonio"                          | 
| "4348"  | "Post at Kearny"                                | 
| "6826"  | "Powell Street BART"                            | 
| "4488"  | "Powell at Post (Union Square)"                 | 
| "695"   | "Redwood City Caltrain Station"                 | 
| "5"     | "Redwood City Medical Center"                   | 
| "59"    | "Redwood City Public Library"                   | 
| "42"    | "Rengstorff Avenue / California Street"         | 
| "879"   | "Ryland Park"                                   | 
| "84"    | "S. Market St at Park Ave"                      | 
| "481"   | "SJSU - San Salvador at 9th"                    | 
| "363"   | "SJSU 4th at San Carlos"                        | 
| "611"   | "San Antonio Caltrain Station"                  | 
| "559"   | "San Antonio Shopping Center"                   | 
| "23591" | "San Francisco Caltrain (Townsend at 4th)"      | 
| "22358" | "San Francisco Caltrain 2 (330 Townsend)"       | 
| "2195"  | "San Francisco City Hall"                       | 
| "518"   | "San Jose City Hall"                            | 
| "543"   | "San Jose Civic Center"                         | 
| "4035"  | "San Jose Diridon Caltrain Station"             | 
| "86"    | "San Mateo County Center"                       | 
| "1215"  | "San Pedro Square"                              | 
| "540"   | "San Salvador at 1st"                           | 
| "420"   | "Santa Clara County Civic Center"               | 
| "1447"  | "Santa Clara at Almaden"                        | 
| "15"    | "Sequoia Hospital"                              | 
| "5398"  | "South Van Ness at Market"                      | 
| "5113"  | "Spear at Folsom"                               | 
| "694"   | "St James Park"                                 | 
| "428"   | "Stanford in Redwood City"                      | 
| "13693" | "Steuart at Market"                             | 
| "13111" | "Temporary Transbay Terminal (Howard at Beale)" | 
| "11170" | "Townsend at 7th"                               | 
| "490"   | "University and Emerson"                        | 
| "2844"  | "Washington at Kearny"                          | 
| "3460"  | "Yerba Buena Center of the Arts (3rd @ Howard)" | 

3. What's the shortest trip that happened?

```
select min(duration) from trips 

result: 60
```

4. What is the average trip duration, by end station?

select avg(duration), end_station from trips group by end_station

| Avg Trip Duration  | End Station Name                                | 
|--------------------|-------------------------------------------------| 
| "557.050760233918" | "2nd at Folsom"                                 | 
| "531.589903573454" | "2nd at South Park"                             | 
| "633.257044057377" | "2nd at Townsend"                               | 
| "1767.0"           | "5th S at E. San Salvador St"                   | 
| "686.0"            | "5th St at E. San Salvador St"                  | 
| "527.298013245033" | "5th St at Folsom St"                           | 
| "583.572311104071" | "5th at Howard"                                 | 
| "828.990789473684" | "Adobe on Almaden"                              | 
| "1426.47592592593" | "Arena Green / SAP Center"                      | 
| "699.791838134431" | "Beale at Market"                               | 
| "756.494616846105" | "Broadway St at Battery St"                     | 
| "1825.5910543131"  | "California Ave Caltrain Station"               | 
| "802.502173913044" | "Castro Street and El Camino Real"              | 
| "2370.22615803815" | "Charleston Park/ North Bayshore Area"          | 
| "1033.10343347639" | "Civic Center BART (7th at Market)"             | 
| "856.799765258216" | "Clay at Battery"                               | 
| "564.716529250098" | "Commercial at Montgomery"                      | 
| "1210.07079646018" | "Cowper at University"                          | 
| "2926.22058823529" | "Cyril Magnin St at Ellis St"                   | 
| "735.510463121784" | "Davis at Jackson"                              | 
| "697.743581616482" | "Embarcadero at Bryant"                         | 
| "613.881648422408" | "Embarcadero at Folsom"                         | 
| "1400.38250762937" | "Embarcadero at Sansome"                        | 
| "1372.67024684379" | "Embarcadero at Vallejo"                        | 
| "739.013157894737" | "Evelyn Park and Ride"                          | 
| "2068.6"           | "Franklin at Maple"                             | 
| "1277.80007601672" | "Golden Gate at Polk"                           | 
| "1478.68141836174" | "Grant Avenue at Columbus Avenue"               | 
| "918.877354048964" | "Harry Bridges Plaza (Ferry Building)"          | 
| "592.663818038391" | "Howard at 2nd"                                 | 
| "969.828918322296" | "Japantown"                                     | 
| "670.296296296296" | "Kaiser Hospital"                               | 
| "1012.9728"        | "MLK Library"                                   | 
| "1044.92866020383" | "Market at 10th"                                | 
| "1022.00102234555" | "Market at 4th"                                 | 
| "612.926951946142" | "Market at Sansome"                             | 
| "731.368790591539" | "Mechanics Plaza (Market at Battery)"           | 
| "644.850877192982" | "Mezes"                                         | 
| "257.0"            | "Mezes Park"                                    | 
| "1199.87096774194" | "Middlefield Light Rail Station"                | 
| "996.882961783439" | "Mountain View Caltrain Station"                | 
| "651.160204828091" | "Mountain View City Hall"                       | 
| "1927.44844357977" | "Palo Alto Caltrain Station"                    | 
| "1405.99264705882" | "Park at Olive"                                 | 
| "724.440170940171" | "Paseo de San Antonio"                          | 
| "744.221122112211" | "Post at Kearny"                                | 
| "991.009053738318" | "Powell Street BART"                            | 
| "1631.98155673648" | "Powell at Post (Union Square)"                 | 
| "1147.66666666667" | "Redwood City Caltrain Station"                 | 
| "359.083333333333" | "Redwood City Medical Center"                   | 
| "1186.70149253731" | "Redwood City Public Library"                   | 
| "1658.5"           | "Rengstorff Avenue / California Street"         | 
| "1223.40402969247" | "Ryland Park"                                   | 
| "1585.74757281553" | "S. Market St at Park Ave"                      | 
| "1227.61968680089" | "SJSU - San Salvador at 9th"                    | 
| "967.132432432432" | "SJSU 4th at San Carlos"                        | 
| "1083.68190127971" | "San Antonio Caltrain Station"                  | 
| "724.399671052632" | "San Antonio Shopping Center"                   | 
| "723.110629443385" | "San Francisco Caltrain (Townsend at 4th)"      | 
| "609.492032547889" | "San Francisco Caltrain 2 (330 Townsend)"       | 
| "1361.31942215088" | "San Francisco City Hall"                       | 
| "1147.76053215078" | "San Jose City Hall"                            | 
| "2372.58423493045" | "San Jose Civic Center"                         | 
| "599.522307692308" | "San Jose Diridon Caltrain Station"             | 
| "1008.02884615385" | "San Mateo County Center"                       | 
| "816.377488514548" | "San Pedro Square"                              | 
| "1084.99333333333" | "San Salvador at 1st"                           | 
| "1604.77399380805" | "Santa Clara County Civic Center"               | 
| "726.675843083276" | "Santa Clara at Almaden"                        | 
| "1633.5"           | "Sequoia Hospital"                              | 
| "1366.03096774194" | "South Van Ness at Market"                      | 
| "608.985535197686" | "Spear at Folsom"                               | 
| "578.417298937784" | "St James Park"                                 | 
| "1071.65904365904" | "Stanford in Redwood City"                      | 
| "668.527482330337" | "Steuart at Market"                             | 
| "582.835282729693" | "Temporary Transbay Terminal (Howard at Beale)" | 
| "666.20582801478"  | "Townsend at 7th"                               | 
| "4710.89772727273" | "University and Emerson"                        | 
| "1061.88506107109" | "Washington at Kearny"                          | 
| "757.095514112903" | "Yerba Buena Center of the Arts (3rd @ Howard)" | 


