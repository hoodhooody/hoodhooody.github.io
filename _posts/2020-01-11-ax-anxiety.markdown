---
layout: post
title: Ax Anxiety
date: 2020-01-11 14:00
description: A simple kotlin app # Add post description (optional)
img: ax-anxiety-background.png # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Programming, Kotlin, Android, App, Project]
---
I had been hearing about Kotlin for a while now, specifically in that way programmers tend to talk about new tech, you know the "Kotlin is the best programming language ever, it cured my baldness and saved a puppy" or "Why you should skip Kotlin because it's awful and it nicked a fiver from my flat" angles.

So, since I'm the type of person that needs to bring a hand close to a fire before I believe it's lit, I decided to write a little project in Kotlin.

## The problem
Whenever I'm in public transport I'm always listening to something, be it audiobooks, podcasts or music. Inevitably there is a small amount of anxiety everytime I'm about to start listening, that my headphones are not connected properly and that the whole wide world will know that I listen to podcasts about serial killers or how much old-timey latino music I actually listen to.

## The solution
A small simple app that plays a completely harmless and unobstrusive sound.

## The implementation
I considered going with Xamarin at first since it's cross platform, but I don't own a Mac and was unwilling to rent one, and due to the aforementioned desire to do something with Kotlin, I decided to go with just Kotlin and Android.

The app is amazingly simple, two screens. One screen has two buttons, one that plays a woodblock sound and another one that plays a beep sound. The sounds were procured from [freesound.org](https://freesound.org/). The other screen is a credits screen.

## The web version
Since I wasn't doing an iOS version, I might as well make a web version. I used [Materialize CSS](https://materializecss.com/) to keep the feel consistent with the Android theme and [howler.js](https://howlerjs.com/) to ensure playback support accross browsers. To save on hosting costs and since I didn't need any server capabilities, I hosted the site on Amazon's S3. I also bought a domain name [axanxiety.mobi](https://axanxiety.mobi/) and used AWS's Certificate Manager to provide an SSL certificate.

## Google Deploy
The actual registration and deploment to Google Play was surprisingly simple. Android Studio provides most of the tools needed, including app signing. I hired a cheap-o designer off of Fiverr to create a logo for me, which also became the website's favicon.


## The end product
And here it's, [the app](https://play.google.com/store/apps/details?id=com.axanxiety.app) and [the website](https://axanxiety.mobi/).

## Lessons Learned
Honestly... The project was a bit too small to give a detailed account of Kotlin. It did feel quite familiar though, like when you're hanging out with a good mate's sibling and even though you don't know them, you know enough about them to not feel awkward. Like with most engineering subjects, the best solution is always to try things out. And even though I can't say for sure if Kotlin is the panacea that will heal all your woes with Java or Android development, it certainly is a fun little wrench to throw into your toolbox.