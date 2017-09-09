---
layout: page
title: NuGet
---
{% include JB/setup %}

<section>
    <h2><strong>//</strong> NuGet Blog &amp; Tweets</h2>

    <div class="row">

        <div class="col-md-12">

            <div class="list-group">
                <a href="https://blog.nuget.org" class="list-group-item active">
                    <h4 class="list-group-item-heading">NuGet Blog</h4>
                </a>
				
				{% for feedItem in site.data.NuGet.Data.Blog.FeedItems limit: 5 %}
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
                <a href="https://twitter.com/nuget" class="list-group-item active">
                    <h4 class="list-group-item-heading">@NuGet on Twitter</h4>
                </a>
				
				{% for tweetItem in site.data.NuGet.Data.Twitter.Tweets limit: 10 %}
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
    <h2><strong>//</strong> GitHub x</h2>

	<div class="row">
	<div class="col-md-12">

            <div class="list-group">
                <a href="https://github.com/NuGet/Announcements" class="list-group-item active">
                    <h4 class="list-group-item-heading">NuGet/Announcements</h4>
                </a>
				
				{% for eventItem in site.data.NuGet.Data.Announcements.Events limit: 10 %}
					{% include DisplayGitHubEvent.html eventItem=eventItem %}
				{% endfor %}
			</div>
        </div>
	</div>
	
    <div class="row">

        <div class="col-md-6">

            <div class="list-group">
                <a href="https://github.com/NuGet/Home" class="list-group-item active">
                    <h4 class="list-group-item-heading">NuGet/Home</h4>
                </a>
				
				{% for eventItem in site.data.NuGet.Data.Home.Events limit: 10 %}
				<a href="{{ eventItem.RelatedUrl }}" class="list-group-item">
                        		<h4 class="list-group-item-heading">
					{% if eventItem.Type == "PushEvent" %}
						<i class="fa fa-cloud-upload" aria-hidden="true"></i>
					{% endif %}
					{% if eventItem.Type == "PullRequestEvent" %}
						<i class="fa fa-code-fork" aria-hidden="true"></i>
					{% endif %}
					{% if eventItem.Type == "WatchEvent" %}
						<i class="fa fa-eye" aria-hidden="true"></i>
					{% endif %}
					{% if eventItem.Type == "IssuesEvent" %}
						<i class="fa fa-sticky-note-o" aria-hidden="true"></i>
					{% endif %}
					{% if eventItem.Type == "IssueCommentEvent" %}
						<i class="fa fa-commenting" aria-hidden="true"></i>
					{% endif %}
					{% if eventItem.Type == "PullRequestReviewCommentEvent" %}
						<i class="fa fa-commenting" aria-hidden="true"></i>
					{% endif %}
					{% if eventItem.Type == "CreateEvent" %}
						<i class="fa fa-plus" aria-hidden="true"></i>
					{% endif %}
					{% if eventItem.Type == "DeleteEvent" %}
						<i class="fa fa-minus" aria-hidden="true"></i>
					{% endif %}
					{% if eventItem.Type == "ForkEvent" %}
						<i class="fa fa-code-fork" aria-hidden="true"></i>
					{% endif %}
					
					{{ eventItem.RelatedDescription }}
					
					</h4>
                        		<p class="list-group-item-text">
                            			on {{ eventItem.CreatedAt | date_to_long_string }} by {{ eventItem.Actor }}
                        		</p>
                    		</a>
				{% endfor %}
			</div>
        </div>
        
        <div class="col-md-6">

            <div class="list-group">
                <a href="https://github.com/NuGet/NuGetGallery" class="list-group-item active">
                    <h4 class="list-group-item-heading">NuGet/NuGetGallery</h4>
                </a>
				
				{% for eventItem in site.data.NuGet.Data.Gallery.Events limit: 10 %}
				<a href="{{ eventItem.RelatedUrl }}" class="list-group-item">
                        		<h4 class="list-group-item-heading">
					{% if eventItem.Type == "PushEvent" %}
						<i class="fa fa-cloud-upload" aria-hidden="true"></i>
					{% endif %}
					{% if eventItem.Type == "PullRequestEvent" %}
						<i class="fa fa-code-fork" aria-hidden="true"></i>
					{% endif %}
					{% if eventItem.Type == "WatchEvent" %}
						<i class="fa fa-eye" aria-hidden="true"></i>
					{% endif %}
					{% if eventItem.Type == "IssuesEvent" %}
						<i class="fa fa-sticky-note-o" aria-hidden="true"></i>
					{% endif %}
					{% if eventItem.Type == "IssueCommentEvent" %}
						<i class="fa fa-commenting" aria-hidden="true"></i>
					{% endif %}
					{% if eventItem.Type == "PullRequestReviewCommentEvent" %}
						<i class="fa fa-commenting" aria-hidden="true"></i>
					{% endif %}
					{% if eventItem.Type == "CreateEvent" %}
						<i class="fa fa-plus" aria-hidden="true"></i>
					{% endif %}
					{% if eventItem.Type == "DeleteEvent" %}
						<i class="fa fa-minus" aria-hidden="true"></i>
					{% endif %}
					{% if eventItem.Type == "ForkEvent" %}
						<i class="fa fa-code-fork" aria-hidden="true"></i>
					{% endif %}
					
					{{ eventItem.RelatedDescription }}
					
					</h4>
                        		<p class="list-group-item-text">
                            			on {{ eventItem.CreatedAt | date_to_long_string }} by {{ eventItem.Actor }}
                        		</p>
                    		</a>
				{% endfor %}
			</div>
        </div>
    </div>
</section>










