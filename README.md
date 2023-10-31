# Live-Project
<h3> Introduction</h3>
<p> For this project I was tasked with developing a web application for a hobbiest to store a collection of things as well as relating API and data scraped. When creating this project I wanted a place for manga enthusiast to digitally store their collection, including details, and covers. My Manga was developed with those ideas in mind, as well as data scraping for covers to be utilized by users. Through the connected API, users can find their next manga filtering search results by category and displaying corresponding synopsis.

The initial steps of this project were applying basic CRUD operations to MyManga interface. The user can CREATE a record of a manga adding it to a database with the user panel. Through the collection page the user can READ those details in the form of bootstrap cards. Each card has a button with EDIT and DELETE functionality. Using BeautifulSoup cover images were scraped from Anilist for users to utilize as cover sources. I connected to Kitsu's API giving the user the ability to search for mangas. A dropdown menu with category options specifies results.

<h3>Project Stories</h3>
<ol>
  <li><a href="#crud">CRUD</a></li>
  <li><a href="#ds">Data Scraping</a></li>
  <li><a href="#api">API</a></li>
  <li><a href="#fe">Front End</a></li>
  <li><a href="#as">Additional Skills</a></li>
</ol>
  
<h4 id="crud">Create Record:</h4>
<p>Created a form for user to insert information into database based upon object model. User has the ability to save, save and add another, and cancel returning to home page.</p>
<img src="code_snippets/code1.PNG">

<h4>Read</h4>
<p>To "read" database objects I utlized bootstrap cards. Using a for loop to scan through the db, the relevent data displays on card. Buttons for update and delete functionality. </p>
<img src="code_snippets/code3.PNG">

<h4>Update & Delete</h4>
<p>Update button renders a details page where user can update database object. Pk is used to display the details of the card that called UPDATE or DELETE function. Delete function initiates the confirm delete function ensuring the user doesn't accidentaly delete an object. On successful deletion user is returned to collection page.</p>
<img src="code_snippets/code2.PNG">

<h4 id="ds">Data Scraping</h4>
<p>Using BeautifulSoup to datascrape, I requested anilists webpage and parsed throgh the raw HTML. From the data I pulled objects with attributes class 'image' and created a dictionary with key 'source' containing object URLs. Data is then linked and displayed on HTML page.</p>
<img src="code_snippets/code5.PNG">

<h4 id="api">API</h4>
<p>This function requests the URL for chosen API by selected category. Based upon the paramaters, JSON response is stored in object manga_data.</p>
<img src="code_snippets/code6.PNG">
<p>If there's data it's extracted into manga_list. For each manga (matching paramaters), the corresponding attribute 'synopsis' is also pulled and stored. Error handling if there is no synopsis or manga data. Information is then rendered to linked HTML page.</p>
<img src="code_snippets/code7.PNG">
<p>On the front-end  a drop down menu gives user category options to search API. Results will then be displayed on a list. When clicked, list items corresponding synopsis is displayed.</p>
<img src="code_snippets/code9.PNG">
<p>JavaScript function that displays synopsis once event listener is triggered. Capturing the current scroll position, when synopsis finally loads the page will stay in its current position so user won't have to scroll back down.
<img src="code_snippets/code10.PNG">


<h4 id="fe">Front End</h4>
<p>To add more user functionality I created buttons that would sort collection by title, demographic, and author. User can also use a search form to find a specific title, displaying an individual card.</p>
<img src="code_snippets/code8.PNG">
<p>Index container styled with <a href="css/styling.css">CSS</a> animation.</p>
<img src="code_snippets/code11.PNG">
<p>List and links styled with <a href="css/styling.css">CSS</a> animation.</p>
<img src="code_snippets/code12.PNG">

<h4 id="as">Additional Skills:</h4>
<ul>
  <li>Live Setting: Working alongside other developers and utilizng different applications to communicate and update project. Overall project flow: assigned stories, version control/branching/merging, stand-ups, sprint meetings/review, etc.</li>
  <li>Advanced Coding: Researching and self-teaching new and advanced coding. Exhausting all resources to achieve end goal.</li>
  <li>Debugging: isolating code to determine where issues stem from, testing multiple options to complete the task, communicating with a team to find best solution.</li>
</ul>

<h4 id="challenges">Challenges</h4>
<ul>
<li>Advanced coding conepts such as datascraping and API were unknown to me at the start of this project. There was pressure having to teach myself these concepts in a timely manner for the first time. Utilizing online resources, our communication platform, and other developers/project instructors helped me overcome this challenge.</li>
<li>Developing a web application of this size and complexity was a first for me. Taking the time to map out how I wanted my pages to look and functionality required to accomplish tasks, I was able to break things down into simple steps completeing one at a time returning desired results.</li>
<li>When problem solving I had to find creative solutions and be willing to pivot as needed. Facing roadblocks, I had to find another way to accomplish the same end result and realize my first idea isn't always the best. </li>
</ul>

