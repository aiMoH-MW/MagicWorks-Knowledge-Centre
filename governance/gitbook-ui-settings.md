# GitBook UI settings for MagicWorks

These settings apply to the synced MagicWorks GitBook site.

## Theme

Site title:

**MagicWorks Knowledge & Resource Centre**

Preferred brand settings:

- Primary accent: `#5B3FBE`
- Deep brand indigo: `#2A1B5C`
- Gold accent: `#D4A537`
- Ivory: `#F7F3EA`
- Graphite: `#1A1A22`

Use:

- `assets/branding/logo-header.webp` for the header logo
- `assets/branding/logo-footer.webp` for footer branding if available on the selected plan
- `assets/branding/favicon.ico` for the favicon

Header logo primary link should point to:

https://magicworksitsolutions.com/

## Header links

1. MagicWorks → https://magicworksitsolutions.com/
2. Services → https://magicworksitsolutions.com/services
3. Work → https://magicworksitsolutions.com/work
4. Knowledge → the Knowledge Centre section
5. Contact → https://magicworksitsolutions.com/contact

No internal UTM parameters.

## Configuration

Recommended:

- Default interface language: English
- Page ratings: enabled
- AI/MCP page actions: enabled where available
- Copy / Markdown page actions: enabled
- MCP connect/copy action: enabled
- PDF export: optional
- Edit on Git: leave disabled for public visitors unless external contributions are intentionally desired

Privacy policy:

https://magicworksitsolutions.com/privacy

Terms:

https://magicworksitsolutions.com/terms

## AI experience

If the selected site plan supports the full GitBook Assistant, use it.

Suggested questions:

1. What services does MagicWorks offer?
2. What is the difference between SEO, AEO and GEO?
3. How do I know whether my company is ready for AI?
4. What is an AI-native website?
5. How does MagicWorks advise marketplace and platform founders?

If the site plan does not retain full Assistant after trial, keep AI Search enabled where supported.

## Machine-readable access

After publication on the custom domain, verify:

- https://knowledge.magicworksitsolutions.com/llms.txt
- https://knowledge.magicworksitsolutions.com/llms-full.txt
- https://knowledge.magicworksitsolutions.com/~gitbook/mcp
- representative page URL with `.md` appended

## Custom domain

Target hostname:

`knowledge.magicworksitsolutions.com`

Use GitBook **Settings → Domain and URL** to start custom-domain configuration.

Copy the exact DNS target shown by GitBook into the DNS provider. Do not guess the CNAME target and do not alter unrelated MagicWorks DNS records.

If Cloudflare is used, validate the hostname with the proxy state GitBook requires before enabling any proxying.

## Analytics

The MagicWorks website currently loads Google Tag Manager container:

`GTM-W75DJC`

GitBook's native Google Analytics integration requires the site's GA4 **Measurement ID** in the `G-XXXXXXXXXX` format. The GTM container ID is not a substitute.

Use the existing MagicWorks GA4 property/web stream if it is intended to measure both the main site and the knowledge subdomain.

Do not create a duplicate GA4 property solely for GitBook unless there is a deliberate measurement reason.

Recommended measurement after publication:

- sessions and landing pages
- organic search entrances
- AI-assistant referral traffic where identifiable
- knowledge → service navigation
- contact/enquiry actions
- resource downloads
- site search / AI search usage
- page feedback

## Search platforms

After publication:

1. Verify the knowledge host in Google Search Console as appropriate.
2. Submit the GitBook-generated sitemap.
3. Add/verify the site in Bing Webmaster Tools.
4. Submit the sitemap there as well.
5. Establish the launch date as the measurement baseline.

## Publication gate

Do not publish until:

- custom-domain setup is ready or an intentional decision is made to launch first on the GitBook hostname;
- logo/favicon are checked;
- AI/search experience is checked;
- page ratings/actions are checked;
- desktop and mobile preview are reviewed;
- post-trial site plan has been confirmed.
