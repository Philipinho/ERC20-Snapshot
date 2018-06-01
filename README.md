# ERC20-Snapshot
ERC20 Token Holders Snapshot Tool

I wanted to do a token swap for my project but i was unable to find any open source tool to make a snapshot of the token holders and their balance so i decided to make one. 
This tool works with ethplorer.io and you do not need an API key.

# How to use 
Set the ```$tokenAddress``` parameter to the contract address. 
Set the ```$numpage``` parameter to the total number of pages containing the token holders. 
To know the number of pages of token holders, goto:
https://ethplorer.io/address/TOKENADDRESS#tab=tab-holders

The output data will be displayed in a table.


You can use curl or wget to download the pages locally before parsing the data. 

I'm not yet good at documenting so if you find any error, please create an issue or a pull request.
Thank you. 
