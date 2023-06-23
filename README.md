# Unhandled-exception-charmap-codec
MySQL Workbench Error Unhandled exception: 'charmap' codec byte Ox81 in position 4053: character ma &lt; undefined>



This error occurred when I tried to import a CSV file that I had downloaded from the following Kaggle dataset: [Top 250 Football Transfers from 2000 to 2018](https://www.kaggle.com/datasets/vardan95ghazaryan/top-250-football-transfers-from-2000-to-2018).

Despite trying various solutions, none of them seemed to work for me. Therefore, I found a workaround by converting the problematic CSV file to a JSON file. I used the website [csvjson.com](https://csvjson.com/csv2json) to perform the conversion, but you can use any other tool or method you prefer.

The error was caused by the presence of player names in the dataset written in Latin script, which MySQL Workbench didn't handle well. Examples of affected names include "LuÃ­s Figo" and "HernÃ¡n Crespo." However, during the import process, MySQL replaced these Latin script characters with some other characters.

As a data scientist, I documented this solution in my GitHub account to help others who might encounter a similar issue.

