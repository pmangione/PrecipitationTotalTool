# PrecipitationTotalTool
I built a tool to automate the calculation of precipitation totals for a given date range on the CoCoRaHS network. 
There is large nation-wide group of weather spotters called CoCoRaHS.  They collect daily precipitation reports at personal weather stations on their property.  I built an automated tool to sum precipitatin totals from each weather station for a given date range.

A crucial part of this process involved "throwing out" weather stations that were missing at least one daily report.  This was achieved by first counting the number of reports that would be required for a date range.  In this code snippet, the number of required records was determined with the help of PHP's date_diff function.  See the code snippet here. 

The next part of this process was to build an array of weather stations from a multidimensional array that had all of the data.  Then using PHP's array_count_values function, an associative array was built which stored the number of times, or the "count", that each weather station appeared.  Finally, the program looped back through the multidimensional array with all of the data and determined if each weather station had the number of required records.  If it did, a new array was built to store the weather station along with its associated rainfall total.  See the code snippet here. 
