# Nipun Balachandran Nair — Personal Website

Source for **[nipunbnair.github.io](https://nipunbnair.github.io)**, my academic and professional portfolio. It collects my research, projects, open-source work and teaching in a single static page.

> MPhil Student · AI Researcher · Machine Learning Engineer
> Monash University, Clayton, Melbourne, Australia

---

## About

I'm an MPhil student at Monash University working on **Generative AI and Conversational Recommendation Systems** under Dr Teresa Wang and Dr Tongtong Wu. My background spans large language models, NLP for low-resource languages, biomedical machine learning and agentic AI systems, with prior industry experience in the automotive sector and research internships at UC Santa Cruz and OdiaGenAI.

This site is where that work lives publicly — papers, code, demos and teaching.

## What's on the site

| Section | Contents |
| --- | --- |
| **About** | Hero portrait, current role and affiliation |
| **Connect** | Email, CV, Google Scholar, GitHub and website links |
| **Research & Interests** | Research statement, focus areas, workshop demo and YouTube channel *The GenAI Pilgrim* |
| **Research Projects** | Six featured projects — Odia LLaMA-2 fine-tuning, Olive (instruction-following Odia GPT), Malayalam dementia dataset, palm-leaf image segmentation with FCNs, Kalman-filter pollution analysis, IPL Auction System |
| **GitHub Repositories** | Filterable cards (AI & ML / Web / Data Science / Academic) linking to public repos |
| **Teaching** | FIT1059 *AI for Everyone* — units taught and SETU reports |

## Built with

Deliberately dependency-free: **HTML5**, **CSS3** (custom properties, CSS Grid, Flexbox) and **vanilla JavaScript**. No framework, no bundler, no `npm install` — the page is a single self-contained file plus assets.

Interactive behaviour is hand-rolled: a sticky nav with a mobile hamburger menu, smooth-scroll anchors, and client-side category filtering for the repository cards.

## Repository structure

```
.
├── index.html                            # The entire site — markup, styles and scripts
├── nipun1.jpg                            # Hero portrait
├── Nipun_Nair_AI_Engineer_Resume.pdf     # Downloadable CV
├── SETU dashboard-TE.pdf                 # Teaching evaluation reports
├── images/                               # Gallery / collage photos
└── README.md
```

## Running it locally

Clone and open — that's the whole workflow.

```bash
git clone https://github.com/nipunbnair/nipunbnair.github.io.git
cd nipunbnair.github.io
open index.html          # or: xdg-open index.html
```

To test relative asset paths and anchor links the way GitHub Pages serves them, use a local server instead:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deployment

Hosted on **GitHub Pages** from the `main` branch. Any push to `main` is published automatically within a minute or two — there is no build step.

```bash
git add .
git commit -m "Update portfolio"
git push origin main
```

## Customising the page

**Theme colours** live as CSS custom properties in the `:root` block at the top of `index.html`:

```css
:root {
    --primary-color: #667eea;
    --secondary-color: #764ba2;
    --dark-color: #2d3748;
    --light-gray: #718096;
}
```

**Adding a repository card** — copy an existing `.repo-card` block and set `data-category` to one or more of `ai-ml`, `web`, `data`, `academic` so the filter buttons pick it up.

**Adding a project** — duplicate a `.project` div inside `.project-container`; the grid reflows on its own.

**Gallery images** — drop files into `images/` and add a `.collage-item` per photo. Resize to roughly 1200 px on the long edge and compress before committing; GitHub Pages serves images uncompressed, and full-size phone photos noticeably slow first paint.

## Responsiveness and accessibility

The layout is mobile-first below 768 px: the nav collapses to a hamburger menu, multi-column grids fold to a single column, and images scale within their containers. Images carry descriptive `alt` text and use `loading="lazy"` below the fold.

## Contact

- **Email** — [nipunbnair@gmail.com](mailto:nipunbnair@gmail.com)
- **Google Scholar** — [Publications](https://scholar.google.co.in/citations?hl=en&user=mefMP2gAAAAJ)
- **GitHub** — [@nipunbnair](https://github.com/nipunbnair/)
- **YouTube** — [The GenAI Pilgrim](https://www.youtube.com/@TheGen-AIPilgrim)

## License

Code in this repository is available under the MIT License. Written content, images, CV and teaching materials are © Nipun Balachandran Nair — please ask before reusing them.
