# ERC20-Snapshot
ERC20 Token Holders Snapshot Tool

I wanted to do a token swap for my project but i was unable to find any open source tool to make a snapshot of the token holders and their balance so i decided to make one. 
This tool works with ethplorer.io and you do not need an API key.

Ethplorer stores contract details in a json file. 
To find out the json file containing recent transfers and token holders of a particular token, goto:
https://ethplorer.io/service/service.php?data=TOKENADDRESS

Each page contains 10 rows. 
To know the number of pages of token holders, goto:
https://ethplorer.io/address/TOKENADDRESS#tab=tab-holders

I used for loop to start from the first page to the total page. 
I.e ```for($i = 1;$i <= 5;$i++)```
Then I used the for loop to iterate over the pages.
```https://ethplorer.io/service/service.php?data=TOKENADDRESS&page=tab%3Dtab-holders%26holders%3D".$i```
So it goes this way;
```https://ethplorer.io/service/service.php?data=TOKENADDRESS&page=tab%3Dtab-holders%26holders%3D1
https://ethplorer.io/service/service.php?data=TOKENADDRESS&page=tab%3Dtab-holders%26holders%3D2
https://ethplorer.io/service/service.php?data=TOKENADDRESS&page=tab%3Dtab-holders%26holders%3D3
```
Until it reaches ```$i <=5;```.

The output data will be displayed in a table. 

You can use curl or wget to download the pages locally before a parsing the data. 

I'm not yet good at documenting so if you find any error, please create an issue or a pull request.
Thank you. 
