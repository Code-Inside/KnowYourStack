--- 
layout: page 
title: All KnowYourStack Pages
--- 
{% include JB/setup %}

<section>
    <div class="row">
    <div class="col-md-12">
      <div class="list-group">
      {% assign stackPages = site.pages | where: "type", "stack" %} 
      {% for page in stackPages %}
                <a href="{{page.url}}" class="list-group-item">{{page.title}}</a> 
      {% endfor %}
      </div>
      
      <div class="btn-group btn-block ">
      <a href="{{ site.github_repo_url }}issues/new" class="btn btn-primary">
        <i class="fa fa-fork" aria-hidden="true"></i> Add your own stack
      </a>
      </div>
    </div>
    </div>

</section>
