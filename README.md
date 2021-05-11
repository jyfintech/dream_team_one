# [Ether Trade Flow Analysis]

## Team Members:
* Alexander Portno
* Jay Yu
* Kamil Wojnowski
* Serra Battal

## Project Description
* This program sends an end of day snapshot of the trading activity at the major exchanges over SMS. It monitors the value of Ether exchanged relative to price over a specific timeframe

## Dataset:
* Etherscan and cryptocompare API
* Matplotlib for 3D plot
* Twilio for SMS feed

## Presentation
### What does our program do?
* Analyzes the value of Ether traded relative to the price of Ether through the course of a trading timeframe
* We gathered transaction data by public key using Etherscans API. We also used Cryptocompare's API to receive historical prices for ETH
* Using Matplotlib, we created a 3D plot with time represented on the x-axis, ETH price on the y-axis and ETH value on the z-axis and converted it to a PNG file
* We then used Twilio to distribute the PNG over SMS as a convenient way to review the trading activity at the end of theday

## Notes
* Need to set conditions on the columns to filter out large variance/improve visualizations of the "core" activity