# WorkAggregation
Internet industry recruitment information aggregation system based on data technology. This system uses Python as the core and relies on web display. All functions can be completed on the web page. Crawlers, analysis, visualization, and interaction are independent modules and can be interoperated. Specifically implemented based on python's rich libraries.
Crawlers: Requests
Analysis: lxml, beautifulsoup4
Data analysis: numpy, pandas
Visualization: pyecharts
Backend: Flask
Storage: csv, MySQL
In order to expand functions, I wrote timers and WeChat push, and in order to adapt to teamwork, I wrote function registers and parameter iterators. The crawler data comes from 51job.com, Qilu Talent Network, Liepin.com, Lagou.com and other websites, and the required basic data is all available.

## ToDo 
- Missing crawler supplement
- Improve UI when crawling

## Environment
- Windows \ Linux 
- Python 3.6 : **numpy , pandas , Requests , pyecharts , lxml , PyMySQL**
- MySQL 8.0.11  
- Chrome

## Install
1. Run install_package.bat (try with administrator rights when error occurs)
2. Modify the mysql configuration located in /analysis/analysis_main.py
The system itself has a visual configuration file, that is, you do not need to import data for analysis. If you want to re-analyze, you need to import database data and modify the input_data.py content according to the database fields.
3. Unzip js.7z and place it in the /static directory
4. Run server.py to run the web server
5. Use Chrome to access http://127.0.0.1

## Architecture
The general structure of the system is as follows. The spider directory stores crawler code, the analysis directory is responsible for importing, analyzing, rendering charts, and interacting with other functions. The data directory stores original data, and the conf directory stores charts and mysql configuration files. The import processing and analysis entrance is uniformly controlled by analysis_main and called by the server. Other functions are directly called by the server. All functions can be started on the home page.


