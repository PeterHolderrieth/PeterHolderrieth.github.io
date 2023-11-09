---
layout: page
title: music
permalink: /music/
description: I am also a passionate guitarist and composer. Find below a list of musical projects that I have done over the years. I don't have many listeners. So you can make a difference :)
nav: true
nav_order: 2
horizontal: false
---

<style>
  /* Add margin between sections */
  .music-project {
    margin-bottom: 30px; /* Adjust the margin as needed */
  }

  /* Style section headers with a smaller font size and bold */
  .music-project h2 {
    font-size: 16px; /* Adjust the font size as needed */
    font-weight: bold;
  }
</style>

<hr> <!-- Add the horizontal line here -->

<!-- Display music projects -->
<div class="music-projects">
{%- assign music_projects = site.data.music_projects -%}
<!-- Loop through music projects -->
{% for project in music_projects %}
  <div class="music-project">
    <h2>{{ project.title }}</h2>
    <p>{{ project.description }}</p>
    <!-- Spotify HTML Embed Code -->
    <div class="spotify-embed">
      {{ project.spotify_embed }}
    </div>
  </div>
{% endfor %}
</div>
