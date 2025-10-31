---
layout: default
title: Home
---

<div class="hero-section">
  <h1>Welcome to My Career Portfolio</h1>
</div>

<div class="content-section">
  <div class="video-container">
    <video id="intro-video" controls width="100%">
      <source src="{{ '/assets/video/intro_en.mp4' | relative_url }}" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
</div>

<script>
  document.addEventListener('DOMContentLoaded', function() {
    const videoSource = document.querySelector('#intro-video source');
    const video = document.getElementById('intro-video');

    // Function to update video based on language
    function updateVideoLanguage(lang) {
      videoSource.src = `{{ '/assets/video/intro_' | relative_url }}${lang}.mp4`;
      video.load(); // Reload the video with the new source
    }

    // Listen for language change events from header
    window.addEventListener('languageChanged', function(event) {
      updateVideoLanguage(event.detail.language);
    });

    // Initialize video with current language
    const currentLang = localStorage.getItem('selectedLanguage') || 'en';
    updateVideoLanguage(currentLang);
  });
</script>