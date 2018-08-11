---
title: "Link your GitHub page to a custom domain"
author_profile: true
tags: [GitHub]
---

I recently linked my GitHub page (*jlefortbesnard.github.io*) to a custom domain (*jeremylefortbesnard.de*). I bought it on *namecheap.com* since it is actually quite cheap.


I did have troubles matching them so here is what worked for me. I found out that it was actually a problem with **me** rather than with GitHub or NameCheap.


Try to follow these steps and that should be fine:

* Create your GitHub page [link](/githubpage/)


* Buy a custom domain (I bought mine on *namecheap.com* for 6$ but you can find one for even cheaper)


* In GitHub, create a document named "CNAME" in your GitHub page repository. Inside this document, write your domain name only (the one you just bought) without the www (e.g., I wrote "jeremylefortbesnard.de" for mine)


* In namecheap.com, go to "domain list", tick your domain and select "manage". Now, click on "Advanced DNS". There, add the four GitHub IP's as "A record", "@", and the IPs like in this picture:


<img src="{{ site.url }}{{ site.baseurl }}/images/namecheap.png" alt="advanced DNS">


Right now, in summer 2018, it is these four IP's:


<img src="{{ site.url }}{{ site.baseurl }}/images/ipsgithub.png" alt="IPs GitHub">


But make sure there isn't any update of these GitHub IPs [there](https://help.github.com/articles/setting-up-an-apex-domain/) (scroll down until "Configuring A records with your DNS provider" and check the IPs)


Take a look at this [video](https://www.youtube.com/watch?v=dNbZ826ufKE) if you need help at this point.


* Still in namecheap.com, add the "CNAME record" with "www", then your GitHub page repository name + a period at the end (jlefortbesnard.github.io. for me). It should finally look like this:


<img src="{{ site.url }}{{ site.baseurl }}/images/namecheap.png" alt="advanced DNS">


* Once it's done, check that the DNS was well propagate: go on [DNSChecker](https://dnschecker.org/), add your domain name and click on "search". There shouldn't be any red cross. It can take up to 24h. I suggest you wait for a day and contact namecheap if it's still not propagated after 24h. Their online chat is quite efficient.


* In GitHub, in your GitHub page repository, remove and re-add the CNAME folder: click on "Settings" then "GitHub Pages" and finally "Custom domain".

That's it, well done!
