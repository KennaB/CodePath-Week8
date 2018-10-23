# Project 8 - Pentesting Live Targets

Time spent: **6** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: Session Hijacking
  - Using exposed PHP session tools and changing the session id allows for hijacking other users' sessions.

Vulnerability #2: 


## Green

Vulnerability #1: Username Enumeration
  - Validity of attempted login username leaks due to differences in formatting, such as bold typeface for valid usernames.

Vulnerability #2:


## Red

Vulnerability #1: IDOR 
  - Data of "fired" employee and recently hired employee who are unlisted can be indirectly accessed by manipulating the id paramater in the Get request.

Vulnerability #2: 


## Notes



The green website had no filter at all on its contact field, so I made a button that edited the cookie name when clicked. Obviously, this was just for the fun of it (and because it was funny to see the buttons rendered on the admin side), and this "attack" could be much stealthier if the attacker used onload or the like.

'''
<div id="dontClick" style="background-color: lime; margin: auto;">Click Me!</div>
<script>
dontClick.addEventListener('click', () => {
	document.cookie="name=the Internet is scary!";
	dontClick.innerHTML = document.cookie;
});
</script>
'''


