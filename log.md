# Graduation Internship ViriCiti
## Week 14
### What did I do?
I started the week off with fixing bugs. I tackled quite a few. After that I implemented Redux some more to improve the app. The user's assets and fleets now are stored in the Redux state.

I also designed the app icons for the app and held a little user test in the office for these icons. I then setup all the developer accounts at Google and Apple for the release of the app.

On Friday I released all the services together with Sakif Surur. The first version of the app can now be tested inhouse. Exciting times!

### For who/what did I do this?
I did all of this to have enough time for the release process. We want to start testing the app as soon as possible. This can now be done.

### What went well/not so well?
Everything went well.

## Week 13
### What did I do?
This week I worked on bugs that needed to be fixed for the beta release. I first fixed the bug where my native server would crash if a socket suddenly disconnected. I then fixed the issue where a token expires. The app will now log you out if the token is expired. I also fixed the issues where the data wasn't sorted correctly.

I then looked into what's needed to compile the IOS app and release it. This week I also had meetings on what else needs to be done to take the app in full production mode.

### For who/what did I do this?
I did all of this to tie up loose ends some more and prepare for beta releasing. I want to get the beta live as soon as possible to keep the iterative process going.

### What went well/not so well?
The bug fixing and the meetings went well. We're getting there!

## Week 12
### What did I do?
This week I worked on the full notification pipeline. I needed to hookup the existing notification service to also send out push notifications to the correct user and device. I wrote a micro-service which hooks in to this service to do this. This was way out of my ballpark, but I got help from Sakif Surur to make this.

This week I also had a meeting with Simon Rijk and Freek Dielissen to discuss beta release plans. We are going test the app in house before releasing a beta to selected customers. This will give me feedback to make improvements before releasing.

I also worked on reading up on the whole release process at Google and Apple to see if I needed to figure out some stuff. It all looks pretty straight forward.

I ended the week with refactoring my code. I run my linter through all the code I written. This made a lot of improvements in the quality of the code.

### For who/what did I do this?
I did all of this to tie up loose ends some more and prepare for beta releasing. I want to get the beta live as soon as possible to keep the iterative process going.

### What went well/not so well?
Everything went well. The most difficult part was writing the micro service since I never work on these kind of projects. With the help of Sakif Surur I managed to get everything working.

## Week 11
### What did I do?
I started the week by creating an API route on the Native Server I build to send notifications to a user. Thanks to the Expo.io SDK this went really quick. I then worked on optimizing the app. I fixed a couple of memory leaks and improved performance overall. I then worked on the final step of the first version of the app. This step was hooking up the call to actions of a notification to whatever it needed to do. I ended the week with working on the visual design of the app. I styled the charts in the way ViriCiti's charts look like in the web app.

### For who/what did I do this?
This week I worked on final features and optimizations. I was all over the place to build and fix everything. ViriCiti wants to test this app amongst employees, so this was to do this as soon as possible.

### What went well/not so well?
This week went well, I managed to do a lot of stuff in a single week. I feel more confident in my product after fixing all these bugs and optimizing the performance. The app is getting there!

## Week 10
### What did I do?
This week I started working on the notification part of the app. I started with the user interface for these notifications. With a few mock notifications I could build all the pages and components needed. After that I started working on getting notificationtokens for Expo.io and handling the logic of receiving notifications. I implemented Redux to keep track of read notifications and displaying an unread notification badge.

After all of that I researched the back-end for the notifications some more. I started the week by using the Expo.io API for the sending of the notifications. I found the API in Node.js online. I could now run all of this locally before implementing it in the Native Server I wrote.

This week my internship supervisor from CMD Amsterdam also visited. We had a short talk on progress and what to do next. I also got my performance reviews by Simon Rijk and Sakif Surur. I ended the week with writing the report about this moment.

### For who/what did I do this?
I worked on the notifications this week because it is a big part of the app and I wanted to have plenty of time in the project to research and build this properly. If I finish this we can properly user test this.

### What went well/not so well?
Building the notification part went really well. I could use Redux, which I learned previously, to complete all the functionality. The performance reviews also went really well. My supervisors were really pleased with my performance the first half of the internship. I will try to improve even more and develop my skills further.

## Week 9
### What did I do?
I started the week off by going to Breytner. Breytner is the company I talked to previously through email at the start of the project. I discussed the features that I build, that I still have to implement and what they use ViriCiti's monitoring system for. This last one was very important.

Breytner is a company with four electric transport trucks. They don't look as much on a daily basis to a lot of data or reports. They're main concern is that the trucks charge overnight. If a truck doesn't charge (correctly) overnight they have a serious problem.

I discussed what we could add in the app to provide them with the information they needed in the easiest way possible. At the moment, you can see if a vehicle is charging. I assumed that that was enough. It turns out that that isn't enough. They usually look up the graph of the battery charging. This way they can see if there is a sudden drop in charging rate. This sometimes happens due to faulty charging cables. When this happens and they don't notice it they can get into trouble. They're trucks need to be charged because of the small size of their fleet. Two not fully charged trucks can cause serious problems. Because of this I want to implement the graph in the app. Currently the gauges with speed and state of charge are shown on the vehicle page. This doesn't make sense when the vehicle is charging. The speed will always be 0 and the soc will go up slowly. I want to take a look at showing the graph instead when the vehicle is charging. It's a small change, with a lot of impact.

This discussion led to the other part of the app. They can setup notifications if their trucks aren't charging withing a range of time. They explained that the trucks get connected to the charger at around 8 p.m. and need to be charged the next morning. By creating a notification for this and receiving it on the native app we can help them prevent this issue. It would be very useful if they get a notification that charging is not going as it should. When they click on the notification they should immediately see how the truck has been charging.

It turned out that Breytner needed this feature, but never knew ViriCiti already does this with emails and sms. It is a feature the user wants but doesn't find easily in the portal. Because of this I want to let users setup a notification in the app. This will be a more in your face approach to getting users to make use of this feature.

The rest of the week I worked on iterating over the design with the new feedback. I then implemented the changes in the app. I also build most of the notifications part of the app.

### For who/what did I do this?
I did this in order to get a better understanding on what the user deems important. I wanted to make sure that what I build will actually be useful for the user. I also started with the notifications part since I want to put out a beta version as early as possible to keep the iterative process going. I want to gather as much user input as I can over the next few months.

### What went well/not so well?
The meeting went really well. I was able to get to the core of the user's need. I could immediately implement the feedback in the designs and the app. Building the notifications part also went really well. I used Redux, which I learned a few weeks ago, to make this feature as good as possible.

## Week 8
### What did I do?
I started the week off with fixing the map after the app has compiled. In development I could see the map perfectly fine, but if I build a standalone app I wasn't able to see it. It was due to authenticating with Google.

After that I implemented Redux some more. I had to keep track of the current screen the user is looking at in order to improve performance by only fetching and updating data when needed.

The rest of the week I prepared for the meeting with Qbuzz in Utrecht on Friday and Breytner on Monday. I made sort of questionair to guide the conversation. I setup multiple lines of questioning based on what they could use the app for. I also printed all the screens for the event of the user wanting to explain something. They could then draw or write on the screens what they are trying to say.

I ended the week on Friday by going to Qbuzz. I was there for a few hours discussing what ViriCiti can offer them and listening to what they want as a user.

### For who/what did I do this?
I visited Qbuzz in order to find out what the user actually wants and to validate idea's to implement in the native app. I made a design and flow of the app and I wanted to test my assumptions with actual users. This is also part of one of my learning goals. I want this app to be as useful to every customer as it can.

### What went well/not so well?
The user testing at Qbuzz didn't go as expected. It turned out that the persons we were meeting weren't fully our end users. They will make use of the app, but the app isn't fully geared towards them. I could still get valuable information out of the visit. Since they use ViriCiti's monitoring system I could still find out what the company uses the system for. This validated my choice for what data to show in the app what is important to show. They also gave a lot of feedback on a future feature for the app geared towards the drivers of the vehicles. I took note of all their suggestions and idea's for the future.

On of the people we had the meeting had did have direct contact to the end users. I asked and instructed him to show the clickable prototype and ask the questions I provided. This way we could still get this information out of the end users.

The rest of the day I prepared the meeting for Monday with the people at Breytner, who will be the end users of the app.

## Week 7
### What did I do?
This week I learned a new skill. I've worked with React for a long time now. To take your React applications to a higher level you can make use of Redux. Redux is a state manager for you application. In order to make a good working application I wanted to learn this during my internship. It was tough to get into, but once I got the hang of it I could implement it fairly easily.

I also worked on the map component a bit more. I wanted to style the map and the markers according to the styleguide of ViriCiti. This gives the app a more round-up feel in the details.

A colleague also invited me to an other client to test and discuss the app. I will be going to Qbuzz in Utrecht coming Friday.

### For who/what did I do this?
I learned Redux for two parties. I learned it for ViriCiti in order to build a well structured and performing application. I learned it for myself to make myself a more skilled developer. Redux is a framework that I just needed to learn as a logical next step in application development.

### What went well/not so well?
I was really happy to learn Redux. It looked like a lot of new and complex things to learn, but it wasn't that bad once I got started. It gave me reassurance that I now know how to use this framework to take applications to the next level.

## Week 6
### What did I do?
This week I mostly worked on the temporary server for the native app. My app will eventually connect to the Gateway that is being build by an other intern. I decided to write a small back-end that will allow us to make a working MVP.

I also made authentication work. A user can now authenticate with his/her existing account. Previously there wasn't any form of authentication. I added this to make this MVP secure during testing.

The second part of the week I worked on two things. I provided my code with code comments to explain to future developers that will work on this project what everything is and does. I also made a more extensive README about what the app does and how you can run a development environment for it.

I have also written front-end tests. It is important for deployment that the code runs through tests to make sure everything works. I have never written a test so I had to do some research on how I can make them. I decided to use Jest, which was already supported by Expo.io. I wrote tests for helper functions I made, UI elements and most importantly the config of the native app. With this config you build the complete interface. It was important to make sure that this config is correct.

### For who/what did I do this?
I did all this work this week to ensure a well working, well documented and thoroughly tested product. By writing the native server, documenting the code and writing tests I accomplished this a bit more.

### What went well/not so well?
This week went well. It made me feel better about my product and my ability to transfer this project to the next person.

## Week 5
### What did I do?
I finished my MVP! Since I set up the web sockets for live data I could finish up the remaining tasks. All the vehicles still needed to be displayed driving on the map. After refactoring the code to make it more modularized I build this. All the data and functionality for the MVP is now there.

I also worked on the performance. The sockets get data multiple times per second. I updated the state several times per second per parameter. This was to much for the device to handle. I made use of throttling to fix this. The app now runs much quicker.

I ended the week with all the little tasks I needed to do to finish the MVP. I added the ViriCiti typography, added all the icons to the app, ensured that errors were handled correctly etc..

### For who/what did I do this?
I did this to have a MPV ready for user testing. I contacted one of the companies ViriCiti works with, Breytner, through the communications department. They're free to have me come over to do inquiries and user testing. In the few weeks I will visit them for this.

### What went well/not so well?
This week went well. I managed to fix all the things I needed to for the MPV in time for user testing. I was able to significantly improve performance. I also was very pleased about refactoring the code. It's not the most exciting part of building the app, but it was very much needed. The code is much more structured and modularized because of this.

## Week 4
### What did I do?
This week I started with live data fetching. It turned out that my temporary solution from last week was too heavy on performance. I basically fetched data every x amount of seconds. The request would be made even if the previous request was not returned yet. In order to fix this I used Async forever. Through a callback this will ensure that the code only gets executed when the previous request was returned. This significantly decreased the network requests.

The second, and most exciting part, of the live data fetching I improved was using native websockets for live vehicle data. I could not set this up previously due to the Socket.io web server. In order to add support for native websockets I setup a websocket server next to the Socket.io web server which will use the same code, but handles it's own connections. After this I spend a lot of time on making sure that the native app would handle sockets as efficient as possible. The app will setup a single websocket connection on load. After that, you can request this socket from every file in the project. There was one downside to using native websockets. It does not use the event emitter like Socket.io. There is just a single ```onmessage``` event. In order to add this to the native websockets I extended the socket class with an event emitter. This works well.

The rest of the week I spend on optimizing the app for tablets. Instead of using pixels for height and layout I made everything relative to the viewport. This ensures that the app will scale from smaller to bigger screens.

### For who/what did I do this?
I did this in order to improve performance and usability. I wanted this app to be ready for user testing and clients of ViriCiti. I also wanted the way I handle sockets in the app to be taken care of. This allows for easy upgrading the sockets once the ViriCiti gateway is live. I am acting like everything is already there in the app. This way we can easily upgrade later.

### What went well/not so well?
The fixes I did this week really paid off. The app runs much better now and is also responsive. This gave a nice feeling of accomplishment. Compared to the previous weeks this was the least fulfilling though. The week was about optimizations which are a lot less exciting than adding new features. It is a part of being a developer and that is why I was fine with it.

## Week 3
### What did I do?
I started the week of with taking care of the data side of the app. I wanted to build this early on in the process. The first step was requesting historical data from the ViriCiti API. This was a fairly easy task. I've worked with this API before so requesting data was quickly build. I used the API class I had written the week before. In order to make everything work I had to modify the data-server to be able to provide functionality I wanted the app to have. A example is getting historical data of all of your fleets combined.

I build a nice extra to the app to add perceived performance to the app. I'm able to set a fetch order in the configuration for fetching most used data first. If a user always looks at the current state of charge first, then this can be fetched first so it feels faster than it actually is.

The next task was taking care of live data sockets. This was somewhat trickier. The main library ViriCiti uses for this in their webapplications is Socket.io. I've worked with this library many times before. Socket.io didn't work as expected. The library wasn't able to get a connection. Luckily I didn't put all my eggs in the Socket.io basket. React Native natively supports regular websockets. The reason I didn't use this in the first place is that ViriCiti is migrating to this. I wanted to implement this once they did. So, for now i adapted. Since I'm building the MVP for this app I decided to use the regular API I used for the historical data. I'm able to request the latest value of a parameter. This was easy to implement since I could use the work I did for the historical data part of the app before. This will not be a thing to use in production since this is far heavier on the performance and data usage. This is because the socket will emit a new value once it changes. This temporary solution will just keep getting the latest value on an interval. This will happen even if it doesn't change in value.

### For who/what did I do this?
I started of with requesting the data this early on in the project so I would notice performance issues immediately. I can now optimize the app from the start while everything is still easily and quickly modified. The second reason I did this was for user testing. Users can now test the app with their own data. This is useful because we can see what they would do with the app once it's live. We can monitor the pattern in their usage. We have now almost got a MVP in within the first moment. I now have the time to iterate over this app.

### What went well/not so well?
Requesting the data went well. I was able to request data in a smart and reusable way. I had to adapt to what I was able to do with the data and even modify the back-end a bit. Overall this week was very productive for the road to the MVP.

## Week 2
### What did I do?
The week started off with iterating over the clickable prototype. I asked the customer service department to inquire about what the customers wanted in the new app. What do they use our system the most for and would they like to see in the app. Breytner, one of the companies that use the system, replied with an extensive wish list. I've used this feedback to iterate over the prototype adding multiple new features like vehicle state and seeing where all the fleets are on the map.

After that I called a meeting with most of the developers. I wanted to discuss the handling of authentication and data requesting. Since a lot of services need to be connect to each other to make everything work I thought this was important. We were able to make a plan which everyone agreed on by doing this. It was a productive meeting where everybody could share their thoughts and expertise.

The rest of the week I build the entire front-end for the dashboard part of the native app. This went really quick, really really quick. This is mainly due to the experience I've gathered in the past two years. I've build all the components in a re-usable way so the codebase stays maintainable and extensible. I also made sure I build all the elements based on a configuration file. This way, all parts are easily changed by changing a parameter in the configuration. This allows for a maintainable and extensible application as well.

After I build all the pages of the dashboard I hooked up the real fleets and vehicles to the app. The dashboard is now ready for the final step. This step is to hook up real-time and historical data. A nice addition is the API class and Local Storage class I've written. This ensures that all the logic is in a separate re-usable file. This keeps the codebase neat and DRY.

### For who/what did I do this?
I iterated over the original prototype to implement user wishes in the app. It makes sense to first make this in a prototype so I wasn't distracted by technical boundaries. It was also nice to spark the conversation with this prototype.

I called the meeting to discuss and agree on the authentication and data requesting in an early stage. This way everyone knows when they need to do their part and what is needed.

In my original planning I wanted to first have all the data present and then start with the building of components. Since I have to work with other developers who are not ready for that yet I decided to start with this. I can build all components with mock data. This speeds up the process of the project and allows for early user testing.

I hooked up the real fleets and vehicles to the app because after this is done we can do proper user testing per company with their own data. It also brought up the first performance issues which I otherwise wouldn't have encountered until a later stage. I was able to fix this fairly easy now.

### What went well/not so well?
The second week went really well! I was able to do a lot of work in an orderly and structured fashion. I was able to show a pro-active attitude which was greatly appreciated. My internship supervisor, Simon Rijk, was impressed by what I build and how I build it. He also liked that I inquired for user input at real companies. I want to keep this up throughout the internship.

## Week 1
### What did I do?
The week started off with some more explanation about the project I was going to do. After that I started with idea generation. I sketched a few idea's to spark the conversation. After that I got feedback on the idea's. With this feedback I started building and designing a clickable prototype which we can test with users. Throughout this process I received feedback for improvements.

I've also spend a good few days diving into React Native, the framework we are going to use in order to build an Android and IOS app with my skills in React. I researched some development environments and quickly came across Expo.io. With the development environment running I started researching React Native. I build a few components to check if I understood everything.

Near the end of the week I started the main project. I researched and build tab-navigation and stack-navigation in order to be able to click through all the screens I was going to build. This was a challenge, but really useful to get out the way at the start of the project.

Finally, I setup a planning for this project. I used Asana as the tool to do this. I build main tasks with subtasks for most of the project. The earlier on in the project, the more detailed the tasks are. This way I could see what's needed to build this app. By continuously keeping track of progress and results here, ViriCiti can see how the project is coming along.

### For who/what did I do this?
I build the prototype mostly for testing our idea's with the users that are going to be using the app. Since this is a new project, it was also great for opening up discussions on what the app should do in detail.

I dove into React Native mostly for myself. I wanted to get my development environment and first small app up an running in the first week so I would be able to make a good planning based on how long it would take me to build.

I setup the project planning in Asana for ViriCiti and myself to give some guidance throughout the project. The ViriCiti team and I now also know at which stage of the project several people will have to jump in to make the functionality happen (e.g. modification of current API).

### What went well/not so well?
The first went really well! I got to know the project and what is needed. I was able to visualize idea's from ViriCiti and myself in the form of an hi-fi clickable prototype. Understanding React Native went even better. I am experienced in React so there wasn't a steep learning curve. Later on in the projects, for instance with building notification functionality, I might have some more trouble.

This went so well because this isn't new to me. I learned the core of Javascript during the minor webdevelopment. This helps me to quickly learn new frameworks. Designing and building a clickable prototype wasn't new to me either since we learned this throughout the study. I was able to put the skills I learned during CMD in to practice.
