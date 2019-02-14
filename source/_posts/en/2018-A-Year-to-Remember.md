---
title: '2018: A Year to Remember'
lang: en
direction: ltr
date: 2018-12-20 18:37:36
tags:
	- al-tameer
	- raban al-safina
	- tatweer
	- odoo
	- flutter
	- turkey
	
---


When I look 12 months back, I see Odoo, Flutter and Turkey. In this 2018 review, I'll talk of each technology I worked with, instead of categorizing it chronologically as months.

I'll call it Odoo and Flutter year.


### <div><span style="float: left">Restaurant's Menu</span><span style="float: right; margin-top: -2px;">{% raw %}<a href="https://play.google.com/store/apps/details?id=com.tatweer.emenu" style="display:inline-block;overflow:hidden;background:url(https://play.google.com/intl/en_us/badges/images/generic/en_badge_web_generic.png) no-repeat;width:85px;height:50px;background-size: contain;"></a>{% endraw %}</span></div>
<br><br>


It was my first task and project for _Tatweer_, the company that I'll work with part-time for the rest of the year. My task was to create an app for restaurant's menu, and it should and must be different, i.e., _creative_, to a degree that our product manager would say _"cool"_. At the same time, I was also going to the gym, and was thinking about the app during workouts. 
In order to start imagining what the app would be, I should inspire my self from app designs UIs, whether from Dribbble or Pinterest, and try to create a mixture from what've seen and learned. I remember, I was programming and playing for a week just to make sure a RecyclerView's layout to behave of whats inside my mind.


Two weeks later, and only about one day before I start programming it, I got an insight of what to do, from colors, transitions and animations and general app layouts. The problem is not with programming, but what functions and UIs to do _exactly_. With the skills I learned in the previews years, and using the power of Kotlin, this app was created, named EMenu, an app that shows food and dishes menu for restaurants so that customers browse them with a tablet. It was really good app for my own interest, because, within a short time, it is possilble for an app with high-quality design can be build. Most importantly, I returned to mobile app development after more than 4 months didn't create an app (due to my work with Odoo (customization) in Al-Tameer, that I'll describe next section). I hope you like the following screenshots and _videoshots_ of the it.

<br>

{% img /2018-a-year-to-remember/emenu-android/emenu-android-foods-home.png 250 Emenu: Foods home %}
{% img /2018-a-year-to-remember/emenu-android/emenu-android-foods-sidemenu.png 250 Emenu: Foods side-menu %}
{% img /2018-a-year-to-remember/emenu-android/emenu-android-dishes.png 250 Emenu: Dishes %}
{% img /2018-a-year-to-remember/emenu-android/emenu-android-dishes-no-order.png 250 Emenu: Dishes with no order functionality %}

<video width="250" controls>
    <source src="/2018-a-year-to-remember/emenu-android/emenu-android-demo.mp4"  type="video/mp4">
	<p>Your browser does not support H.264/MP4.</p>
</video>

<br>

## Odoo


It all begins when a university wanted to apply an ERP, and they selected Odoo among other ERPs. I applied for Al-Tameer to work as an iOS developer, but, ended up working with Odoo customization 😁. They're very far fields, but, since I know Python from my MSc degree, where research project was written with Python, I said let's see what is Odoo. I didn't quit the job, because they provided very good residence for employees outside of Baghdad, and Iraq. And, I thought I should work part-time after my full-time and continue my passion with mobile app development. That is to say, Odoo in full-time and mobile apps development in part-time.
In order to apply Odoo there, the university insisted on using Odoo Enterprise, and the customization and support should be managed by Odoo folks themselves. I didn't agree, and suggested to use the free and open-source version of Odoo, and will customize it according to their needs. They didn't agree with me about it, and as a solution, they asked us (Al-Tameer) to apply it first at our company, and when succeeded, it will be applied at their university.


Odoo customization, to be honest, is not easy. Some tasks might took days, even weeks, to finish, due to the bizarre nature of how to develop a plug-in for Odoo and the lack or existence of poor documentation. It is awkward and cumbersome; pain with tears to see the results.

I thank sincerely, our project manager, Nooruldeen, for his continues persistence gathering requirements from the HR and financial departments. Every time, he came with what is required to start applying Odoo. 
What the HR wanted is to export a summary report containing the total hours of leaves requests and delays for each employee according to his/her working hours. At that time, the employees were using [CakeHR](https://cake.hr) to apply leave request, and it was my task to migrate leave requests from CakeHR to Odoo.

### Flask

There was some small Flask project I developed for acting as a back-end that communicates with Odoo using JSON-RPC. I used this Flask project, so that, for any client, mobile or Web, can communicate with Flask, instead of directly with Odoo. Why? because the client communicates with the back-end much easily as a RESTful API than with JSON-RPC.

<center>
{% img /2018-a-year-to-remember/odoo/altameer-flask-json-rpc-odoo.png 300 How a client (mobile or a web) connects with Odoo using Flask as a back-end (RESTful API) %}
</center>


I continued developing this Flask back-end so that it accept leave requests, from a bot (script) that syncs all CakeHR leaves to Odoo using RESTful API from Flask. I was really happy when I saw all of the employees leaves are imported from CakeHR to the Leaves Dashboard of Odoo.

<br>

<center>
	{% img /2018-a-year-to-remember/odoo/odoo-employee-leaves-dashboard.png 600 Leaves Dashboard in Odoo %}
</center>

### XLSX Reports

So, the HR departent wanted a summary of the selected departments, that prints employees attendance, absence, delays, and their leave requests.
I thought it was trivial, and I was wrong. It took me more than two months to produce correct numbers about this summary. The main algorithm was planted in Odoo, and testing and seeing the results or calculations was _painful_ (as I mentioned how Odoo development is clumsy). The following screenshots shows how this is done and what are its results.

 <br>
{% img /2018-a-year-to-remember/odoo/odoo-print-xlsx-summary-leaves-report-full.png 600 Printing XLSX summary report for attendance and leaves in Odoo for a specified period %}
<br>

When _PRINT SPREADSHEET_ button is clicked, it produces the HR attendance summary, an XLSX downloadable file, as shown below.
<br>
{% img /2018-a-year-to-remember/odoo/hr-attendance-summary-xlsx.png 600 Attendance and Leaves Summary XLSX Report %}
<br>

### Salary Calculations

The finance department wanted to calculate employees pay-slips based on the HR summary report (XLSX sheet) automatically, according to their salary calculation formula. After _customizing_ the pay-slip calculations, and configuring the salary structure and rules, I finally reached the desired result, shown below. And, I repeat, it was also not a trivial task (I remember about two weeks to get things working like this).

<br>
{% img /2018-a-year-to-remember/odoo/salary-caclculaton-sheet-odoo.png 600 Salary calculation sheet in Odoo %}
<br>




### Docker


Since Raban Al-Safina is a group of companies, meaning that there will be more than a branch where Odoo will be applied. I have a very basic knowledge of what Dockerization is, and I thought it would be better if applied here to Odoo for each branch. I spent sometime playing with Docker and then building Odoo and Postgresql images. In the end, and for each branch, it is now very easy to build a branch container, specifying its parameters and everything will be Ok. Docker saved me lots of time, setup (configuration), and _memory_.

<br>

{% img /2018-a-year-to-remember/odoo/altameer-odoo-dockers.png 600 Odoo dockers for AlTameerHR %}





### Email Summary Reports

What if the employee receives a weekly report of his/her attendance summary? not a bad idea. 
Before the HR summary report being submitted to the financial department at the end of the month, for every week, the employee gets an email with all of his/her delays, check-ins and check-outs, and leaves, in order to verify that these data are valid, and if there are any errors or mistakes, he/she will contact the HR department and explain the issue. The process of sending the HR summary to the _selected_ employees is done _manually_ (using AlTameerHR app, discussed below) by the HR manager. This is my HR summary from 24/11/2018 to 02/12/2018. Any date range can be specified.

<br>

{% img /2018-a-year-to-remember/odoo/my-altameer-hr-attendance-and-leaves-summary-mail-1.png 295 My Al-tameer HR Attendance and Leaves Summary Report on Mail %}
{% img /2018-a-year-to-remember/odoo/my-altameer-hr-attendance-and-leaves-summary-mail-2.png 295 My Al-tameer HR Attendance and Leaves Summary Report on Mail %}





### Telegram Bot

I didn't want to skip mentioning this tiny little Telegram bot. It logs some cron job tasks that done automatically, e.g., syncing FingerTec checks daily.
<br>
<center>
{% img /2018-a-year-to-remember/odoo/al-tameer-odoo-telegram-bot.png 200 Al-Tameer Odoo Telegram Bot %}
</center>

### Notes

Luckily, most of the time I wrote the tasks using [Things](https://culturedcode.com/things/). The detailed tasks of this project are listed in the following screenshots from Things (it is not an _exact_ list of tasks done, there are some that I didn't write and was easy to remember and done easily).

{% img /2018-a-year-to-remember/odoo/tasks-finished-altameer-odoo-altameerhrapp--5.png 295 Task finished in Al-Tameer for Odoo and AlTameerHR mobile app %}
{% img /2018-a-year-to-remember/odoo/tasks-finished-altameer-odoo-altameerhrapp--4.png 295 Task finished in Al-Tameer for Odoo and AlTameerHR mobile app %}
{% img /2018-a-year-to-remember/odoo/tasks-finished-altameer-odoo-altameerhrapp--3.png 295 Task finished in Al-Tameer for Odoo and AlTameerHR mobile app %}
{% img /2018-a-year-to-remember/odoo/tasks-finished-altameer-odoo-altameerhrapp--2.png 295 Task finished in Al-Tameer for Odoo and AlTameerHR mobile app %}
{% img /2018-a-year-to-remember/odoo/tasks-finished-altameer-odoo-altameerhrapp--1.png 295 Task finished in Al-Tameer for Odoo and AlTameerHR mobile app %}




## Flutter
### How I got hooked

You can not imagine how much I am proponent against cross-platform mobile frameworks, like ReactNative, Xamarin, Cordova or PhoneGap. Luckily, I have a friend ([Mustafa](https://www.facebook.com/mustafa1024m)) who always suggests cutting-edge technologies to try with. So one day (in March or April, 2018) he told me to try [Flutter](https://www.flutter.io), and I (between me and my self) refused and was against this or any cross-platform technology. But, one day, while I was working part-time with @Tatweer, one of our clients (GK Auto, a Hyundai agent in Iraq) wanted high-quality app for both Android and iOS, and within a month or less 🤔.
So, the  challenge was to how do it within this time-frame. And, I don't want to to repeat the two-brains-ache for developing Android in Kotlin and iOS with Swift. I wanted to see practical and _beautiful_ solution. I tried ReactNative before, and was not at all satisfied with its UI and programming with JavaScript and the bridge thing. 
So, I remembered my friend tip: Try Flutter!. I installed the [Flutter Gallery Example](https://play.google.com/store/apps/details?id=io.flutter.demo.gallery), and I was fascinated by its smoothness and UI composition, and most importantly, how it handles RTL at best. The challenge began in May 2018, by learning Flutter and developing our client app within a month. Keep in mind, that I was working full-time (08:00-16:00) at Al-Tameer and working on Flutter at part-time (any four hours after 16:00, after my full-time).

### <div><span style="float: left">GK Auto - Hyundai</span><span style="float: right; margin-top: -4px;">{% raw %}<a href="https://play.google.com/store/apps/details?id=com.tatweer.hyundai" style="display:inline-block;overflow:hidden;background:url(https://play.google.com/intl/en_us/badges/images/generic/en_badge_web_generic.png) no-repeat;width:85px;height:50px;background-size: contain;"></a>{% endraw %}</span></div>
<br><br>

It is not the first time I build a mobile app, and learning Flutter the first time was (for me) not a completely new experience. 
It is the same concepts with Android and iOS, but now, with different language (Dart) and different component names. The learning curve was fast.
I built some prototypes to learn Flutter before starting with the Hyundai app. After about two weeks of consistent and hard working with Flutter, 
I got used with the framework and its philosophy. <br>


Next, are the screenshots and _videoshots_ of different phases during building my first production-level flutter app. The application is available on [Google Play](https://play.google.com/store/apps/details?id=com.tatweer.hyundai) (on AppStore, our client still keeping it on the _pending_ state).

<br>

{% img /2018-a-year-to-remember/hyundai/image-3D-rotation-in-Flutter.png 140 image 3D rotation in Flutter %}
{% img /2018-a-year-to-remember/hyundai/grid-flutter-arabic.png 140 Grid in Flutter (Arabic text) %}

<video width="140" controls>
    <source src="/2018-a-year-to-remember/hyundai/20180523_202059.mp4" type="video/mp4" />
</video>

<video width="140" controls>
    <source src="/2018-a-year-to-remember/hyundai/20180523_202157.mp4" type="video/mp4" />
</video>

<video width="140" controls>
    <source src="/2018-a-year-to-remember/hyundai/20180524_040859.mp4" type="video/mp4" />
</video>

<video width="140" controls>
    <source src="/2018-a-year-to-remember/hyundai/20180525_035427.mp4" type="video/mp4" />
</video>

<video width="140" controls>
    <source src="/2018-a-year-to-remember/hyundai/hyundai-app-car-info-page2.mp4" type="video/mp4" />
</video>

{% img /2018-a-year-to-remember/hyundai/hyundai-flutter-app-iq-4.png 140 Hyundai Flutter App - Iraq %}
{% img /2018-a-year-to-remember/hyundai/hyundai-flutter-app-iq-0.png 140 Hyundai Flutter App - Iraq %}
{% img /2018-a-year-to-remember/hyundai/hyundai-flutter-app-iq-1.png 140 Hyundai Flutter App - Iraq %}
{% img /2018-a-year-to-remember/hyundai/hyundai-flutter-app-iq-2.png 140 Hyundai Flutter App - Iraq %}
{% img /2018-a-year-to-remember/hyundai/hyundai-flutter-app-iq-3.png 140 Hyundai Flutter App - Iraq %}
{% img /2018-a-year-to-remember/hyundai/hyundai-flutter-app-iq-5.png 140 Hyundai Flutter App - Iraq %}
{% img /2018-a-year-to-remember/hyundai/hyundai-flutter-app-iq-6.png 140 Hyundai Flutter App - Iraq %}
{% img /2018-a-year-to-remember/hyundai/hyundai-flutter-app-iq-7.png 140 Hyundai Flutter App - Iraq %}

<video width="140" controls>
    <source src="/2018-a-year-to-remember/hyundai/hyundai-rectangle-dots-zoomable.mp4" type="video/mp4" />
</video>

<br>

One of the early reasons convinced me to adopt Flutter was its handling of Arabic language (RTL) at best. As you can see from the shots above, the app is in Arabic and it was one of the requirement our client talked on.

The deadline of the project was a month, but, the development continues for three months. All of the design and ideas of the app was proposed by us. Our client wanted an app that represents their identity about vehicles they show and sell. Every detail, and every single step in the app was thoroughly discussed everyday, between me, and the back-end developer, Abdullah, and our product manager, Sadoon.

One thing to mention and not to forget about, is that, the work on this app was the toughest for me this year (2018). It was Ramadan (Our muslim's fasting month), and I remember I was staying awake the whole month till 04:00 at dawn, and then waking up to my work at 07:15, and luckily, our full-time reduced to 14:00 at this month. The routine continues days after Ramadan, and I still have the urge to stay up late to do my next Flutter project: A Tourism Demo App.



### <div><span style="float: left">Tourism Demo App</span><span style="float: right; margin-top: 4px">{% raw %}<a class="github-button" href="https://github.com/bluemix/tourism-demo" data-show-count="true" aria-label="Star bluemix/tourism-demo on GitHub">Star</a><script async defer src="https://buttons.github.io/buttons.js"></script>{% endraw %}</span></div>
<br><br>

It was Eid Al-Fitr (after Ramadan), and I wanted to build cutting-edge, beautiful, and fast. I wanted to build the best I can do with Flutter and then publishing it on GitHub. 

<br>


{% img /2018-a-year-to-remember/tourism/flutter-tourism-demo-400x300.gif 450 tourism-demo-flutter %}


{% img /2018-a-year-to-remember/tourism/squres-clippers-flutter1.png 150 tourism-demo-flutter %}
{% img /2018-a-year-to-remember/tourism/squres-clippers-flutter2.png 150 tourism-demo-flutter %}
{% img /2018-a-year-to-remember/tourism/squres-clippers-flutter3.png 150 tourism-demo-flutter %}

{% img /2018-a-year-to-remember/tourism/sc4.png 150 tourism-demo-flutter %}
{% img /2018-a-year-to-remember/tourism/sc2.png 150 tourism-demo-flutter %}
{% img /2018-a-year-to-remember/tourism/sc1.png 150 tourism-demo-flutter %}
{% img /2018-a-year-to-remember/tourism/sc3.png 150 tourism-demo-flutter %}


<video width="150" controls>
    <source src="/2018-a-year-to-remember/tourism/tourism-app-demo-4_2.mp4" type="video/mp4" />
</video>


<br>

I've published the app on [GitHub](https://github.com/bluemix/flutter-tourism-demo), and i hope people will like it more. It uses Redux, shows animations, internationalization (i18n), ClipPath, and fonts, among others. I focused on how to switch between Arabic and English in the app using Redux. It was really important for me, especially, I was really proud of it showing it in the Flutter time in Google I/O Extended - Baghdad.



### Google I/O 2018 Extended, Baghdad - Flutter

Probably, one of the best developers events happened in 2018 (July 13th) was this: Google I/O 2018 Extended in Baghdad, hosted by [d3 Studio](https://d3stud.io/) at [The Station](https://www.facebook.com/thestationiq/). It featured cutting-edge technologies, and luckily (and honored), I was a [speaker](https://www.facebook.com/GDGBaghdad/photos/a.129742190962410/250301902239771) about Flutter. 


<center>
 {% raw %}
  <iframe src="https://www.facebook.com/plugins/post.php?href=https%3A%2F%2Fwww.facebook.com%2FGDGBaghdad%2Fposts%2F250339478902680&width=500" width="500" height="556" style="border:none;overflow:hidden" scrolling="no" frameborder="0" allowTransparency="true" allow="encrypted-media"></iframe>
  
 {% endraw %}

	{% twitter https://twitter.com/SniperDW/status/1018041227776847872 %}
	{% twitter https://twitter.com/SniperDW/status/1017679319349460993 %}
	
</center>



I was kinda new to this framework, only two months early being working on it, heavily. I couldn't talk about the Hyundai project (it was a private project), and the only thing to show to them was the [Tourism Demo](https://github.com/bluemix/flutter-tourism-demo), which shows the capabilities Flutter is in terms of animations and i18n, among many other things. 
The challenge for me was how to show to the audience the difference between Flutter and ReactNative, and how Flutter has better app quality in terms of UI composition, smooth animations, and how Dart is compiled natively instead of using a JS bridge in ReactNative. Talk slides are [here](https://www.slideshare.net/AbdElmomenKadhim/google-io-2018-extended-baghdad-flutter). It was really a _thing_ for us, as developers, because it shows that we are up-to-date to current technologies and our region is not living in a separate world, and to encourage programmers here to rely and start developing cross-platform apps using Flutter, and most importantly, is to push the use of technological advancements at our area. I sincerely thank the organizers of this event 💛.



### <div><span style="float: left">AlTameerHR App</span><span style="float: right">{% raw %}<a href="https://itunes.apple.com/us/app/altameerhr/id1451702705?mt=8" style="display:inline-block;overflow:hidden;background:url(https://linkmaker.itunes.apple.com/en-us/badge-lrg.svg?releaseDate=2019-02-07&kind=iossoftware&bubble=ios_apps) no-repeat;width:75px;height:45px;background-size: contain;"></a><a href="https://play.google.com/store/apps/details?id=com.al_tameer.altameerhr" style="display:inline-block;overflow:hidden;background:url(https://play.google.com/intl/en_us/badges/images/generic/en_badge_web_generic.png) no-repeat;width:85px;height:50px;background-size: contain;"></a>{% endraw %}</span></div>
<br><br>

Up to that time, I was developing in Flutter without using specific architecture, which led the Hyundai app to become a mess for me, because as the app grows, lots of Widgets will be built and you'll lose focus of where part are you working now. 

Before I started my next production-level project, I needed to understand an architecture before jumping to code Flutter. [inKino](https://github.com/roughike/inKino) was my savior. I spent more than a week understanding the code and playing with it. The code was neat, well-thought, and beautiful. It used [Redux](https://github.com/brianegan/flutter_redux) for its architecture. 

<br>

{% img /2018-a-year-to-remember/altameer-hr/altameer-hr-flutter-english-ui-1.png 195 AlTameerHR App - English UI %}
{% img /2018-a-year-to-remember/altameer-hr/altameer-hr-flutter-english-ui-2.png 195 AlTameerHR App - English UI %}
{% img /2018-a-year-to-remember/altameer-hr/altameer-hr-flutter-english-ui-3.png 195 AlTameerHR App - English UI %}
{% img /2018-a-year-to-remember/altameer-hr/altameer-hr-flutter-english-ui-4.png 195 AlTameerHR App - English UI %}
{% img /2018-a-year-to-remember/altameer-hr/altameer-hr-flutter-english-ui-5.png 195 AlTameerHR App - English UI %}

<br>

{% img /2018-a-year-to-remember/altameer-hr/altameer-hr-flutter-arabic-ui-1.png 195 AlTameerHR App - Arabic UI %}
{% img /2018-a-year-to-remember/altameer-hr/altameer-hr-flutter-arabic-ui-5.png 195 AlTameerHR App - Arabic UI %}
{% img /2018-a-year-to-remember/altameer-hr/altameer-hr-flutter-arabic-ui-2.png 195 AlTameerHR App - Arabic UI %}
{% img /2018-a-year-to-remember/altameer-hr/altameer-hr-flutter-arabic-ui-4.png 195 AlTameerHR App - Arabic UI %}
{% img /2018-a-year-to-remember/altameer-hr/altameer-hr-flutter-arabic-ui-3.png 195 AlTameerHR App - Arabic UI %}

<br>

It is the first time I develop an app inspired by gradients and curved backgrounds. The challenge was how to create a beautiful HR application, but the problem was all I have was text-based data, e.g., check-ins and check-outs, attendance summary, leave requests, etc... and the only image available was the employee avatar picture. So, in order to add colors and shapes to the app, gradient buttons and gradient background is added, to contain the dullness of text-only data. 
The app is available on [Google Play](https://play.google.com/store/apps/details?id=com.al_tameer.altameerhr), and it was a struggle with iOS on the AppStore, because, kind of such apps developed specifically for employees requires Apple Developer Program for organizations, instead of publishing it under my own _personal_ account (I wanted to upload it to the AppStore, but failed in the review process, insisting this type of apps be outside of the app store or with an account for organizations).

### <div><span style="float: left">Gradient Screens </span><span style="float: right; margin-top: 4px">{% raw %}<a class="github-button" href="https://github.com/bluemix/Gradient-Screens" data-show-count="true" aria-label="Star bluemix/Gradient-Screens on GitHub">Star</a><script async defer src="https://buttons.github.io/buttons.js"></script>{% endraw %}</span></div>
<br><br>

Inspired by gradients from AlTameerHR app, I said why not creating pages contains gradients, whether buttons, cards, or texts. So, I started designing those screens with the intent of publishing them on GitHub. Some of the screens were my designs, other taken from other UI designers. Below are the repo and its screenshots.

<br>


{% img /2018-a-year-to-remember/gradient-screens/gradient_screen_arabic_text_flutter.png 195 Gradients Screen with Arabic text in Flutter %}
{% img /2018-a-year-to-remember/gradient-screens/intro_page.png 195 Gradients Screen with English text in Flutter %}
{% img /2018-a-year-to-remember/gradient-screens/info_page.png 195 Gradients Screen in Flutter %}
{% img /2018-a-year-to-remember/gradient-screens/login_page.png 195 Gradients Screens in Flutter %}
{% img /2018-a-year-to-remember/gradient-screens/genres_page.png 195 Gradients Screens in Flutter %}
{% img /2018-a-year-to-remember/gradient-screens/be_kind_page.png 195 Gradients Screens in Flutter %}
<br>


### <div><span style="float: left">Gradient Widgets</span><span style="float: right; margin-top: 4px">{% raw %}<a class="github-button" href="https://github.com/bluemix/gradient-widgets" data-show-count="true" aria-label="Star bluemix/gradient-widgets on GitHub">Star</a><script async defer src="https://buttons.github.io/buttons.js"></script>{% endraw %}</span></div>
<br><br>

The idea incepted from gradient-screens, by turning gradient widgets into a Dart package and publishing it on GitHub. 



<center>
{% img /2018-a-year-to-remember/gradient-widgets/gradient-widgets-flutter.png 260 Gradient Widgets in Flutter %}
</center>

Gradient progress was the longest one to develop. 

<center>
{% img /2018-a-year-to-remember/gradient-widgets/gradient_widgets_progress_demo.gif 400 Gradient Widgets in Flutter %}
</center>

I learned, I can publish the project when the main features are finished, and then continue enhancements later, otherwise, _I will never_ publish a project. 
Those days where really hard and amazing 🙏🏼. 





 
## BilWeekend to Sulaimaniya


After finishing _Strike a Pose_ screen at 02:00 AM, I should start going at 03:00 AM to the bus, where a trip to Sulaymaniyah for four days was waiting us (me and my sister and my little sister) with [BilWeekend](https://www.facebook.com/BilWeekend/posts/2260915274143666). It was the first time I go with my little sister on a trip. The trip includes hiking, camping and visitng Ahmed Awa's waterfalls. It was really enjoying experience. I was capturing photos using my Nikon D750, and 35mm f/1.4 Sigma ART lens only. Sure, I took lots of photos, and two of them got featured on [Pexels](https://www.pexels.com/@bluemix). 

<br>

{% raw %}
<iframe src="https://www.facebook.com/plugins/post.php?href=https%3A%2F%2Fwww.facebook.com%2Fbluemix%2Fposts%2F10216926348693269&width=500" width="500" height="728" style="border:none;overflow:hidden" scrolling="no" frameborder="0" allowTransparency="true" allow="encrypted-media"></iframe>
{% endraw %}
<br>

One of the surprises in the trip, is that, an iOS developer friend, was also going with us, [Husam](https://www.facebook.com/husamaamer.9), and a popular (or public-figure) photographer in Baghdad, [Ali DabDab](https://www.facebook.com/ALI.DAB.DAB11).

It was not the first time I go to Sulaymaniyah. This is my second time, and the first was on April 2018 with BilWeekend too, but was alone, and was cold, and I was shooting with 85mm Sigma ART lens. The following pictures (post) are taken from both of the trips. I hope you like them 🙂.

<br>
{% raw %}
<iframe src="https://www.facebook.com/plugins/post.php?href=https%3A%2F%2Fwww.facebook.com%2Fbluemix%2Fposts%2F10218297743177274&width=500" width="500" height="625" style="border:none;overflow:hidden" scrolling="no" frameborder="0" allowTransparency="true" allow="encrypted-media"></iframe>
{% endraw %}



## Turkey 🇹🇷


Istanbul was not just a city for me. It is a mix of different cultures and rife history, reflects to me how Turkey is a civilization, and we're (Iraq) behind them by at least 30 or 40 years, and I believe, it is not only better in terms of quality of life, but, the people's mindset is modern too. I admire their civil infrastructure, e.g., the roads, road sides, etc..., are built with care and very good finishing.
The people were kind, helpful and felt like it is a very good place to live. This level of advancements can't be achieved without honest, hard work to develop their country and their mindset.


Nikon D750, with 35mm Sigma ART was my companion. The whole 7 days (except for one night), I was shooting whenever I go, in cloudy, light or heavy rain, day and night. All of my best shots were published on [Pexels](https://www.pexels.com/@bluemix). I also post some of them on Facebook. They were my favorite shots till the time of this writing. Istanbul is beautiful, it is just like designed to be gorgeous from every angle you take picture. It was filled with details.

<br>
{% raw %}
<iframe src="https://www.facebook.com/plugins/post.php?href=https%3A%2F%2Fwww.facebook.com%2Fbluemix%2Fposts%2F10218728559667417&width=500" width="500" height="734" style="border:none;overflow:hidden" scrolling="no" frameborder="0" allowTransparency="true" allow="encrypted-media"></iframe>
{% endraw %}
<br>


I've used Uber and Google Maps, which really helped me to discover tourism attraction places, especially, Galata Tower (it was not on the trip schedule list to visit). The first time I use a power-bank, because, half the day I was with our guide to show us places, and the other half was free time, where I was discovering new places. The last two days I got really tired from walking long distances with my camera, and you get the feeling to return home, although, new places to discover are always coming to you, and 7 days are not enough to explore Istanbul.

<center>
{% img /2018-a-year-to-remember/turkey/turkey-walking-health-data.png 225 My average walking distance during the tour to Turkey  %}
</center>

<br>

My trip to Turkey is one of the check points in my life. I learned a lot from this country.

<br>

## December

I've got work breakdown with Al-Tameer. Everyday, I wake up going to work according to my mood. Some day I go at 10:00 and the other day is off. The reason I had this, because I had some management issues considering the registration of AlTameerHR iOS app, and they didn't care at all to proceed with the process or to cancel the whole project. For me, it ignites the temptation to quit. I don't see any work will be valued or being cared for here. I am wasting my time for the short and long-term with this company.

<center>
{% img /2018-a-year-to-remember/december/december2018-my-altameer-hr-smmary.png 225 My Al-Tameer HR Summary for December %}
</center>


I don't remember having any work breakdown. I was very eager to work and building stuff.  But, this breakdown, by having many days off and lots, lots of sleep (I even talked to my friend by calling December _the sleeping month_) changed my appreciation about work. I realized how work is a bless for us, as a human being. Life has no taste without feeling the joy in or after your hard work. I really valued (with grief) the days were I was doing great stuff (at least for me).



## Lots of Music

I measure how I am making a good, honest work, by having new music added to my [Music](https://www.apple.com/lae/music/). It is _crazy_, I know. But, the more new songs I listen, the more I am enjoying my work.

<br>
<center>
{% img /2018-a-year-to-remember/music/my-apple-music-songs.png 600 My Apple Music songs %}
</center>


## But Why?

So, 2018 was a prosperous year, and this can never done without persistence and hard work, and I am really glad that I wrote this article (although late). I wrote this article, because, I want to remember, 10 years from now, what I was doing. I want to get inspired by, at least I was doing things. I don't want those memories and work to fade.

> I hope, to use this knowledge and experience, in someday, _to change_.

