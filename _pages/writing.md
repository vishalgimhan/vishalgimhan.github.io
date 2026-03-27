---
permalink: /writing/
title: "Writing"
author_profile: true
---

<div id="medium-articles"></div>

<script>
fetch('https://api.rss2json.com/v1/api.json?rss_url=https://medium.com/feed/@vishalgimhan')
  .then(res => res.json())
  .then(data => {
    const container = document.getElementById('medium-articles');
    data.items.forEach(item => {
      container.innerHTML += `
        <div style="margin-bottom:2em">
          <h3><a href="${item.link}" target="_blank">${item.title}</a></h3>
          <p style="color:grey">${item.pubDate.substring(0,10)}</p>
          <p>${item.description.substring(0,200)}...</p>
        </div>`;
    });
  });
</script>
