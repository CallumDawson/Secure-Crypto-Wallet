# Secure Crypto Wallet ("Project Kratos")
A hot wallet with more security than modern-day banks.

**NOTE:** This project is a work-in-progress and the Python script is being developed.

## Purpose
Using this method you can make use of a "hot wallet" (a wallet that performs transactions over the internet) while at the same time knowing that it's as secure as a cold wallet.

## Requirements
* LAN server (such as a Raspberry Pi)
* 3 x OTP apps across geographically diverse stakeholders

## Setup
1. Setup an offline multisig (2-of-3) wallet
2. Setup a LAN server which runs barebones Linux with no ports forwarded to the internet - it should be powered off while not in use
3. Setup a Python script on the LAN server that can securely encrypt 3 OTP secrets into the private keys
4. Setup 3 OTP apps, each with a different secret

## Process
1. Power on the LAN server ready to use
2. Invoke the Python script and setup the transaction ("BUY BTC", "BUY USDT", "TRANSFER", etc.)
3. Phone a stakeholder to get their OTP code
4. Input 2 OTP codes into the Python script which will compute the private address without storing it and perform the transaction

## Security Benefits
* Hackers can only intercept OTP codes which are useless, especially after the 30 seconds expire
* If the LAN server is stolen, it doesn't store any information - hackers would need the OTP codes
* A single OTP authenticator is useless if the phone is stolen and hacked into
