---
layout: post
author: Erwin
title: "Python Timetable Parser"
tag: Project
image: /img/blog/python_timetable_parser/python_timetable_parser.png
image_high: /img/blog/python_timetable_parser/python_timetable_parser_full.png
---

##### Problem statement...
The fact that there is no way to export the timetable of my lectures and tutorials in an .ics file which i can import to my calendar and sync to all of my devices really ruffles my feathers. I would resort on typing all of the timetables manually, since I am an organised person who prefers everything to be in my calendar in lieu of having everything "screenshot-ed"! I often lose track of the pictures i take, so I would normally put important dates and tasks on my calendar and Todoist (I will talk more about this awesome productivity app in the future blog).

##### Eureka! Moment
During my short-three-weeks break, I attempted to automate this tedious process by writing my very first python script. I have self-studied Python for the past 1 month and reading the textbook without doing any concrete project is, frankly speaking, very mundane! Here comes the Eureka moment! I have just thought of a problem that I could solve while teaching myself python.

##### Technical details
Caveat: It is going to be a bit technical from here onwards. For those of you who are interested in the technicalities, by all means you may continue reading this post.

{% if site.url != "http://localhost:4000" %}
<img src="{{ "/img/blog/python_timetable_parser/image1.png" | prepend: site.baseurl | prepend: site.github_repository | prepend: "/" | prepend: site.url }}"width="400" alt="Screenshot of a terminal output" class="image-center" />
{% else %}
<img src="/img/blog/python_timetable_parser/image1.png" width="400" alt="Screenshot of a terminal output" class="image-center" />
{% endif %}

##### I picked up Python!
I tried to search for a library that is able to parse HTML tags in Python. Alas! I found BeautifulSoup4 that works impeccably in parsing HTML tags. The learning curve wasn't that steep because I have a foundation in C, C++, PHP, and Java. I spent one last week of my holiday coding this script from scratch. Frankly, there is this sense of achievement when i completed my script and started sharing it with my friends. 

##### How it works?
Firstly, this is the menu that the script will prompt you once you run the python script. It will search through your current working directory recursively for all of the HTML files. You will subsequently need to enter the file that contains the particular timetable you want to extract. For this demonstration, I am going to choose the first one.

After processing it, it will show you some key information such as: the subjects that it has successfully extracted, the number of lectures and tutorials for that subject, and the lecturer and the tutorial lecturer for that particular subject.

Frankly, I would like to say that BeautifulSoup4 is very well documented. I didn't have any difficulties navigating the online documents. Although, I would highly encourage you to read up about HTML before even attempting to use BeautifulSoup. You must what are 'id' and 'class' in bare minimum.

Upon surmounting BeautifulSoup, I had to start dabbling on the .ics file format. I would like to point out that the documentation of the iCalendar format (ics) is really poorly documented. I had to learn the syntax through trials and errors, since there is no crystal-clear documentation on iCalendar. 

##### Conclusion
The best way to pick up a programming language is by doing a project! Please do persevere no matter how hard it is. Trust me, it is going to be rewarding! If you are interested, you can look at my codes on [Github](https://github.com/erwinleonardy/Visual-Cryptography).

<div class="container">
	<div class="row">
		<div class="col-sm-12 col-md-12 portfolio-block">
			<div class="owl-carousel portfolio-page-carousel">
				<div class="item">
					<img src="/img/blog/python_timetable_parser/image2.png" alt="Screenshot of a terminal output" height="420" />
				</div>
				<div class="item">
					<img src="/img/blog/python_timetable_parser/image3.png" alt="Screenshot of a terminal output" height="420"/>
				</div>
			</div>
			{% if site.url != "http://localhost:4000" %}
				<script src="{{ "/js/jquery-2.1.3.min.js" | prepend: site.baseurl | prepend: site.github_repository | prepend: "/" | prepend: site.url }}"></script>
				<script src="{{ "/js/imagesloaded.pkgd.min.js" | prepend: site.baseurl | prepend: site.github_repository | prepend: "/" | prepend: site.url }}"></script>
				<script src="{{ "/js/owl.carousel.min.js" | prepend: site.baseurl | prepend: site.github_repository | prepend: "/" | prepend: site.url }}"></script>
			{% else %}
				<script src="/js/jquery-2.1.3.min.js"></script>
				<script src="/js/imagesloaded.pkgd.min.js"></script>
				<script src='/js/owl.carousel.min.js'></script>
			{% endif %}
			<script type="text/javascript">
				jQuery(document).ready(function($){
					$('.portfolio-page-carousel').imagesLoaded(function(){
						$('.portfolio-page-carousel').owlCarousel({
							smartSpeed:1200,
							items: 1,
							loop: true,
							dots: true,
							nav: true,
							navText: false,
							margin: 10,
							autoHeight:true
						});
					});
				});
			</script>
		</div>
	</div>
</div>