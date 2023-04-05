---
description: HTML is rendered at build time and reused for each request
---

# Section 1, Static Site Generation

Static generation, the HTML is generated at build time and is reused for each request.

Case 1: SSG with and without data fetching (marketing page/about page): HTML is generated at build time.&#x20;

<figure><img src="../../.gitbook/assets/Screenshot 2023-04-04 at 11.20.32 AM.png" alt=""><figcaption></figcaption></figure>

Case 2: SSG with data (blog post/to dos): HTML is generated AFTER fetching data at build time

<figure><img src="../../.gitbook/assets/Screenshot 2023-04-04 at 11.19.03 AM.png" alt=""><figcaption></figcaption></figure>

Case 3: Incremental Static Regeneration (ISR) is also possible with getStaticProps() in which case you can set a revalidation period based on the cache control http header.

<figure><img src="../../.gitbook/assets/Screenshot 2023-04-04 at 11.23.15 AM.png" alt=""><figcaption></figcaption></figure>

If the page path depends on external data, you will fetch the external data and then generate a path for each of the blog posts in your blog using getStaticPaths()

Use getStaticProps when:

* All the data needed for page rendering is available at build-time (even if the data is fetched over the network)
* The data is cacheable
* The page must be pre-rendered for SEO
* The page must load fast

\[Review SSG, it's shortcomings and transition into SSR]
