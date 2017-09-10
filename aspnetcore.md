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
		
		<div class="col-md-12">

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
	
	<ul class="nav nav-tabs">
		<li class="active"><a data-toggle="tab" href="#Mvc">Mvc</a></li>
		<li><a data-toggle="tab" href="#Razor">Razor</a></li>
		<li><a data-toggle="tab" href="#SignalR">SignalR</a></li>
		<li><a data-toggle="tab" href="#Identity">Identity</a></li>
		<li><a data-toggle="tab" href="#Kestrel">Kestrel</a></li>
	</ul>
	
	<div class="tab-content">
		<div id="Mvc" class="tab-pane fade in active">
			<h3>Mvc</h3>
			<div class="list-group">
                <a href="https://github.com/aspnet/Mvc" class="list-group-item active">
                    <h4 class="list-group-item-heading">aspnet/Mvc</h4>
                </a>
				
				{% for eventItem in site.data.AspNetCore.Data.Mvc.Events limit: 10 %}
					{% include DisplayGitHubEvent.html eventItem=eventItem %}
				{% endfor %}
			</div>
		</div>
		<div id="Razor" class="tab-pane fade in">
			<h3>Razor</h3>
			<div class="list-group">
                <a href="https://github.com/aspnet/Razor" class="list-group-item active">
                    <h4 class="list-group-item-heading">aspnet/Razor</h4>
                </a>
				
				{% for eventItem in site.data.AspNetCore.Data.Razor.Events limit: 10 %}
					{% include DisplayGitHubEvent.html eventItem=eventItem %}
				{% endfor %}
			</div>
		</div>
		<div id="SignalR" class="tab-pane fade in">
			<h3>SignalR</h3>
			<div class="list-group">
                <a href="https://github.com/aspnet/SignalR" class="list-group-item active">
                    <h4 class="list-group-item-heading">aspnet/SignalR</h4>
                </a>
				
				{% for eventItem in site.data.AspNetCore.Data.SignalR.Events limit: 10 %}
					{% include DisplayGitHubEvent.html eventItem=eventItem %}
				{% endfor %}
			</div>
		</div>
		<div id="Identity" class="tab-pane fade in">
			<h3>Identity</h3>
			<div class="list-group">
                <a href="https://github.com/aspnet/Identity" class="list-group-item active">
                    <h4 class="list-group-item-heading">aspnet/Identity</h4>
                </a>
				
				{% for eventItem in site.data.AspNetCore.Data.Identity.Events limit: 10 %}
					{% include DisplayGitHubEvent.html eventItem=eventItem %}
				{% endfor %}
			</div>
		</div>
		<div id="Kestrel" class="tab-pane fade in">
			<h3>Kestrel</h3>
			<div class="list-group">
                <a href="https://github.com/aspnet/KestrelHttpServer" class="list-group-item active">
                    <h4 class="list-group-item-heading">aspnet/KestrelHttpServer</h4>
                </a>
				
				{% for eventItem in site.data.AspNetCore.Data.Kestrel.Events limit: 10 %}
					{% include DisplayGitHubEvent.html eventItem=eventItem %}
				{% endfor %}
			</div>
		</div>
	</div>
</section>