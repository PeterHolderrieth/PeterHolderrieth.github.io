---
layout: page
title: music
permalink: /music/
description: I am also a passionate guitarist and love writing music. Find below a list of musical works that I have written over the years. I don't have many listeners. So you can make a difference :) I am also playing in the band <em>Indigo</em> with whom I play regularly in the Boston area.
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

  .music-photos {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
    margin-bottom: 30px;
  }

  .music-photos img {
    width: 100%;
    height: 280px;
    object-fit: cover;
    border-radius: 12px;
  }

  /* Keep the guitar portrait framed on the player rather than the ceiling */
  .music-photos img.portrait {
    object-position: center 30%;
  }

  @media (max-width: 576px) {
    .music-photos {
      grid-template-columns: 1fr;
    }

    .music-photos img {
      height: 240px;
    }
  }
</style>

<div class="music-photos">
  <img class="portrait" src="{{ '/assets/img/music/guitar.jpeg' | relative_url }}" alt="Playing classical guitar" loading="lazy">
  <img src="{{ '/assets/img/music/indigo.JPG' | relative_url }}" alt="On stage with the band Indigo in Boston" loading="lazy">
</div>

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
