# YOU LI CHINA WORLD BANGLADESH — Website

**尤利中制品有限公司** · China-connected fabric sourcing for Bangladesh apparel.

A complete 90-page B2B fabric-sourcing website implementing the *Evidence-led China-connected
sourcing & Bangladesh execution* strategy: full sitemap from the strategic brief, every page
in the mega-menu, an evidence-status design system, a filterable/compared fabric library,
progressive RFQ, and full editorial content on every page.

## Run it

```bash
npm run dev     # build + serve → http://localhost:8080
# or separately:
npm run build   # generates public/ (zero dependencies)
npm run serve   # serves public/ on 0.0.0.0:8080
```

No build tooling, no runtime dependencies — Node ≥18 only.

## Structure

```
site/
  build.js            Static site generator (templates, schema.org, sitemap)
  serve.js            Zero-dependency static server with clean URLs
  content/            All page & product content (evidence-labeled)
    site.js           Identity, navigation (all pages), contacts
    products-*.js     6 categories × (hub + 36 product records)
    pages-*.js        Company, network, quality, services, industries,
                      resources (8 guides + indexes + FAQ), legal
  assets/
    css/style.css     Design system — see DESIGN.md
    js/main.js        Nav, library filter/compare, multi-step forms
    img/              10 conceptual images (labeled as such on-site)
public/               Generated site (90 pages + sitemap.xml + robots.txt)
DESIGN.md             Luxury design-system documentation & industry research
```

## The 90 pages

| Area | Pages |
| --- | --- |
| Home | `/` |
| Products | Library + 6 category hubs + **36 product records** (woven 9, knit 7, denim 5, activewear 4, functional 5, yarns 6) |
| Services | Fabric Sourcing · Yarn Sourcing · Product Development · Import & Distribution · Sourcing Process · Technical Support |
| Company | Overview · Our Story · Why YOU LI · Team · Offices (Bangladesh, China) |
| Sourcing Network | China · Asia · Europe · Planned Regions |
| Quality & Compliance | Quality Assurance · Inline Inspection · Pre-Shipment Verification · Certifications & Compliance · Sustainability |
| Industries | Apparel Brands · Garment Exporters · Buying Houses · Product Development Teams |
| Resources | Fabric Guides + 4 guides · Textile Insights + 2 articles · Quality & Compliance Guides + 2 guides · FAQ · Case Studies · Buyer Success Stories |
| Conversion | Request a Quote (3-step progressive RFQ) · Request a Sample · Contact |
| Legal | Privacy · Terms · Cookies |

## Evidence discipline (per the strategy brief)

Every claim carries a published status — `Verified document`, `Company statement`,
`Reference range`, `Verification in progress`, `Buyer permission required`,
`Not publicly verified` — rendered as first-class pills. Sedex/Higg/Inditex are tracked in
the public verification register as **not publicly verified**, never as endorsements.
Client names and testimonials publish only through the permission gate (stated on-site).
Placeholder contact values are marked as launch-draft for final verification.

## Replace before launch

1. Contact values in `site/content/site.js` (`contact`) — phone/email are placeholders.
2. Legal-entity details on the legal pages once confirmed.
3. Form endpoints — the RFQ/sample/contact forms simulate submission client-side
   (inquiry IDs, confirmation); wire them to your CRM/email in `site/build.js` + `site/assets/js/main.js`.
4. Real photography may replace conceptual imagery as assets become available (keep captions truthful).
