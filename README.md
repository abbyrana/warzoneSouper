# Webscraping Call of Duty: Warzone weapon data
Google Collab Notebook Link:

<br>
<br>

# What I did?

*   Extracted data of 1500+ weapon attachments in Call of Duty Warzone from [GAme8](https://game8.co/games/Modern-Warfare-3/archives/431902) via web scraping using [BeautifulSoup4](https://beautiful-soup-4.readthedocs.io/en/latest/) python library.
*   Extracted list of all compatible weapons for all 1500+ attachments in a very small amount of time by applying the concept of [Multithreading](https://docs.python.org/3/library/threading.html).
*   Built an app on Google [AppSheet](https://about.appsheet.com/home/) which  manages attachment inventory and ranks the best guns which unlock the most best attachments.
*   Created database on Google Sheets which is used by the app.

<br>
<br>

# Challenges
*   Getting a specific html tag using one css selector accross diffrent pages due to inconsistent ordering of tag elements.<br>
FIX: Use find() method to search a specific string to get the desired tag.

* Dealinjg with None type errors due to absence of desired data on the webpage.
FIX: Use if statement to skip the None type values.

*   Trying not to make too many requests.<br>
FIX: Write and test code in a block that is separeted from the request calls on Google .

*   Getting a specific column value of a key from the a diffrent table in Google Sheets.<br>
FIX: Use lookup() or vlookup() function.

*   Coming up with a ranking system that ranks and groups weapons from highest amount of attachment unlock to least and from lowest level to highest level requirement.<br>
FIX: Make a column that appends sum of all attachment's points that the weapon unlocks, weapon name and 100 minus the level requirment. Sort the table by this column in decending  order.

<br>
