---
layout: default
title: Home
---

This is my site. I need to write posts in markdown and then add a custom jekyll theme. That's easy.

<hr/>

<div class="container mx-auto p-4">
  <h1 class="text-3xl font-semibold mb-4">Welcome to My Photography Portfolio</h1>
  <p class="text-gray-600">I'm a passionate photographer showcasing my work.</p>
  <p class="text-gray-600">Bio: Insert your bio here...</p>
</div>

<div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4 p-4">
  {% for photo in site.data.photos %}
    <div class="border border-gray-300 rounded-lg overflow-hidden">
      <img src="{{ photo.img }}" alt="{{ photo.title }}" class="w-full h-48 object-cover">
      <div class="p-4">
        <h2 class="text-xl font-semibold mb-2">{{ photo.title }}</h2>
        <a href="{{ photo.img }}" class="text-blue-500 hover:underline">View Full Image</a>
      </div>
    </div>
  {% endfor %}
</div>

