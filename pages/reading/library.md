---
layout: page
title: Library
permalink: /library/
tags: library read_list
---

I decided keep track of the books and particularly thoughtful articles that I've read since July 2021. 

For particularly polarizing books or articles, I go more in depth at my [reviews]({{ site.baseurl }}/reviews) page. Maybe I'll be able to review all of them in depth eventually!

<section style="display: flex; justify-content: space-between; flex-wrap: wrap">
{% for member in site.data.library %}
    {% if member.review_path %}
        <a target="_blank" rel="noopener noreferrer" href="{{ site.baseurl }}/reviews/{{ member.review_path }}" style="color: #333333; flex: 1; width: 100%; min-width: 250px; padding-top: 5%;">
    {% else %}
        <a target="_blank" rel="noopener noreferrer" href="https://www.librarything.com/isbn/{{ member.isbn }}" style="color: #333333; flex: 1; width: 100%; min-width: 250px; padding-top: 5%;">
    {% endif %}
        <div style="width: 250px">
            <img class="grow-me" src="http://covers.openlibrary.org/b/ISBN/{{ member.isbn }}-L.jpg">
        </div>
        <div style="width: 250px">
            <h4>{{ member.title }}</h4>
            <h6>{{ member.author }}</h6>
            <h6>{{ member.rating }}</h6>
        </div>
    </a>
{% endfor %}
</section>

<style>
.grow-me {
  border-radius: 4px;
  transition: all .2s ease-in-out;
}

.grow-me:hover {
  transform: scale(1.02);
}

</style>
