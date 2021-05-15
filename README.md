# Ether Trade Flow Analysis

## Team Members:
* Alexander Portno
* Jay Yu
* Kamil Wojnowski
* Serra Battal

## Project Description
* This program receives a list of transactions for a specified public key, generates a 3D plot of the trading activity, and then sends the visual over SMS

## References:
* Etherscan and cryptocompare API
* Matplotlib for 3D plot
* Twilio for SMS feed

## Presentation
### What is the API request?
* We pull time of transaction, spot price and quantity of Ether using Etherscan and cryptocompare APIs
* After pulling the financial data, we then convert the JSON file into a Pandas dataframe and save it as a .CSV file
* This allows us to easily pass the datapoints into the Axes3D scatter plot method

### How is the 3D plot generated?
* Using Axes3D scatter plot function, we pass "time" into the x-axis, "quantity of Ether" into the y-axis and "spot price" into the z-axis
* Lighter shades of each dot represent higher spot price, while the darker shades represent lower spot price
* The plot is then converted into a .PNG file in order to send the visual over SMS

### How is Twilio's API being used?
* The .PNG file is uploaded to a server so it can be referenced as a URL
* Next, we send the .PNG file to a specified phone number using Twilio's REST API
