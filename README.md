# ADLA website — JavaScript export

Complete static website: plain HTML, CSS and JavaScript. No npm install, Node.js server, build step, API key or Sites account is needed to host it.

Includes English and Arabic, the charcoal/silver design with the original blue/mint logo, five-image hero slideshow, services, mission/vision, four project case studies, model/layer explorers, process, deliverables, FAQ and contact form. The website portfolio is included; the underlying POS and Python applications are not deployed by this package.

## Publish on GitHub Pages

1. Unzip this download. Create a public GitHub repository, for example `adla-website`.
2. Upload the **contents** of this folder to the repository root. `index.html` must be at the top level beside `app.js`, `styles.css` and `assets/`; do not upload just the ZIP or nest everything in another folder. Include `.nojekyll` (create that empty file in GitHub if your uploader hides it).
3. In repository **Settings → Pages**, choose **Deploy from a branch**, then **main** and **/(root)**. Save.
4. Open the URL GitHub provides when deployment finishes. Relative links support both `https://USERNAME.github.io/REPOSITORY/` and a custom domain.

## Connect your Namecheap domain

Replace `USERNAME` with your GitHub account name. No domain name has been preconfigured because you have not supplied one.

1. Add your actual domain under GitHub repository **Settings → Pages → Custom domain** and save **before** changing DNS. GitHub creates a `CNAME` file; keep it in future uploads.
2. If using Namecheap BasicDNS, open **Domain List → Manage → Advanced DNS → Host Records**. If another provider manages your nameservers, edit DNS there instead.
3. Replace conflicting parking/redirect records for `@` and `www` with these records. Preserve unrelated mail and verification records.

| Type | Host | Value |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | USERNAME.github.io |

Use automatic/default TTL. The CNAME value has no `https://` or repository path. Allow DNS propagation and certificate provisioning, then enable **Enforce HTTPS** in GitHub Pages. See the official guides below for current details.

## Contact form

The form uses FormSubmit and sends to `adla.agency@outlook.com`. It requires internet access and any activation requested by FormSubmit. After publishing, submit one enquiry yourself, complete any activation email and confirm delivery. Delivery has not been verified in this export. The thank-you redirect automatically uses your current domain/repository path. WhatsApp and phone links are also included.

## Edit and preview

- `app.js`: homepage text, sections, translations, slideshow and form.
- `styles.css`: visual design and responsive layouts.
- `case-data.js`: bilingual project details.
- `case-studies.js`: case-study rendering and explorers.
- `assets/`: logo, photos and plots.
- Four named project HTML files: individual case-study entry points.
- `thanks.html`: enquiry confirmation page.
- `demos/`: earlier standalone demos, retained from the site export.

For local preview, open the folder with VS Code Live Server, or run `python -m http.server 8000` here and visit `http://localhost:8000`. Do not test email delivery from a `file://` page.

External services: Google Fonts, FormSubmit and the linked Fume Society website. Project visualizations use saved model outputs/default inputs; the POS preview is a code-adapted illustration. Real recordings and client testimonials remain pending. No raw project archives, model weights, credentials or Git history are included.

## Official setup references

Checked 7 October 2026:
- https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
- https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site
- https://www.namecheap.com/support/knowledgebase/article.aspx/9645/2208/how-do-i-link-my-domain-to-github-pages/
