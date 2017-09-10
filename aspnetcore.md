---
layout: page
title: ASP.NET Core
---
{% include JB/setup %}

<section>
    <h2><strong>//</strong> ASP.NET Blog &amp; Tweets</h2>

    <div class="row">

        <div class="col-md-12">

            <div class="list-group">
                <a href="https://blogs.msdn.microsoft.com/webdev" class="list-group-item active">
                    <h4 class="list-group-item-heading">.NET Web Development and Tools Blog</h4>
                </a>
				
				{% for feedItem in site.data.AspNetCore.Data.Blog.FeedItems limit: 5 %}
					<a href="{{ feedItem.Href }}" class="list-group-item">
                        <h4 class="list-group-item-heading">{{ feedItem.Title }}</h4>
                        <p class="list-group-item-text">
                            Published on {{ feedItem.PublishedOn | date_to_long_string }}
                        </p>
                    </a>
				{% endfor %}
            </div>
        </div>
		
		
    </div>
	
	<div class="row"> 
        <div class="col-md-12">
            <div class="list-group">
                <a href="https://twitter.com/aspnet" class="list-group-item active">
                    <h4 class="list-group-item-heading">@aspnet on Twitter</h4>
                </a>
				
				{% for tweetItem in site.data.AspNetCore.Data.Twitter.Tweets limit: 10 %}
					<a href="https://twitter.com/{{ tweetItem.UserScreenname }}/status/{{ tweetItem.Id }}" class="list-group-item">
                        <h4 class="list-group-item-heading">{{ tweetItem.Text }}</h4>
                        <p class="list-group-item-text">
                            @{{ tweetItem.UserScreenname }} | Published on {{ tweetItem.CreatedAt | date_to_long_string }}
                        </p>
                    </a>
				{% endfor %}
            </div>
        </div>
	</div>
	
</section>

<section>
    <h2><strong>//</strong> GitHub</h2>

	<div class="row">
	<div class="col-md-12">

            <div class="list-group">
                <a href="https://github.com/aspnet/Announcements" class="list-group-item active">
                    <h4 class="list-group-item-heading">aspnet/Announcements</h4>
                </a>
				
				{% for eventItem in site.data.AspNetCore.Data.Announcements.Events limit: 10 %}
					{% include DisplayGitHubEvent.html eventItem=eventItem %}
				{% endfor %}
			</div>
        </div>
		
		<div class="col-md-6">

            <div class="list-group">
                <a href="https://github.com/aspnet/Home" class="list-group-item active">
                    <h4 class="list-group-item-heading">aspnet/Home</h4>
                </a>
				
				{% for eventItem in site.data.AspNetCore.Data.Home.Events limit: 10 %}
					{% include DisplayGitHubEvent.html eventItem=eventItem %}
				{% endfor %}
			</div>
        </div>
	</div>
	
    <div class="row">
	
	<ul class="nav nav-tabs">
  <li class="active"><a data-toggle="tab" href="#home">Home</a></li>
  <li><a data-toggle="tab" href="#menu1">Menu 1</a></li>
  <li><a data-toggle="tab" href="#menu2">Menu 2</a></li>
</ul>

<div class="tab-content">
  <div id="home" class="tab-pane fade in active">
    <h3>HOME</h3>
    <p>Some content.</p>
  </div>
  <div id="menu1" class="tab-pane fade">
    <h3>Menu 1</h3>
    <p>Some content in menu 1.</p>
  </div>
  <div id="menu2" class="tab-pane fade">
    <h3>Menu 2</h3>
    <p>Some content in menu 2.</p>
  </div>
</div>
    </div>
</section>










