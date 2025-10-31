---
layout: default
title: Home
---

<div class="hero-section">
  <h1>Welcome to My Career Portfolio</h1>
  <p>Select a language to view my resume</p>
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
    const languageButtons = document.querySelectorAll('.language-btn');
    const videoSource = document.querySelector('#intro-video source');
    const video = document.getElementById('intro-video');

    languageButtons.forEach(button => {
      button.addEventListener('click', function() {
        const selectedLang = this.getAttribute('data-lang');
        
        // Update video source
        videoSource.src = `{{ '/assets/video/intro_' | relative_url }}${selectedLang}.mp4`;
        video.load(); // Reload the video with the new source
      });
    });
  });
</script>