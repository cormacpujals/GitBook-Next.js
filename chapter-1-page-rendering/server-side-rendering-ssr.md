---
description: HTML is generated on each request
---

# Section 2, Server Side Rendering

Assuming data needs to be fetched, that happens first and then the HTML is generated.

<figure><img src="../../.gitbook/assets/Screenshot 2023-04-04 at 8.58.37 PM.png" alt=""><figcaption></figcaption></figure>

The key drawback is also the reason to use SSR: use SSR when the page rendered needs to fetch data for each request. The downside is that each time someone makes a request for an SSR page, the server has to make the request to go out and get the data. (ISR is a great alternative if the data doesn't have to be real-time)&#x20;
