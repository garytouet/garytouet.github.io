---
layout: page
title: Archives
meta-title: Dive into the Archive!
permalink: /archives/
---



## Quick access
1. [Archive of all posts in reverse chronological order,](#all)
1. [Archive by year and month,](#months)
1. [Archive by category,](#categories)
1. [Subscribe to the RSS feed.](#feed)


<section id="all" class="archive_section">

<h2>All posts</h2>

<ul>
{% for post in site.posts %}
<li class="archive_item">
<a class="archive_permalink" href="{{ post.url }}" title="Permanent Link to {{ post.title }}">{{ post.title }}</a>
<span class="archive_post-date">{{ post.date | date: site.date_format }}</span>
</li>
{% endfor %}
</ul>
</section>

<section id="months" class="archive_section">

<h2>Archive by year and month</h2>

{% assign postsByMonthYear = site.posts | group_by_exp:"post", "post.date | date: '%B %Y'"  %}

{% for monthYear in postsByMonthYear %}
<h3>{{ monthYear.name }}</h3>
<ul>
{% for post in monthYear.items %}
<li class="archive_item">
<a class="archive_permalink" href="{{ post.url }}" title="Permanent Link to {{ post.title }}">{{ post.title }}</a>
<span class="archive_post-date">{{ post.date | date: site.date_format }}</span>
</li>
{% endfor %}
</ul>
{% endfor %}
</section>

<section id="categories" class="archive_section">

<h2>Categories</h2>

<ul>
    {% for category in site.categories %}
    <li class="archive_item">
        <a class="archive_permalink" href="/category/{{ category[0] | slugify }}">
            {{ category[0] }}
        </a>
    </li>
    {% endfor %}
</ul>
</section>

<section id="feed" class="archive_section">

<h2>Available RSS feed</h2>

<a href="{{ site.url }}/feed.xml" alt="Full content Atom feed">Atom feed</a>

</section>
