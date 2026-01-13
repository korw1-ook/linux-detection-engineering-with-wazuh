

# Korw Wazuh Rules (Linux SSH & User Activity)

This repo is where I write my own Wazuh rules.
They are all focused on Linux and mainly around SSH and user activity.

I made these rules to learn detection engineering and to catch
common things attackers do when they get into a Linux machine.

---

## 💡 What These Rules Detect

✔ Failed SSH logins  
✔ Invalid username attempts  
✔ Successful SSH login  
✔ Root login through SSH  
✔ Sudo commands being used   
✔ New user getting created  
✔ User being added to sudo group  
✔ Password changes

Each one of these events *can* be normal,
but they are also often used in real attacks.

---

## 🧩 Why I Picked These

When someone hacks a Linux box,
they usually:

1. Try many logins  
2. Find a valid user  
3. Log in successfully  
4. Use sudo  
5. Create a backdoor user  
6. Change passwords   
7. Come back later

My rules detect every one of those steps.



