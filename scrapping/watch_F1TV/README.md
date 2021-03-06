# AutoPlayer F1TV

## Context: 
I love Formula 1 and from time to time I like to watch older seasons' compacts and championship summary videos on YouTube. Most of those videos, however, were taken down due to Copyright. The solution for me was to sign up on F1TV, where we can find coverage from even older races (70's and 80's included) in the [archive section](https://f1tv.formula1.com/page/493/archive).

## Problem:
There is no playlist to watch videos on F1TV site, and we need to find the links one by one in order to watch the whole season in sequence. Older youtube videos (some extracted from older VHS tapes and DVDs) present the sequence of the race compacts, so I could lay on bed and watch all the sequence. The web page navigation also went through several improvements recently, but the player is still not good.

## First solution:
After a brief reddit search, I discovered [this website](https://g-hartmann.github.io/F1TVlinks/) that presents a fast way to find the videos I want. From the website, we can copy the link to the clipboard and watch... however the login and password are easily lost during the navigation, so I needed frequently to login again. Also, we needed to open one by one, click on play, then fullscreen... many steps.

## Second solution:
I had a brief knowledge of the Selenium lib (used for interface testing and data scrapping from websites). With the browser interaction commands from Selenium, I started to think about ways to automatize browser navigation in order to open the videos one by one so I can watch the whole season review without getting off bed. This was also a nice way to learn about automatic browser interaction and navigation using the Selenium lib :)

So, my problem was: *could I automatize browser navigation simulating the creation of a F1TV playlist using Python and Selenium?*

With the scope defined, I went for mapping the interaction flow in order to open a video on the site player (including elements and wait times), researched about cookies and session registration for f1tv login, found out how to use info copied on the clipboard by the g-hartmann website and developed a solution able to solve this small problem!

## Third solution:
With changes on navigation of the website, the navigation was made easier (they made lots of enhancements server-side!) but I still haven't got my playlist and my old code did not run anymore. Therefore I modified some aspects of the mapped flow, using links that can give access to season webpages. With this, we can access the videos using only the inner navigation flow. This solution is the current solution on the notebook.

The Jupyter notebook presented in this folder details the prototipation process step by step, given as parameters the year you want to watch and the number of the race you want to start :)

**USAGE**:
*   Configure .env with credentials (login and password for f1TV)
*   Follow the steps described on the cells of the Jupyter-notebook

**REQUIREMENTS**
* Google Chrome
* Selenium==4.1.3
* chromedriver_autoinstaller==0.3.1
* python-dotenv==0.13.0
* undetected-chromedriver==3.1.5post4

## Disclaimer

If you work on F1TV, I am not trying to download any content or to DDOS attack your servers, it is just a fun personal project that made me learn a little bit more about website automation and scrappers. Don't block me please :)