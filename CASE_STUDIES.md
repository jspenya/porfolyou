# Case study guide

Use this structure for new portfolio case studies and when extending existing ones. Steph approved it through the Cornerstone Instagram case study. The reference implementation is [case-studies/cornerstone-instagram.html](case-studies/cornerstone-instagram.html); use [DESIGN.md](DESIGN.md) for the portfolio’s visual language.

## Page structure

Keep these sections in order. Adapt their headings and length to the project; the example wording is not a requirement. Include screenshot sections when real evidence is available, and omit them when it is not.

1. **Introduction.** Link back to the homepage’s case studies section. Add a short project/category label, an outcome-focused lowercase title, and a one-paragraph summary. Follow with “my contribution” and “built with” metadata. Describe Steph’s actual scope.
2. **Published examples — “out in the world.”** Show real outputs early so visitors can see what the work produced. Give each screenshot a brief descriptive caption and a link to the original public result when available.
3. **The challenge.** Explain the user’s problem and why the feature was needed. Establish the business or workflow context before technical details.
4. **The workflow.** Explain the experience from input to result. Use a short ordered sequence for actual steps (Cornerstone uses Brief → Generate → Review → Publish), followed by prose explaining important handoffs or human decisions.
5. **Inside the product — “inside the admin.”** Show the real interface that supports the workflow. Explain what is visible and connect it to an output shown earlier where possible.
6. **The decisions behind it.** Use short subsections for meaningful engineering or product choices. Explain the problem each decision addresses, how the solution behaves, and relevant tradeoffs. Cornerstone covers product context, independent regeneration, publishing, and traceability; choose topics appropriate to the new case.
7. **The outcome — “what this makes possible.”** Describe the delivered capability and the difference it makes to the workflow. Include measured results only when supported by evidence. Close with a short personal takeaway grounded in the work.
8. **Closing links.** Provide a return to case studies and a link to the homepage contact section.

## Voice and evidence

- Write in Steph’s first-person voice: casual, clear, and specific. Keep headings lowercase and paragraphs comfortably short.
- Lead with the user’s experience. Include technical details when they explain a decision or substantiate a capability.
- Verify implementation claims against the source or supplied project evidence. Distinguish automated steps from human review and approval.
- Use actual screenshots and public links supplied or verified for the project. Keep descriptions faithful to what the evidence shows.
- Distinguish delivered capabilities from measured business results. Do not invent time savings, engagement improvements, customer quotes, or metrics.
- Match claims about tests to available evidence; the presence of specs is different from a verified passing test run.

## Screenshots and layout

- Store case-study assets under `assets/case-studies/<project>/` with descriptive filenames.
- Preserve full screenshots and their natural aspect ratios, including captions or interface context. Follow the existing full-width, vertically stacked presentation so details remain readable.
- Wrap each screenshot in a link to the full-size image. Use a semantic `figure` and `figcaption`, meaningful alt text, explicit image dimensions, and lazy loading for images below the opening content.
- Keep the original-post link separate from the full-size screenshot link. External links that open a new tab use `rel="noopener noreferrer"` and an accessible new-tab indication.
- Reuse the existing `study-*`, `project-image`, and portfolio design tokens. Preserve the charcoal-and-butter palette, Lora headings, DM Sans body, generous spacing, and bounded prose width.
- Let workflow columns stack on small screens. Keep keyboard focus visible and respect reduced-motion preferences.

## Adding a case study

1. Create `case-studies/<slug>.html` with Jekyll frontmatter: `layout: default`, a descriptive `title`, a concise `description`, and `permalink: /case-studies/<slug>/`.
2. Build the page using the structure above and the reference page’s semantic markup. Give section headings unique IDs and connect each section with `aria-labelledby`.
3. Add a summary entry to the homepage’s `#case-studies` section: project title, brief context, outcome-focused summary, and a descriptive link to the full story. Use the homepage’s compact `study-grid` / `study-card` presentation: project name, an uncropped preview linking to the story, one short summary, and a descriptive read link. Full-size screenshot links and captions belong on the detail page. Keep the existing navigation destination.
4. Use Jekyll’s `relative_url` filter for local assets and internal links. From a detail page, link back to homepage anchors using the homepage URL, rather than a fragment alone.
5. Verify the result before presenting it: Jekyll builds successfully; every image loads; screenshot links open the intended full-size file; public links match their examples; homepage/detail/contact navigation works; desktop and mobile layouts have no horizontal overflow. The reference was checked at 1280, 768, 390, and 320 pixels.
6. Present a local preview and report edits, commits, pushes, and deployments as separate states. Follow the project’s publication authorization rules.
