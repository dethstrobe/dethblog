---
title: "How to delete a passkey on Chrome."
description: Find out where the hell passkeys are kept
date: 2025-08-28
tags: [Google Chrome, passkeys, passkey management, Chrome, MacOS]
---
Let's say you're developing a site on localhost, like you do. And you're using passkeys, because they're said to be more secure, spoof proof, phish proof, the future of web authentication, etc etc.

So naturally, you wipe your DB and regenerate the DB, and all your migrations and seed files worked! But, when you go to register a new user and log back in, you see the old passkeys still being prompted.

So you give one of the old passkeys a shot, and of course it fails, because the DB doesn't remember those old credentials. Okay, nice to know, you can't just sign in with any ol' passkey. But how do I remove the now dead passkey? Well, after wasting all day on trying to figure out how to do that, I'll tell you.

There are 3 places you'll want to look.

I'm on a **Mac (15.6.1)** using **Google Chrome (139.0.7258.139)**, by the way. So this article might not be as relevant to people using other OSes.

## Inside Google Chrome Settings
[chrome://settings/passkeys](chrome://settings/passkeys) is the url you want to plug in to your browser to see any locally saved passkeys. Odds are this will be empty. The reason it is empty is because Chrome usually offloads passkey management to another credential manager, like the build-in OS's credential manager. But if you don't have it setup to sync with another cred manager, you might find some passkeys here.

## Passwords App
So it turns out that moved all authentication from Keychain Access to a new and dedicated app called **Passwords**.

In there you'll find a little button on the left called **Passkeys**, where–as you might have assumed—is the home for all the passkeys saved on your Mac and synced up to your iCloud.

If you select one of the passkeys, you'll notice a little edit button in the corner. And from there you can click the **Delete Passkey** button to send that passkey to the Shadow Realm or something like that.

## Google Password Manager
While [passwords.google.com](https://passwords.google.com/) doesn't mention passkeys, it does actually contain passkeys.

For myself, I searched for good ol' **localhost** and found it there. There are also some localhosts with ports (i.e. `localhost:5173`), but the one I was looking for was just under plain ol' **localhost**. From there, once I deleted them from passwords.google.com they were removed from my passkey prompts in Chrome as well.

---

There, hope that helps. So you don't have to waste all day trying to hunt down where the devil Chrome is hiding your passkeys.