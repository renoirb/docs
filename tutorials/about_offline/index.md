---
title: Introduction to offline web applications
attributions:
  - 'Portions of this content come from HTML5Rocks! [article](http://www.html5rocks.com/tutorials/offline/whats-offline/)'
readiness: 'Ready to Use'
summary: 'An introduction to offline applications.'
tags:
  - Guides
  - FileAPI
  - IndexedDB
  - Webworkers
uri: 'tutorials/about offline'

---
**By Michael Mahemoff**
Originally published published Aug. 2, 2010, updated Oct. 13, 2011

## Summary

An introduction to offline applications.

## Introduction: The Meaning of "Offline"

"Web" and "online" are two closely associated terms, downright synonymous to many people. So why on earth would we talk about "offline" web technologies, and what does the term even mean?

At one level, we can talk about completely offline web apps, those unusual creatures that run inside a browser, but never see the light of the internet. Typically, they will run on a `file:///` URI, pointing to a hard drive, USB key, or DVD (if you remember those). For example, those USB keys you sometimes get at conferences, which you stick in your computer to receive a multimedia presentation of something-or-other, running in your browser. A more complex example is the concept of Single Page Applications, like [TiddlyWiki](http://tiddlywiki.com), a kind of personal notepad that runs entirely offline, exploiting custom browser features to save changes to the hard drive.

However, it gets more nuanced than "always-offline". Another class of applications is "online-offline" apps (sometimes just called "offline apps", somewhat ambiguously). These apps are ultimately intended to sync with the cloud, but can survive periods of downtime. The downtime might be an interim loss of connection, like passing through a tunnel, or an extended period of offline activity, like a long-haul flight. Online-offline applications will handle these cases with varying degrees of gracefulness. An example is GMail's [offline facility](http://gmailblog.blogspot.com/2009/01/new-in-labs-offline-gmail.html).

There are also online-offline applications that intentionally keep certain information locally. Sometimes, that might be done to tie data to the browser, rather than to the user's account, e.g., the current song being played by a media player application. Local storage is also an interesting alternative to server-based storage for simple applications without user registration; by offloading data storage to clients, you avoid the hassle of maintaining a database on your server. Of course, you should only do this for non-critical data, e.g., a list of recent searches. Another reason is security and privacy, the concept of [Host-Proof Hosting](http://ajaxpatterns.org/Host-Proof_Hosting). An early example is [HalfNote](http://www.youngpup.net/2006/10/09/), by Aaron Boodman (now a Chrome engineer).

Online-offline applications come at the cost of increased complexity, and you should consider whether offline support is justified. The argument against this mode is best summed up in a [famous article](http://37signals.com/svn/posts/347-youre-not-on-a-fucking-plane-and-if-you-are-it-doesnt-matter) from a few years back. David Hanson makes the argument that it's not worth making offline apps just for airplane activity, which is the one place you're likely to be offline for a long period of time. But there are still situations where it's worthwhile, and also situations where offline technologies are useful for protecting aganst server or network outages. Just be aware that it comes at the cost of complexity, and that that complexity needs to be justified.

Even assuming an internet utopia where everything is always online, offline technologies still serve a purpose. Why? Because it's faster that way. Offline technologies support caching and detailed control over the caching process. Therefore, web apps can boot quickly and show data instantly. You might protest that these technologies shouldn't be called "offline" if they are used by purely online apps. Yes, the term is ambiguous. At one level, "offline technologies" could be defined as "technologies supporting offline apps", making the protest valid. But another definition is "technologies operating outside of the cloud", and that's the one used here. Of course, there's a lot of overlap between the two definitions; offline apps certainly need to operate outside of the cloud.

As well as offering quick startup, offline apps can be used in a transient way too. Although bandwidth is much faster these days, there are still noticeable limitations for certain applications, in terms of both throughput and latency. If you were designing a high-density video editor, you'll probably find the video is too big to fit into memory at once, meaning you have to swap content in and out of your app. It would be painfully slow to store the whole thing on a server (unless you and all your users are lucky enough to be on a super-fast network). Much better to store the entire video offline and push *changes* to the server as and when they happen.

## Application Cache and Offline Storage

There are primarily two offline capabilities in HTML5: application caching and offline storage (or "client-side storage"). The distinction is core application logic versus data. Application caching involves saving the application's core logic and user interface. Offline storage is about capturing specific data generated by the user or resources the user has expressed interest in.

For example, imagine a browser-based game. Application caching would retain the initial HTML document, the JavaScript, the CSS, frequently used icons and images for game characters and scenes, and sound samples. Consequently, the next time the user visited the site, it would load immediately. To some extent, regular browser caching will already enable that capability, but browser caches are easily overwritten, whereas application caches are intended to enjoy special status on the user's hard drive so they can't be displaced just because the user downloaded a large video. In addition, there are APIs to control what's cached and what's not, which is not the same as regular browser caching.

In our game example, visiting the site a second time would load the site instantly—but what if we wanted to let the user continue playing the game from a previous position, i.e., restore the state of the game? The kind of data required is not held in the application cache, because it's user-specific, so this is a job for offline storage. Whenever the user hits save, we upload to the cloud but we also store game data on disk at the same time, i.e., store it offline (for example, we might save the player's health level and the states of all objects and characters inside the game universe). We might even keep a loop running to continuously store the game data offline. That way, the latest changes are still there if the user loses connectivity and has to shut down the browser before they can get online again. It also takes less bandwidth than continuously uploading the various states to the server. We might save data locally every 10 seconds, while uploading it only every 5 minutes as a bandwidth-saving measure.

You can read more about AppCache [here](http://www.html5rocks.com/tutorials/#appcache).

## Older Offline Storage Techniques

While there's only one kind of application cache, there's a whole flock of offline storage capabilities available, or becoming available. Let's begin with a quick survey of older storage techniques, those that have been around several years and are not generally associated with the "HTML5" label.

### Cookies

Cookies have been around since the early days of the web. They were originally intended to associate a little data with the user, though these days most applications only store identifying information and store the rest of the user's data on the server. Still, the fact that cookies can store some data does put them in the category of offline storage. However, the data capacity is extremely limited, as low as 20 cookies limited to 4KB each according to [this specification](http://www.ietf.org/rfc/rfc2109.txt). Just as important, cookies slow down network activity because they are transferred to and from the server inside HTTP headers.

### Plugin-Based Storage

Plugin-based storage has been supported by several plugins, notably Flash, Java, and Google Gears. Since Flash 6, there has been the concept of a local shared object. Java applets have also been an option, since Java can write to local files. Google Gears is a third example of a plugin, and in its case, offline storage was one of the main selling points right from its inception. The main downside of plugin-based storage is the obvious one: You have to assume the plugin is present, and that you have the right version. It's not uncommon for company firewalls to block plugins and for plugin releases to lag behind, or not exist at all, on certain operating systems. You also have to have faith in the plugin manufacturer keeping up plugin quality and market share going forth, versus the easy substitutability of open-source, open-standards based browsers.

### Browser-Specific Deatures

Browser-specific features are capabilities that are available, but outside the realm of standard web technologies. They typically have an "underground" nature, being little-known and lightly documented. For example, TiddlyWiki and the derivative [twFile jQuery plugin](http://jquery.tiddlywiki.org/twFile.html) use IE-specific and Firefox-specific APIs to access the underlying file system on those respective browsers, falling back to Java applets where that's not possible. IE, since version 5, also supports the [UserData](http://msdn.microsoft.com/en-us/library/ms531424(VS.85).aspx) API. Similar to plugin-based storage, the problem with these is significant: You're requiring the user to be working with a particular browser and you're putting faith in the browser manufacturer going forward. This is different from using features only present in just one or two browsers *so far*, where the feature is part of an open standards process and other manufacturers are likely to include it in the future.

## Offline Storage in the Era of HTML5

The newer storage APIs, what we might call "HTML5 storage", are generally superior in terms of openness and standards compliance. Of course, not all browsers include all of the new APIs, and you may have to support older browsers that don't include any of them at all. So the older techniques are still useful for graceful degradation.

The new APIs are Web Storage (also called "Local Storage" or "DOM Storage"), Web SQL Database (or simply "SQL Storage"), IndexedDB, and File Storage. In all cases, the same-origin principle applies: the store is tied to the [origin](http://dev.w3.org/html5/spec/Overview.html#origin-0) of the site that creates it (typically this amounts to the site domain or subdomain), so that it cannot be accessed by any other origin. Stores and origins are therefore associated 1:N, where N is the number of distinct storage mechanisms represented by the current browser. For example, Chrome currently supports Web Storage and Web SQL Database Storage, so a given origin (e.g., "html5rocks.com") has access to precisely two dedicated stores when the user is visiting from Chrome.

Now let's meet each of the new storage technologies.

### Web Storage

[Web Storage](http://dev.w3.org/html5/webstorage/) is a very convenient form of offline storage, being just a simple structure of key-value pairs like any JavaScript object. This works well for situations such as the game example, where you could store the current game under a "currentGame" key: `localStorage["currentGame"] = gameState`, and load it back the same way: `gameState = localStorage["currentGame"]`. If you wanted to keep a list of saved games, you'd just store an array inside this structure, `savedGames = localStorage["savedGames"];`.

Although the spec indicates that values can be any type, this is not the case in practice. Browsers presently support only string values, so you will need to serialize your values for storage (i.e., convert them to strings). Fortunately, we have built-in serialization these days, by way of the JSON API, so you can do something like: `localStorage["currentGame"] = JSON.stringify(gameState)` and `gameState = JSON.parse(localStorage["currentGame"])`.

There's also a variant of localStorage called "sessionStorage". It's there mostly for security purposes, as the data is removed when the window is closed.

For many offline storage scenarios, Web Storage might be all you need, and it's the most compatible format right now. However, the data isn't structured, so if you wanted to locate all games at level 10 or above, for example, you'd have to iterate through every single game item manually.

A gotcha and further downside of Web Storage is the lack of [transactions](http://en.wikipedia.org/wiki/Database_transaction). For example, the user might have your app open in two tabs. Tab 1 starts writing several things to the database, then tab 2 starts reading it, getting the data when it has only partially been updated. Thus, Web Storage is "racy", meaning it's susceptible to race conditions, and you need to take precautions to ensure the integrity of your data and the accuracy of any queries.

### Web SQL Database

[Web SQL Database](http://dev.w3.org/html5/webdatabase/) is just what it says on the tin: an offline SQL database. Implementations today are based on [SQLite](http://www.sqlite.org/), a general-purpose, open-source SQL engine. It comes with all the pros and cons of traditional databases. On the one hand, you have a fully relational structure, allowing you to rapidly query and manipulate data via joins, e.g., "delete all saved games where the level is less than 10 and the game hasn't been loaded in the past 30 days". You can express that in a line of SQL, whereas you'd have to manually wander through the equivalent corpus of Web Storage data. And if you have a strong need for performance, you can also lean on several decades of research on database optimisation (although tuning would have to be done separately for each possible SQL engine being used).

Furthermore, there's support for transactions, so that your database is protected from the kind of race conditions that can arise with Web Storage.

On the other hand, Web SQL Database also comes at the cost of complexity. Do you really need a full-blown database in your front-end web client? Do you really want to go through the effort of specifying a schema and coding up SQL for every data access? Sometimes it's overkill. The other issue is compatibility. For now, Microsoft and Mozilla haven't put it in their plans and don't have any (public) plans to do so. You can still use it if you feel there will be advantages, but unless you only need to target a particular browser that supports it (e.g., a Chrome extension), don't use it in a way that assumes it's definitely present.

You can read more about Web Database [here](http://www.html5rocks.com/tutorials/#webdatabase).

### IndexedDB

[IndexedDB](http://www.w3.org/TR/IndexedDB/) is a nice compromise between Web Storage and Web SQL Database. Like the former, it's relatively simple; and like the latter, it's capable of being very fast. The trick is to take a standard mapping, like LocalStorage, but index on certain fields inside the stored data. So if your game data was a structure including a "level" field, you could tell IndexedDB to index on "level". Consequently, you can make fast queries about game levels; your application won't have to trawl through all the game data structures because it has a separate list of just the "level" fields. And it has a concept of cursors, so your application can quickly walk through result sets.

As with Web SQL Database, you also have transactions available to protect against race conditions.

You can read more about IndexedDB [here](http://www.html5rocks.com/tutorials/#indexeddb).

### Filesystem API

[File API: Directories and System](http://dev.w3.org/2009/dap/file-system/file-dir-sys.html) fills a niche not supported by the other techniques. It gives you a way to store binary content (as well as plain text), create folder hierarchies, and store potentially huge data structures. There are separate specifications for its other component APIs: [FileReader](http://www.w3.org/TR/FileAPI/) and [FileWriter](http://www.w3.org/TR/file-writer-api/).

The Filesystem API is supported today in Chrome, enabling apps to create and access and entire sandbox directory structure.

If you need a directory structure, use this API to store large chunks of data, e.g., large text documents or even entire movies.

You can read more about the File APIs [here](http://www.html5rocks.com/tutorials/#file).

## How to Use the Offline Technologies

In this section, we'll look at some common problems developers face. The solutions are somewhat speculative, given that most of these technologies are new and, in some cases, not even implemented yet! Nevertheless, applications like GMail have been using some aspects of these technologies for several years (as well as the earlier Google Gears plugin), so we can suggest some meaningful rules of thumb.

### Storing Miscellaneous Data

All things being equal, Web Storage should be your default port of call for storing offline data. It's a dead-simple API and one that's widely supported. Only consider using the other techniques if you have a specialised requirement not satisfied by Web Storage.

### Extracting Binary Resources

You will sometimes want to extract binary data from a server so that it can be retained locally. You can download binary files very easily with data type improvements made to XMLHttpRequest 2. See [Fetching data](http://www.html5rocks.com/tutorials/file/xhr2/#toc-bin-data) for more information.

Note that this isn't specifically about offline technologies, but is a common task that will come up when you're using them. The section below explains how you can store binary data once you've read it.

### Storing Binary Data

You can store binary data directly or you can convert it to plain text. For direct binary storage, you can either use a Web SQL Database with a column of "BLOB" type or the File Writer API. Alternatively, you can convert the binary content to plain text using a binary encoding technique. The obvious choice is Base 64, since that's the format commonly used on the net and in HTML5, i.e., it's supported by browsers via data: URIs. When you read back your base64-encoded content, you'll find that you can include it in your web app using a data URI, e.g., `image.src = "data:image/jpg;base64," + base64data`.

Unfortunately, base64 encoding can be quite slow, so use the techniques described in the next section to ensure the system stays responsive to user events. Alternatively, it might be worthwhile exposing base64-encoded representations right on your server, so your app can download them and directly store them. It will take up a little more space, to the tune of [around 30%](http://www.phpied.com/uncompressed-data-in-base64-probably-not/), but the UI will run faster.

### Ensuring the Application Runs Smoothly

When dealing with large amounts of data, there's a risk that your JavaScript will get so busy processing data it won't devote any time to the user interface. JavaScript is fundamentally single-threaded, meaning that only one thing happens at a time. If the user clicks a button, for instance, and the system is engaged in a long data activity, the click event will linger on a queue for several seconds and the user will be dismayed. Even longer delays will likely lead to the browser opening a dialog box asking the user if they want to stop the script. Best avoided.

Assuming you can't (or don't want to) reduce the amount of data you're storing, the most important thing you can do is exploit asynchronous APIs. With these APIs, the browser will automatically create a new thread for you, do the work, and then return results back to the main thread. While the other thread is doing the work, your user-interface will keep chugging along nicely in the main thread. If you've used XMLHttpRequest before, you already know that it's almost always used in asynchronous mode, so you should do that for any Ajax calls. As for storage, most but not all of the APIs have asynchronous modes. LocalStorage is the exception; it's only synchronous, so large quantities of data I/O may slow things down. Web SQL Database, IndexedDB, and File Writer all have both synchronous and asynchronous modes. You should generally favour asynchronous mode, even if it makes the programming model more complex.

The other way to do things asynchronously is to use [WebWorkers](http://www.html5rocks.com/tutorials/workers/basics/), a way to introduce new threads into your JavaScript, with your own code running in the derivative thread. However, there are some major limitations; the storage APIs generally won't work inside a Worker thread, and messages passed in and out of Workers can take a long time. I've found transferring several MB to and from a worker will take several seconds and lock up the user interface. So only use WebWorkers if you can't achieve the same thing with an aysnchronous storage call. The situation will improve as more browsers support SharedWorkers, which have fewer limitations, though more complexity for the developer to deal with.

### Handling Simultaneous Data Opertations

We noted earlier that Web Storage doesn't support transactions, so if you're using it, you have several choices: prevent multiple clients, use locking, design around it, or hope for the best! The last choice is certainly viable, but not for robust web apps. The first choice has been attempted many times, with various tricks used to constrain an app to a single window, but somehow goes against the grain of the web. Locking is more feasible, and hopefully libraries will evolve to support this pattern. Designing around it is also possible, as evidenced by various "NOSQL" frameworks for server-side applications and elsewhere. For example, in some circumstances, you might be able to just keep appending info instead of replacing it (and periodically removing old data).

A simpler solution, in many cases, will be to use transactions, as supported by Web SQL Database and (in the future) IndexedDB.

### Storing Large Amounts of Data

If you are looking to store many Megabytes or more, beware that there are limits in place, which are handled in different ways depending on the browser and the particular API. In most cases, there is a magic number of 5MB. For Application Cache and the various offline stores, there will be no problem if your domain stores less than 5MB. When you go above that, several things can happen: (a) it won't work; (b) the browser will ask the user for more space; (c) the browser will check for special configuration (as with the "unlimited\_storage" permission in the Chrome extension manifest). In the case of Chrome, extensions can request certain permissions, including "unlimited\_storage".

### Detecting if You're Online

There's an HTML5 API to let you query if a browser is online: `navigator.onLine()`. You can also listen for these online/offline events using `document.body.addEventListener("online", function () {...})` and `document.body.addEventListener("offline", function () {...})`.

You should generally assume the network is present and make calls as normal. It's only in the event of a server timeout or related error that you should invoke `navigator.online`. Doing so will serve two purposes: (a) you can decide if the error is caused by a network outage versus a server-specific outage, and if it's a network outage, inform the user so they can get back online; (b) you can start watching for the "online" event, and take action when the user is back online.

### Structuring File Data

The Filsystem API is designed for this use case. However, it is currently not supported everywhere. Alternatives include IndexedDB and Web SQL Database, which support structured data and queries against those structures. The general guideline would be to use one of those if you're in need of complex queries. But what if you need to store file data? You can use the BLOB type of Web SQL Database, but it's not intended for very large data items and it won't work on all browsers.

### Ensuring Cross-Browser Compatibility

As you've probably noticed by now, storage support varies widely across the different browsers. If that's true for the latest versions of each browser, imagine the differences that arise when you consider older versions too. To handle this, you're best off creating—or reusing—a common storage abstraction with calls such as `store.save(id, data)` and `store.findByIDs()`. An example of an open-source abstraction like this is [persist-js](http://github.com/jeremydurham/persist-js). An abstraction should determine which storage APIs are available (possibly using the [Modernizr](http://www.modernizr.com/)) API and then access the store using that API. This will help keep your library portable.

### Protecting Against Lost Data

Offline data is best used for caching content, rather than being the primary placeholder for user content. Browsers generally let users delete local storage, and there's a strong risk that some users will do so without realising the consequences. Thus, ensure data is frequently synchronised to the server, preferably in an automated fashion.

### Securing Offline Data

As [Nicholas Zakas has pointed out](http://www.nczonline.net/blog/2010/04/13/towards-more-secure-client-side-data-storage/), a risk with offline storage is that users sometimes share the same browser. This may not be true with mobile browsers, but it's certainly true in many family homes and, scarily, more true in the case of internet cafes. There's a big risk of sensitive data being available to other users. They may not even be malicious users; they might just visit the site as someone else, only to find all of the previous user's locally stored data in front of them.

A good compromise may be to use the LocalStorage variant, SessionStorage, which deletes data when the window is closed. However, even this is not guaranteed to happen when a user leaves, and sessionStorage partially defeats the purpose of offline storage anyway. Zakas proposes encrypting any sensitive data before storing it locally, though it remains to be seen if this will become a common practice among developers. There's a counter-argument that users can encrypt their own file system separately (as happens with many corporate systems), and that users who leave other data on their hard drive, e.g., cookies and regular data files, are already at significant risk.

For now, use offline storage for caching public data and perhaps other data of a general nature, e.g., an e-book the user has paid to download. For more sensitive data, you should consider the usage context and the nature of the data; sometimes it will make sense to store it offline, sometimes not.

## Summary

Offline storage has many potential applications well beyond the obvious "I want my application to run when users are on a plane" scenario. Developers in the past had to resort to workarounds, plugins, or browser-specific APIs, but modern developers have a veritable arsenal of standards-based capabilities to leverage. The challenge is to decide which to use when, and to use them in the right way. Hopefully, this article has been helpful in guiding your decision process.

## Further Reading

[HTML5Rocks](http://html5rocks.com) has resources on offline technologies in the [tutorials section](http://www.html5rocks.com/tutorials/), where you can get hands-on with code examples.
