<h1>What is Clickjacking?</h1>

Clickjacking, also known as a “UI redress attack” is an interface-based attack in which a user is tricked into clicking on actionable content on a hidden website by clicking on some other content in a decoy website. In simple words, an attacker uses multiple transparent or opaque layers to trick a user into clicking on a button or link on another page when they were intending to click on the top level page. Thus, the attacker is “hijacking” clicks meant for their page and routing them to another page, most likely owned by another application, domain, or both.
Using a similar technique, keystrokes can also be hijacked. With a carefully crafted combination of stylesheets, iframes, and text boxes, a user can be led to believe they are typing in the password to their email or bank account, but are instead typing into an invisible frame controlled by the attacker.

<h1>How Clickjacking Works?</h1>


Clickjacking works by using an iframe to load a vulnerable website on top of an attacker's controlled domain. In the above diagram, you can see there are two web pages let us call them A and B. Website A : A website vulnerable to clickjacking which says that "You won a free iPhone!" so that the victim gets lured by "Claiming the Prize!" Website B: It is an attacker controlled website wherein you have the option to "Pay" This is the exact scenario of how Clickjacking works. Attackers create an attractive website, in our case website A, to lure the victim. Create an iframe and load it in the attacker controlled domain which is website B. In this manner the attacker manages to fool the victim and make him pay while attracting him for a free prize! So this is how Clickjacking attack is performed.
Severity

Clickjacking based vulnerabilities are one of the simple bugs to find and are classified into two types:

    Clickjacking on Non-Sensitive Pages
    Clickjacking on Sensitive Pages

Clickjacking on Non-Sensitive Pages are generally considered as Informational and categorized as P5 vulnerability where-as Clickjacking on Sensitive Pages are categorized as P4. Clickjacking on sensitive pages can also increase the impact of account takeover and hence can sometimes go up to P3 category.

<h1> LABS </h1>
Now we are going to check the lab and see if the lab is vulnerable to Clickjacking or not



<img width="1100" alt="image" src="https://github.com/neostardustdr/hacktify/assets/121484808/d26fa08c-8a2b-468a-b486-9d1ef2291509">

Now when we analyse the networktab in the developer tools option, we can see that there is no Xfame protection enabled; also no xframe-options availble so we can think that this site might be vulnerable to Clickjacking 

<img width="1156" alt="image" src="https://github.com/neostardustdr/hacktify/assets/121484808/cd7a827a-a008-46a6-adfd-e5c7a4c44e49">

Now we will try another method to confirm this.

We have an HTML code that we have developed and save as a HTML file 

<html>
    <head>
        <title>Clickjack test page</title>
    </head>
    <body>
<p> Website is vulnerable to Clickjacking </p/>
        <iframe src="http://labs.hacktify.in/HTML/clickjacking_lab/lab_1/lab_1.php
" width="500" height="500"></iframe>
    </body>
</html>

<p>And once you save the file and open in the browser and here is the result</p> 

<img width="324" alt="image" src="https://github.com/neostardustdr/hacktify/assets/121484808/31054142-4748-4449-9cdb-9783704d9361">


Another way is using https://samy.pl/quickjack/quickjack.html

When we put the target website and click on go we get the below result 


Hide QuickJack Frame (clickjacking only): This feature likely hides the frame used in a clickjacking attack to make it appear as though the user is interacting with the legitimate page while actually interacting with a hidden malicious frame.

Prevent Frame Breakouts (FF only): This feature may prevent the framed content from breaking out of the frame in Firefox (FF), thereby confining it to the intended frame and preventing it from hijacking the entire browser window.

Continue Jacking after First Click: This option likely allows the clickjacking attack to continue even after the user has clicked on something, possibly to further manipulate the user's interactions without their knowledge.

Prevent Clicks (slice only): This feature likely prevents clicks on the sliced portions of a web page, which could be used to prevent users from interacting with specific elements targeted by the clickjacking attack.

Resize 2nd page to 100% (slice only): This option may resize the second page (presumably the one being manipulated) to 100% of the viewport, ensuring that it covers the entire visible area and making it more convincing to the user.

Hide Referrer (requires redirection package): This feature hides the referrer information that the browser sends when navigating from one page to another. This can be used to prevent the attacker from seeing where the traffic is coming from.

Redirect Browser (slice only): This option likely redirects the user's browser to a different page or URL after the clickjacking attack has been executed, possibly to further manipulate the user or to cover up the attack.

Another way is to use https://securityheaders.com we can see that there is no xframe options availble 

<img width="1019" alt="image" src="https://github.com/neostardustdr/hacktify/assets/121484808/6682a7f2-6abd-4f92-ba3c-03213a0583be">



