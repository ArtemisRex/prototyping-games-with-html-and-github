Introduction
===
I’ve been using HTML5 recently to prototype a few game ideas. I’ve spent quite a bit of my career happily writing C/C++ for graphics and numerical analysis applications; but for some odd reason I also enjoy writing JavaScript. It’s a productive, rapid prototyping language that runs incredibly fast in modern browsers thanks to optimized interpreters like V8 [reference here]. In fact, the prototypes I’ve done so far are fast enough that I haven’t needed to minify or compile using something like [Google’s Closure compiler](https://developers.google.com/closure/compiler/).

For my current project I’ve decided to do a significant portion of the prototyping in JavaScript and port the result to Objective-C. I have no idea how well this will work but I feel like anyone with some proficiency in both languages should be able to pull it off. I’ll save that discussion for a later post. In this post I’d like to show how I use Github to host my HTML5 prototypes for free. The technique is simple and only requires a [Github account](https://github.com) and some basic [Git](http://git-scm.com/) skills.

Prototyping
===
Anyone who’s written a game has experienced that moment when the player gets it. The “a-ha” moment is so much fun; and getting “a-ha” moments in front of players quickly is incredibly inspirational for me. This is why I love prototyping with HTML5. Anyone with a modern browser can be testing your prototype within a matter of seconds...with zero installation. From a developer’s perspective the dev environment is about as simple as it can get. All you need is an editor and a good browser. I’m currently using Vim, [Powerline](https://github.com/Lokaltog/powerline), [jshint](https://github.com/wookiehangover/jshint.vim) and Chrome.

Hosting
===
If you haven’t used git and/or Github, I’d recommend trying both out. I’ve used git at my last two jobs and it is by far my favorite version control system. A while back I discovered this this neat little Github feature that allows you to host static web pages for each of your repos. Simply create a branch called `gh-pages`, add an `index.html` and viola, Github’s hosting your page. The page can then be found at the following location: `http://<your-github-name>.github.io/<your-repo-name>`

Here’s the cool part. If your game or prototype is already written in JavaScript and HTML5 you likely already have an `index.html` which means the only thing you need to do is create a `gh-pages` branch off any working branch and push it up to Gituhub. For example, let’s say you’re on a branch called dev and you’ve got something running locally in a browser. You can push your work up to Github for the world to see in three easy steps: 

~~~
git checkout -b gh-pages
git commit -am “did some work”
git push origin gh-pages.
~~~

Here’s a simple example: 

Repository: [github.com/JeffLutzenberger/protoyping-games-with-html-and-github](https://github.com/JeffLutzenberger/prototyping-games-with-html-and-github)

Hosted Page: [jefflutzenberger.github.oi/prototyping-games-with-html-and-github](http://jefflutzenberger.github.oi/prototyping-games-with-html-and-github)

If you clone or fork this repo you’ll be able to run the simulation locally and also push it up to your own Github repo for the world to see.  

Limitations and Observations
===
###Pros

Unity engine: Github pages will run Unity based games and demos just fine.
WebGL: WebGL works great.
It is free and super easy to set up.
Github is awesome: Github is a great way to share your code with the world. As a hiring manager, it is one of the first things I look at when reviewing candidates.
###Cons
Static hosting: You can upload JavaScript libraries like twitter bootstrap [reference] and jquery [reference] but github does not provide a datastore option. So far for my prototyping needs this has been an acceptable tradeoff. 
Your pages are wide open (potential con). While you can lock down your repo by making it private, at the time of this writing the pages are still publicly visible [try this out!]

Conclusion
===
I think this is a pretty neat way to prototype. It has some obvious limitations for sure but for the type of games I’m currently experimenting with I’m finding it incredibly fun. It allows me to easily get ideas in front of people and encourages me to be more open with my code...so, now that I’ve shown you mine, let’s see yours!    


