```
---
title: Tracking how much I go to the bathroom
author: Andreas Backström
date: 2020-07-20
slug: tracking-bathroom-times
---
```

A topic that no one wants to talk about unless your five years old, poop. But it is something that we all do and sometimes actually gets questioned about (mainly by doctors).
So how many times per day do you go to the bathroom? A question I could not even guess an answer too before yesterday. 



## Keeping track

I use a rather simple method of logging when I go to the bathroom. After I am finished I open a app on my phone and click a button corresponding to what I did (if I peed, pooped or both). The app then calls an API endpoint on my server and writes two things to the database I use to store my health related data in. The first is what I did and the second is when I did it, date and time. This then gets displayed on [health.andreasbackstrom.se](https://health.andreasbackstrom.se) in a simple table at the moment.

The API was made to allow me to use different ways of communicating a bathroom visit, the app is only the first and I plan to expand into using buttons or sensors of some kind in my bathroom.

<img src="/images/posts/tracking-bathroom-times-01.png" alt="Image of app with three buttons, each having an emoji on the buttons." width=500/>

Just to make it more fun, the app looks a bit childish with it's three buttons 😄 



Both the app and API are custom made for this sole purporse by yours truly and is at the moment not open-sourced. 

The app is made with [Dart](https://dart.dev/) and the [Flutter framework](https://flutter.dev/) and only has three buttons to interact with, depending on what button you press a corresponding POST request will be made to the API server. 

The API server is written with Python [flask](https://flask.palletsprojects.com/en/1.1.x/) and deployed with [gunicorn](https://gunicorn.org/) and nginx on the same server as my health dashboard. The API then talks to the database.



One thing to possibly work on in the future is to generalize the API and app to commendate more types of datapoints.



## But why?!

For me, there are a few reasons to do this. Mainly I want to know if I can see some kind of long term pattern in when in the day I am most likely in need of a bathroom. But it is also something that we might spend a lot of time in doing and I would like to see if we can optimize our bathroom visits in someway.



So if you are interested in knowing how many times per day I go to the bathroom, you can visit my health dashboard over at [health.andreasbackstrom.se](https://health.andreasbackstrom.se)

Bathroom related data is only available from 2020-07-19 and forward into the future.



Thank you for reading.

-Andreas