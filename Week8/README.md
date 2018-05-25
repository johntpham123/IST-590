# Project 8 - Pentesting Live Targets

Time spent: **X** hours spent in total

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
![session hijacking](https://user-images.githubusercontent.com/37943892/40519708-efe57fbe-5f75-11e8-8426-8a7be589cc8d.gif)


Vulnerability #2: SQL Injection. Blind SQL injection slowing the page down
![sql injections](https://user-images.githubusercontent.com/37943892/40519412-3a208f26-5f74-11e8-8005-feaf6bf5d117.gif)


## Green

Vulnerability #1: XSS
![xss](https://user-images.githubusercontent.com/37943892/40519611-45acb8fa-5f75-11e8-86d6-89cb4020a93c.gif)


Vulnerability #2: User Enumeration
![xss](https://user-images.githubusercontent.com/37943892/40516603-342178f0-5f66-11e8-95c7-8845184a0439.gif)




## Red

Vulnerability #1: IDOR
![idor](https://user-images.githubusercontent.com/37943892/40516388-5972b2fa-5f65-11e8-8766-0629fbc6c483.gif)


Vulnerability #2: CSRF
![csrf - red](https://user-images.githubusercontent.com/37943892/40516550-ef706068-5f65-11e8-91a5-ec378717fb26.gif)


## Notes

1) Which attacks were easiest to execute? Which were the most difficult?
The XSS and IDOR were the easiest to execute and the most difficult would be the the SQL injection

2) What is a good rule of thumb which would prevent accidentally username enumeration vulnerabilities like the one created here?
Give the same result for all login activity so the attacker won't know if the username they're using is the correct one.

3) Since you should be somewhat familiar with the CMS and how it was coded, can you think of another resource which could be made vulnerable to an Insecure Direct Object Reference? What code could be removed which would expose it? (Hint: It was also the answer to the first bonus objective to the Weekly Assignment for week 3.)
IDOR can be used to steal sensitive information like addresses, credit card information, and social security numbers. 

4) Many SQL Injections use OR as part of the injected code. (For example: ' OR 1=1 --'.) Could AND work just as well in place of OR? (For example: ' AND 1=1 --'.) Why or why not?
It depends on what kind of information you're trying to get. using an AND statement would mean that would conditions would need to be true for information to be pulled. Using the OR statement gives you more flexibility because it can pull both conditions

5) A stored XSS attack requires patience because it could be stored for months before being triggered. Because of this, what important ingredient would an attacker most likely include in a stored XSS attack script?
They would have to be able to hide their scripts somewhere that would be hard for the admin to find

6) Imagine that one of your classmates is an authorized admin for the site's CMS and you are not. How would you get them to visit the self-submitting, hidden form page you created in Objective #5 (CSRF)?
I would send them a forged html link and they would click on it because it looks the same as the actual link.

7) Compare session hijacking and session fixation. Which attack do you think is easier for an attacker to execute? Why? One of them is much easier to defend against than the other. Which one and why? 
Session hijacking would be easier because you can remote steal their cookies using a remote session. Session fixation is harder because you have to obtain a valid session ID and make the victim use it so you can get access to their session. 
