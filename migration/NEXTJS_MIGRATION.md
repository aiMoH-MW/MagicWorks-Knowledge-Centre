# Next.js migration plan

The repository remains the **source of truth** for the MagicWorks Knowledge & Resource Centre after GitBook.

## Recommended target

- Next.js App Router
- TypeScript
- Tailwind CSS
- Deploy on Vercel
- Domain: `https://knowledge.magicworksitsolutions.com`
- Content stays in the existing `home/`, `knowledge/`, `help/`, and `changelog/` directories

Do not rewrite the knowledge content into React components. Keep Markdown as the editorial source and render it at build/runtime.

## Stable URL policy

Preserve these public route families:

- `/` → `home/README.md`
- `/knowledge/*` → `knowledge/**.md`
- `/help/*` → `help/**.md`
- `/changelog/*` → `changelog/**.md`

The machine-readable route map is stored in `migration/route-manifest.json`.

If GitBook URLs are ever indexed before migration, add explicit 301 redirects from those paths to the stable Next.js equivalents.

## Content parsing

Use a Markdown pipeline that supports:

- YAML frontmatter
- GitHub Flavored Markdown
- tables
- code blocks
- headings with stable anchors
- images and local assets
- external links
- internal relative links

Suggested packages:

- `gray-matter`
- `remark`
- `remark-gfm`
- `remark-rehype`
- `rehype-slug`
- `rehype-autolink-headings`

## GitBook-specific syntax

Some pages currently use GitBook blocks such as:

- `{% hint %}`
- `{% columns %}`
- card tables using `data-view="cards"`
- GitBook-style button classes

Do **not** rewrite all content manually.

Create a compatibility layer that converts these blocks to Next.js/MDX components during rendering. Once the Next.js site is stable, the syntax can be normalised gradually if desired.

## Information architecture

Keep four top-level content areas:

1. Home
2. Knowledge Centre
3. Help Centre
4. Changelog

The public Knowledge Centre continues to cover:

- Digital Marketing
- SEO / AEO / GEO / AI Search Visibility
- AI Consultation & AI Readiness
- AI Automation
- Web Development / AI-native websites
- Marketplace & Platform Consultation
- Brand, Research & Publishing
- Buyer guides
- Frameworks and case-study learnings

## Branding

Use the existing MagicWorks brand tokens:

- Indigo: `#2A1B5C`
- Violet: `#5B3FBE`
- Gold: `#D4A537`
- Ivory: `#F7F3EA`
- Graphite: `#1A1A22`
- Pale violet: `#EDE9F7`

Typography:

- Headings: Source Serif 4
- Body/interface: Inter

Approved brand assets are under `assets/branding/`.

## SEO

Next.js must generate:

- canonical URLs
- titles and descriptions from frontmatter
- Open Graph/Twitter metadata
- XML sitemap
- robots.txt
- breadcrumbs
- structured data where useful
- stable heading anchors
- 301 redirects for retired GitBook URLs

The main MagicWorks website remains the commercial canonical surface. The Knowledge Centre remains the explanatory/reference surface.

## AI discoverability

Recreate the GitBook machine-readable benefits in Next.js:

- `/llms.txt`
- `/llms-full.txt`
- Markdown/plain-text page representations where useful
- a read-only MCP endpoint if retained as part of the MagicWorks AI-discovery strategy
- clear entity, framework and authorship data

Do not promise citation by AI systems.

## Search and analytics

When the Next.js site is live on the final custom domain:

- create/verify a dedicated GSC URL-prefix property for `https://knowledge.magicworksitsolutions.com/`
- add a separate Bing Webmaster Tools site
- use a dedicated GA4 web stream inside the existing MagicWorks GA4 property
- do not use internal UTMs between the main site and knowledge subdomain

## GitBook transition

Until migration:

- keep GitBook content Git-synced from this repository if GitBook is used for staging;
- do not make GitBook-only content edits that are not committed back to Git;
- do not depend on trial-only GitBook features for permanent functionality;
- do not index a temporary `.gitbook.io` URL if the Next.js custom-domain launch is imminent.

After the Next.js site is validated, GitBook can be retired without losing the knowledge content.
