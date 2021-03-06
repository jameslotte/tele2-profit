# Tele2 Profit
Console application that allows you to quickly sell your Tele2 data on their **Market**


## Features
* Quick market listing of your Tele2 data
* Bumping up lots that haven't been sold
* Asyncronous queries to _Tele2 API_ allow to perform multiple actions simultaneously


## Demo
![imgur demo gif](https://i.imgur.com/xKTTRDS.gif)


## Installation
#### Steps:
1. Clone repository
2. Setup virtual environment (optional)  
    2.1. Create **venv** with `python -m venv venv`  
    2.2. Activate by running this comand (just paste it after previous and hit enter) `venv\Scripts\activate`
3. Install dependencies with `pip install -r requirements.txt`
4. You are good to go!

#### Command list (Windows):
* `git clone https://github.com/raritetmolodoy/tele2-profit.git`
* `cd tele2-profit`
* `python -m venv venv`
* `venv\Scripts\activate`
* `pip install -r requirements.txt`


## Usage
1. Login with running `python auth.py`. Access token works 4 hours, then it needs to be updated.  
**note: access-token saves on your PC _only_, in `./config.json` file** 
2. Run `python main.py` and select action.

### FYI: Current Tele2 market lot rules

#### Gigabytes
* Minimum GB amount - **1 GB**
* Minimum GB price - **15 rub/GB**, maximum - **50 rub/GB**

#### Minutes
* Minimum minute amount - **50 min**
* Minimum minute price - **0.8 rub/min**, maximum - **2 rub/min**

### Listing lots
**Preparing lots is done with this syntax: `<lot amount> <lot price>`**  
For example: `60 80` - 60 minutes (or gb) will be listed for 80 rub.  

**Standard syntax can be shortened to just `<lot amount>`**   
For example: `68` -  68 minutes (or gb) will be listed with **minimum** possible price *(in this case - 55 rub if minutes, 1020 rub if gb)*.  
When done leave input field empty (just hit enter) and you will jump to the next part.


## TODO
* Use refresh token to support longer auth persistence (currently 4 hours)
