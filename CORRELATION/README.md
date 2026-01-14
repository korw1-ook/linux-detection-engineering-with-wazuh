
##🔥 My Wazuh SSH Detection Rules 

I made some custom rules in Wazuh to catch real attacks on SSH, not just random password fails.
----


##🚨 What my rules detect
#1️⃣ Slow brute force

Same IP failing many times slowly

20 fails in 1 hour

From same IP

Good for bots trying to avoid detection

SID: 120010

#2️⃣ Success after brute force

This is the breach moment

First fails happen

Then same IP logs in successfully

Means password guessed or stolen

SID: 120012

#3️⃣ Sudo after login

If attacker gets in, they try to escalate

SSH login happens

Then sudo command within 15 minutes

Possible hacker trying root

SID: 120013

#4️⃣ Password spray

Same IP trying multiple usernames

5 different usernames

Within 10 minutes

Spraying stolen credential list

SID: 120011

#5️⃣ Login from unusual country

Success login from country I don’t expect

I allow only IN

Anything else = suspicious

SID: 120014
