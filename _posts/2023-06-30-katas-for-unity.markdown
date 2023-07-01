---
layout: post
title: "Katas for Unity: Exercises to deepen your understanding of Unity ( And any other Game Engine For That Matter)"
date: 2023-06-30
description: Ignite your game dev prowess with Unity katas! Dive into practical exercises and level up your skills. 
tags: []
---
I'm a enthusiastic martial arts student, although I wouldn't call myself an expert. I prefer to think of myself as an eternal white-belt, continuously seeking knowledge. While I have a basic understanding of various martial arts, including boxing, Greco-Roman wrestling, German and Italian Longsword, Scottish backhold, Jiujitsu (both traditional and Brazilian), savate, and judo, my expertise is limited across the board. However, one concept that transcends different martial arts is that of the kata.

In its simplest form, a kata is a predetermined sequence of movements practiced individually. Katas are designed to refine techniques, enhance balance, and foster mental discipline. They facilitate memorization and repetition of fundamental movements.

There is an ongoing debate about the efficacy of katas as teaching methods, considering the advancements in pedagogy since the 19th century when most modern martial arts systems were codified. However, the scope of this article does not delve into that debate. Instead, I aim to use the concept of the kata to introduce a series of exercises that can be performed in Unity or any other game engine to enhance your understanding of the engine and sharpen your game development skills.

Similar to katas, the exercises I suggest are for training and simulacrum, and they can never replace work experience, and you should adapt and mold them to suit your preferred work style.

On the other hand, it's essential to remember that game development is a realm of anarchy where rules are scarce, except perhaps for a few practical guidelines like refraining from releasing projects on a Friday or before holidays.

Without further ado, let's delve into the katas themselves:

Kata 1: The Crafty Dragon Laughs In His Junk Palace - The Workshop

The Workshop serves as the first kata we'll explore. Essentially, the Workshop is an eternal Unity project where you can experiment, test new concepts, and explore recently released features. Here are a few examples of what you can do within the Workshop:

* Utilize it as your proof-of-concept staging ground. When you have a new game idea and want to quickly prototype it without worrying about names, designs, or anything besides the core gameplay (which should be your primary focus), the Workshop offers an ideal environment.
* Utilize it as a repository for commonly used code. Certain pieces of code will inevitably be reused, but you may not want to rely on searching the web each time. For instance, in my Workshop, I have custom code snippets for handling buttons, game states, pause menus, and various other essential elements that every game requires. These snippets save time and effort, eliminating the need to write custom code for each new game.
  * A helpful tip for this approach if you ever copy code from online soruces is to ensure you understand the copied code, rewrite it to adhere to your project's style and standards, and add a comment indicating its origin. Code authors may update their implementations, or you may forget the context for using a particular solution, but a comment can provide the necessary information.
* Utilize it to learn, experiment, and test new features. By keeping the Workshop project updated to the latest version (you can maintain a separate branch for the LTS version), you can explore new features without the burden of creating an entirely new project or worse, trying to fit them into your ongoing project.
  * As of June 2023, for example, Unity has released a new set of AI Tools. Instead of creating an entirely new project to utilize these features, I can reuse existing scenes in my Workshop to experiment. For instance, my simple pong implementation could benefit from AI-generated textures.

Kata 2: The Crafty Fox Dances for the Moon - The Clone

Have you ever played a game and wondered, "How did they accomplish that?" Now is your chance to find out. When you lack ideas for your own game development or are between project, select a game you've recently played, choose a mechanic, effect, or feature from that game, and attempt to clone it.

While undertaking this exercise, keep the following points in mind:

* When I mention cloning, I'm not referring to an exact replica but rather capturing the essence of the chosen element.
  * For instance, I've recently been fascinated by the movement system in Spider-Man: Miles Morales. However, attempting to clone the entire movement system of such a complex 3D action game would be quite challenging. Instead, I would focus on cloning the aspect that most captivates me, such as web swinging. To accomplish this, I don't need a complete Spider-Man model or detailed buildings. A simple cube responding to player button presses and creating a rope from which the player character swings and moves forward would suffice to replicate the freedom of movement experienced in the original game.
* Set a strict time limit for yourself. Remember, you're not creating an entire game but rather cloning a single element from an existing one. Allocate around six working days, equivalent to three weekends, which is ample time for both full-time students and working developers.
* This is the perfect opportunity to leverage the Workshop. It provides an ideal space to store your cloning projects. If you decide to pursue a specific concept further, you can easily copy it into its own project without sifting through lists of abandoned Git projects.
* If your portfolio feels somewhat lacking, this exercise is an excellent way to enhance it. Take the cloned element, polish it by adding a menu, pause function, background music, and an introduction explaining your goals. Such a finished product will impress recruiters far more than a document filled with brilliant but unfinished game ideas.
* After each cloning exercise, conduct a brief post-mortem analysis. Reflect on what worked well, identify weaknesses, consider future improvements, and extract any valuable lessons worth carrying forward.

Kata 3: The Gods Love a Fool - Clowning

Occasionally, I indulge in clowning. I select an idea that is technically interesting or combines several technical components I wish to learn or revisit, but holds no commercial potential or practical value.

The purpose of clowning is to remove the pressure for perfection. When working on a project intended for profit or presentation to others, design decisions become more conscious. Clowning allows you to focus solely on deepening your knowledge in specific areas.

For example, a few years ago I embarked on a project called "Wizardry Exchange." It was an app that converted currency from real-world denominations (CAD, EUR, GBP, or USD) to the currency used in Harry Potter's universe (knuts, sickles, and galleons). This project involved Unity3D WebGL for the front-end, Go for the backend, a custom caching system, and deployment on AWS using Docker.

Is this a practical or useful project? Not at all! The front-end doesn't require Unity, Go is overkill for a few simple endpoints, and the application could run on a potato, let alone AWS.

So, why go through the trouble? To learn about WebGL with Unity, employ Go for server development, and gain experience in building and deploying applications using Docker on AWS. The end result isn't as important as the process of acquiring knowledge.

Here are a couple more considerations for clowning:

* Clowning projects are not intended for sharing, so embrace the freedom to work on things that genuinely interest you. Unlike The Clone, this project is more time-consuming.
* However, limit your clowning projects to no more than two months of work. It's a valuable exercise but should be approached as a means to introduce variety into your training regimen.
* Avoid trying to incorporate every possible learning aspect into your clowning project. Choose two or three areas you want to explore, and feel free to reuse code (perhaps from your Workshop) or copy code for parts you aren't particularly concerned about.

And that concludes the three katas that can help deepen your understanding of Unity or any game engine.

I'd like to draw attention to a specific phrase I used earlier: "training regimen." This approach has guided my engineering practice for over 15 years. I consider graduating from univerity like getting your black belt, and, similar to Judo (from which the belt system originated), a black belt signifies a grasp of the basics rather than mastery. It is expected that, after attaining a black belt, one undertakes independent research to further develop their skills in the art of Judo.

Likewise, upon graduating, it becomes your responsibility to establish a training regimen to continually improve your technical skills and acquire knowledge. While you will gain knowledge through work, it may lack guidance and personal development. Thus, creating a training regimen to sharpen your engineering skills is crucial. This way, if an opportunity arises, such as a new position opening up in your company, termination from your current job, or encountering an enticing role elsewhere, you are equipped with more than just work experience.

Remember that, unlike in university, your job may not necessarily prioritize advancing your talents beyond a certain point. A good job will, but distinguishing between the two can be challenging at times. Having a training regimen in place safeguards your professional growth.

I hope that you've found these katas at the very least interesting if not useful, and that they might unlock a new way for advancing your technical skills.