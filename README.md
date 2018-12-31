# Github Finder

Allows user to search for GitHub profiles and displays them along with 5 last repositories.

You can make the following easy changes to the application to make it custom and unique.
I've spent good hour just playing with the themes and bootstrap classes!

Kindly note that the application will work in demo mode unless you register it.
This is due to restrictions on GitHub API this application is using.
This means that you will be able to do just a couple of searches per hour.
But don't worry! To be able to use it all the time you can obtain id and secret key by registering your version of application.
To do that please complete a registration form here: www.github.com/settings/applications/new .

Once you have obtained id and keys you will need to do the following:

1. Open github.js with your text editor and uncomment lines 4 & 5 removing /* & */
2. Enter your id and secret key like this:

before:
 ``this.client_id = '';
    this.client_secret = ''; ``
after:
 ``this.client_id = 'your.id.goes.here';
    this.client_secret = 'your.key.goes.here'; ``

3.You're nearly done! Modify line 12 and 14 changing the following: 

before:
  ``line 12: https://api.github.com/users/${user}``
  ``line 14: https://api.github.com/users/${user}/repos?per_page=${this.repos_count}&sort=${this.repos_sort}``
after:
  ``https://api.github.com/users/${user}?client_id=${this.client_id}&client_secret=${this.client_secret}``
  ``https://api.github.com/users/${user}/repos?per_page=${this.repos_count}&sort=${this.repos_sort}&client_id=${this.client_id}&client_secret=${this.client_secret}``

You will be able to use it all the time.

Now.Let's have some fun!

You can easily change the theme of the application:

1. Go to www.bootswatch.com and find the theme you like 
2. Click on download
3. Copy the link from the new link
4. Open application's index.html file in text editor
5. Find "https://bootswatch.com/4/cerulean/bootstrap.min.css", replace it and enjoy your new theme!

**Language: native JavaScript (no JQuery)**

**Framework: I've used Bootswatch (Cerulean theme)**


## Getting started

`git clone https://github.com/KrzysztofBalejko/Guess-The-Number.git` or download the application to your desktop.

 Simply open index.html file in your browser

 I recommend using Chrome instead of IE.