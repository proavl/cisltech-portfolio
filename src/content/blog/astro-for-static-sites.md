---
title: "Why I Switched to Astro for Static Sites in 2024"
description: "After years of reaching for Next.js for everything, I've been defaulting to Astro for portfolio sites, documentation, and content-heavy projects. Here's why."
pubDate: 2025-01-08
updatedDate: 2025-03-20
tags: ["Astro", "Web Development", "Static Sites", "JavaScript"]
---

I've built a lot of websites. Marketing sites, web apps, dashboards, documentation portals. For most of the 2020s my default was Next.js — it was flexible, had a great ecosystem, and React was everywhere.

But for static and mostly-static sites, Next felt like overkill. The bundle sizes were large, the build times were slow, and the mental overhead of thinking about SSR vs. SSG vs. ISR for a six-page portfolio site was real.

Then I tried Astro.

## What Astro Gets Right

**Zero JS by default.** Astro ships no JavaScript to the browser unless you explicitly opt in with an `client:*` directive. For content-heavy sites, this is transformative — the performance improvements are immediate and measurable.

**Islands architecture.** If you need interactivity in one component, you can hydrate just that island. The rest of the page is static HTML. You can even use React, Vue, Svelte, or Solid components side-by-side in the same project.

**Content collections.** Astro's content collection API with Zod schema validation is genuinely excellent. Type-safe frontmatter, automatic slug generation, and a clean `getCollection()` API. Writing a blog or docs site is a joy.

**Performance out of the box.** Lighthouse 100s without jumping through hoops. Astro handles image optimisation, CSS scoping, and minimal JS automatically.

## The Trade-Offs

Astro isn't for everything. If you're building an application with lots of client-side state — a dashboard, a SaaS product — Next.js or Remix are still better choices. Astro's sweet spot is content: blogs, portfolios, documentation, marketing sites.

The ecosystem is also smaller than React's, though it's grown significantly. Most things you need exist.

## My Current Stack for Static Sites

For a typical portfolio or marketing site now:

```
Astro + MDX (content)
Tailwind (or plain CSS with custom properties)
Vercel or GitHub Pages (hosting)
```

That's it. No unnecessary complexity. Ships fast, costs nothing to host, scores well on Core Web Vitals, and is a pleasure to maintain.

This site was built with exactly that stack. The source is on [GitHub](https://github.com/proavl) if you want to poke around.

## Conclusion

Use the right tool for the job. Astro is now my default for static and content sites. Next.js is still my choice for full applications. The key is not defaulting to the same framework for everything.
