---
layout: default
title: Home
---

<div class="hero">
  <p class="hero-eyebrow">Technology · Ideas · Engineering</p>

  <h1>
    Here to explore<br>
  </h1>

  <p class="hero-description">
    A personal space for exploring technology, artificial
    intelligence, software, and ideas I personally find worth thinking about.
  </p>
</div>

<section class="featured-writing" id="writing">
  <h2>Latest writing</h2>
  <p>Notes, perspectives, and things I've been exploring.</p>

{% for post in site.posts limit:5%}
{% unless post.archive %}
<article class="article-card">
<p class="post-meta">
{{ post.date | date: "%B %-d, %Y" }}
</p>

      <h3>
        <a href="{{ post.url | relative_url }}">
          {{ post.title | escape }}
        </a>
      </h3>

      <p>
        {{ post.excerpt | strip_html | normalize_whitespace | truncate: 180 }}
      </p>

      <a href="{{ post.url | relative_url }}">
        Read article &rarr;
      </a>
    </article>
{% endunless %}
{% else %}
<p>New writing coming soon.</p>
{% endfor %}
</section>