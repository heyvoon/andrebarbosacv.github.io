---
layout: default
title: Home
---

<div class="hero-section">
  <h1>Welcome to my Carreer Portifolio. I am glad you want to know more about me.</h1>
  <p>Select a language to get started</p>
</div>

<div class="language-switcher">
  <button class="language-btn active" data-lang="en">English</button>
  <button class="language-btn" data-lang="es">Español</button>
  <button class="language-btn" data-lang="pt">Português</button>
</div>

<div class="content-section">
  <div class="video-container">
    <video id="intro-video" controls width="100%">
      <source src="{{ '/assets/video/intro_en.mp4' | relative_url }}" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>

  <div class="actions-container">
    <div class="view-cv-section">
      <h2>View My Resume</h2>
      <div class="cv-links">
        <a href="/resume-en/" class="btn">View English CV</a>
        <a href="/resume-es/" class="btn">View Spanish CV</a>
        <a href="/resume-pt/" class="btn">View Portuguese CV</a>
      </div>
    </div>

    <div class="pdf-download-section">
      <h2>Download My CV</h2>
      <div class="pdf-links">
        <a href="{{ '/assets/pdf/andre_barbosa_resume_english.pdf' | relative_url }}" class="btn" download>Download English CV (PDF)</a>
        <a href="{{ '/assets/pdf/andre_barbosa_resume_spanish.pdf' | relative_url }}" class="btn" download>Download Spanish CV (PDF)</a>
        <a href="{{ '/assets/pdf/andre_barbosa_resume_portuguese.pdf' | relative_url }}" class="btn" download>Download Portuguese CV (PDF)</a>
      </div>
    </div>
  </div>
</div>

<script>
  document.addEventListener('DOMContentLoaded', function() {
    const languageButtons = document.querySelectorAll('.language-btn');
    const videoSource = document.querySelector('#intro-video source');
    const video = document.getElementById('intro-video');
    const viewCvLinks = {
      'en': '/resume-en/',
      'es': '/resume-es/',
      'pt': '/resume-pt/'
    };
    const downloadPdfLinks = {
      'en': '{{ "/assets/pdf/andre_barbosa_resume_english.pdf" | relative_url }}',
      'es': '{{ "/assets/pdf/andre_barbosa_resume_spanish.pdf" | relative_url }}',
      'pt': '{{ "/assets/pdf/andre_barbosa_resume_portuguese.pdf" | relative_url }}'
    };
    const viewCvButtons = document.querySelectorAll('.view-cv-section .btn');
    const downloadPdfButtons = document.querySelectorAll('.pdf-download-section .btn');


    languageButtons.forEach(button => {
      button.addEventListener('click', function() {
        const selectedLang = this.getAttribute('data-lang');
        
        // Update active button
        languageButtons.forEach(btn => btn.classList.remove('active'));
        this.classList.add('active');

        // Update video source
        videoSource.src = `{{ '/assets/video/intro_' | relative_url }}${selectedLang}.mp4`;
        video.load(); // Reload the video with the new source

        // Update "View CV" links
        viewCvButtons.forEach(btn => {
          const lang = btn.textContent.toLowerCase().includes('english') ? 'en' :
                       btn.textContent.toLowerCase().includes('spanish') ? 'es' : 'pt';
          if (lang === selectedLang) {
            btn.style.display = 'inline-block';
          } else {
            btn.style.display = 'none';
          }
        });

        // Update "Download CV" links
        downloadPdfButtons.forEach(btn => {
          const lang = btn.textContent.toLowerCase().includes('english') ? 'en' :
                       btn.textContent.toLowerCase().includes('spanish') ? 'es' : 'pt';
          if (lang === selectedLang) {
            btn.style.display = 'inline-block';
          } else {
            btn.style.display = 'none';
          }
        });
      });
    });

    // Initialize with English as active
    document.querySelector('.language-btn[data-lang="en"]').click();
  });
</script>