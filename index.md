---
layout: page
---
{% include JB/setup %}

<section>
    <h2><strong>//</strong> All KnowYourStack Pages</h2>

	<div class="row">

        <div class="col-md-12">

		<div class="list-group">
			{% assign stackPages = site.pages | where: "type", "stack" %}
			{% for page in stackPages %}
			<a href="{{page.url}}" class="list-group-item">{{page.title}}</a>
			{% endfor %}
		</div>
		
    </div>
	
	
</section>

