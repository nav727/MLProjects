# Steam web scraping

Task is to scrape the details of top 5 “New & Trending” Game details from [Steam page](https://store.steampowered.com/games/).
-	Understand how webscraping is done.



For every game in top 5 "New and Trending" games get:
- number of positive reviews
- name of developers
- publisher of the game
- system requirements
- 10 reviews for each game

### Challenges faced

On scraping the site using beautiful soup, many of the div tags were not found even though they could be seen via Chrome developer tools panel. Reason for the issue was steam being dynamically loaded website (uses javascript embedded in the HTML) would only render after the browser would run the scripts. 

So to solve this particular problem, I used requests-html library in python which would return the rendered HTML page. This could furthur be fed to beautiful soup for scraping purposes.
