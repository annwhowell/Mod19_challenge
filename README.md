# Mod19_challenge: Fintech Finder

# Overview
#This app (fintech_finder.py) uses blockchain technology to connect Fintech Developers to customers.
#Customers can choose and pay the Fintech developer with Ethereum cryptocurrency through the app.
#The app uses python and Streamlit to function. Ganache has been leveraged to test the app.


# Files
#The primary app is fintech_finder.py
#It calls several functions from crypto_wallet.py
#a .env file with a mnemonic code is required to run this app
#during development, the mnemonic code and testing blockchain were provided from Ganache 

# Libraries and imports
#Crypto_wallet.py creates the account wallet thru a generate_account function
#It also defines the get_balance function and the send_transaction function

#The Crypto_wallet.py code requires the following imports:
'''
import os
import requests
from dotenv import load_dotenv
load_dotenv()
from bip44 import Wallet
from web3 import Account
from web3 import middleware
from web3.gas_strategies.time_based import medium_gas_price_strategy
'''

#Fintech_finder.py requires the following imports:
'''
import streamlit as st
from dataclasses import dataclass
from typing import Any, List
from web3 import Web3
w3 = Web3(Web3.HTTPProvider('HTTP://127.0.0.1:7545'))
'''


# Output

# Launch
#To launch the web application built on Streamlit, use the terminal to input the command 'streamlit run fintech_finder.py'
#The command will launch the web page in a browser and provide the url
#This example is done a localhost

![<Terminal command to launch and resulting webpage>](<./Images/terminal_commands.png>)

# Webpage
#This image shows the webpage launched on the localhost

![<The launched web page>](<Images/main_page_screenshot.png>)

# Validation of the transaction occurring
#The web page shows that the validation occureed and the transaction went through

![<Validation of the transaction occurring>](</Images/validated_transaction.png>)

# Verification through Ganache
#Ganache provided the mnemonic phrase and the testing environment for the app
#After running the app, the results verifying the transaction are seen on Ganache

#The Ganache main page shows and overview and the mnemonic phrase

![<Ganache Account>](<./Images/ganache_account.png>)

#The transactions page shows the transaction details

![<Ganache Record of Transaction>](<./Images/ganache_transaction.png>)

# Created By
#Ann Howell with support from the Rice FinTech Bootcamp

# License
#MIT
