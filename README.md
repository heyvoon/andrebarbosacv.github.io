# Digital Curriculum - André Barbosa

A modern, multilingual digital curriculum vitae built with Jekyll, featuring a single-page application interface with video introductions and resume content in multiple languages.

## 🌟 Features

- **Multilingual Support**: Available in English, Spanish, and Portuguese
- **Single-Page Application**: Tabbed interface with smooth transitions
- **Video Introductions**: Language-specific video presentations
- **Responsive Design**: Optimized for desktop and mobile devices
- **Dark Theme**: Modern dark color scheme with accent colors
- **Dynamic Content**: Language switching without page reloads
- **PDF Downloads**: Downloadable resume PDFs for each language

## 🚀 Quick Start

This is a Jekyll-based static site that can be deployed to GitHub Pages or any static hosting service.

### Prerequisites

- Ruby (for local development)
- Jekyll (for local development)

### Local Development

1. Clone the repository:
```bash
git clone https://github.com/yourusername/digital-cv.git
cd digital-cv
```

2. Serve locally (if you have Jekyll installed):
```bash
jekyll serve
```

3. Open `http://localhost:4000` in your browser

### Deployment

The site is configured for GitHub Pages deployment. Simply push to the main branch and GitHub Pages will automatically build and deploy the site.

## 📁 Project Structure

```
digital_cv/
├── _config.yml          # Jekyll configuration
├── _data/               # Language-specific content
│   ├── en.yml           # English content
│   ├── es.yml           # Spanish content
│   └── pt.yml           # Portuguese content
├── _includes/           # Reusable components
│   └── header.html      # Site header with navigation
├── _layouts/            # Page templates
│   └── default.html     # Main layout (SPA template)
├── _pages/              # Additional pages (legacy)
├── assets/              # Static assets
│   ├── css/
│   │   └── main.scss    # Main stylesheet
│   ├── pdf/             # PDF resume files
│   ├── resumes/         # Markdown resume content
│   └── video/           # Video introduction files
├── index.md             # Homepage
└── README.md            # This file
```

## 🎨 Design Features

### Header
- Site title with custom styling
- LinkedIn profile link with official logo
- Language selector (EN, ES, PT) with active state highlighting

### Navigation
- Two-tab interface: Video Introduction and Resume
- Smooth transitions between tabs
- Persistent active tab state

### Content Sections

#### Video Introduction Tab
- Embedded video player with language-specific content
- Muted auto-play with user controls
- Responsive video container

#### Resume Tab
- Web-formatted resume content in markdown
- Language-specific content switching
- Download PDF button for each language
- Clean typography and spacing

### Technical Features
- **Local Storage**: Remembers user's language preference
- **Dynamic Updates**: Content updates without page reloads
- **Responsive**: Mobile-first design approach
- **Accessibility**: Semantic HTML and keyboard navigation

## 🌐 Language Support

The site supports three languages:

- **English (EN)**: Primary language
- **Spanish (ES)**: Español
- **Portuguese (PT)**: Português

Each language has:
- Complete navigation labels
- Resume content in markdown format
- Video introduction
- PDF download link

## 🛠️ Customization

### Adding New Languages

1. Create a new data file in `_data/` (e.g., `fr.yml`)
2. Add the language code to the header template in `_includes/header.html`
3. Create markdown resume content in `assets/resumes/`
4. Add video file to `assets/video/`
5. Add PDF file to `assets/pdf/`

### Styling

The site uses SCSS for styling with a dark theme. Key color variables:
- Primary: `#bb86fc` (Purple accent)
- Secondary: `#89ddff` (Blue accent)
- Background: `#121212` (Dark background)
- Surface: `#1e1e1e` (Card backgrounds)

### Content Management

All text content is managed through the `_data/` YAML files, making it easy to update without modifying templates.

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📞 Contact

- **LinkedIn**: [André Barbosa](https://www.linkedin.com/in/abamaral)
- **Live Site**: https://yourusername.github.io/

---

Built with ❤️ using Jekyll and modern web technologies.