---
title: "Link your GitHub page to a custom domain"
author_profile: true
tags: [Portfolio, Github, Page]
---

## Hi there,

I recently linked my GitHub page (*jlefortbesnard.github.io*) to a custom domain (*jeremylefortbesnard.de*). I bought it on *namecheap.com* since it actually is quite cheap.


I did have troubles matching them so here is what worked for me. I found out that it was actually a problem with **me** rather than with GitHub or NameCheap.


Try to follow these steps and that should be fine:
1. Create your GitHub page [link](/githubpage/)
2. Buy a custom domain (I bought mine on *cheapname.com* for 6$ but you can find some for even cheaper)
3. In GitHub, create a folder named "CNAME" in your GitHub page repository with your domain name (the one you just bought) without the wwww (e.g., I wrote "jeremylefortbesnard.de" for mine)
4. In cheapname.com, got to "domain list", tick on yours and select "manage", now click on "Advanced DNS". There, add the four GitHub IPs as "A record" "@" and the IPs like in this picture:
<img src="{{ site.url }}{{ site.baseurl }}/images/namecheap.png" alt="advanced DNS">
Right now, in summer 2018, it is these 4 ones:
<img src="{{ site.url }}{{ site.baseurl }}/images/ipsgithub.png" alt="IPs GitHub">
But make sure there is no update of these GitHub IPs [there](https://help.github.com/articles/setting-up-an-apex-domain/)
Take a look at this [video](https://www.youtube.com/watch?v=dNbZ826ufKE) if you need help to do so
5. Still in cheapname.com, add the "CNAME record" with "www", then your GitHub page repository name + a period at the end (jlefortbesnard.github.io. for me). It should finally look like this:
<img src="{{ site.url }}{{ site.baseurl }}/images/namecheap.png" alt="advanced DNS">
4. Check that the DNS was well propagated (go on [DNSChecker](https://dnschecker.org/), add you domain name and click on "search"). There shouldn't be any red cross. It can take up to 24h. I suggest you wait for a day and contact namecheap.com if it's still not propagated after 24h. Their online chat is quite efficient.
5. In GitHub, in your GitHub page repository, remove and re-add the CNAME folder (Settings/GitHub Pages/Custom domain)

That's it, weel done!
