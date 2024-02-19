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

