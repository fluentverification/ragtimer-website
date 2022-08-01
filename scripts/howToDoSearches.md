# How to make your website searchable

Most websites use a server-side database lookup to do a sitewide search, but the STAMINA website (and I bet your website too) is hosted on GitHub pages, making it so that it's *static*. This means, no PHP, CGI, or server-side anything (and that means *NO DATABASES*). However, I implemented some stuff to do this in vanilla JS. I referenced [this site](https://gomakethings.com/how-to-create-a-vanilla-js-search-page-for-a-static-website/) quite a bit while doing this, so it's probably a better reference than this markdown file. However, there are a couple of implementation-specific nuances.

You will need to create a JSON file with all of your search information. The python file in the root directory will help you do this. Make sure you use the `-j` option so it's in JSON format. Then you will need to do some work on the `search.html` page. `search.html` looks for a search query called `q`, meaning you will be able to query it using https://yourwebsite.com/search.html?q=your\_query. Any other page on your site just has to go to that location. You can even import `search.js` and use the `search(query)` function to do this (but change the root domain).

I made some improvements to the reference I used. Mainly, it highlights where in the page the result is. If you don't like the style, just mess around with the CSS until you do.
