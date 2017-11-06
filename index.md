---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
---
<div style="background: red">
<form method="POST" action="https://api.staticman.net/v2/entry/fuselagetown/staticmantest/gh-pages/comments/">
  <input name="options[redirect]" type="hidden" value="https://stitchfix-prototype.netlify.com/clients/kid">
  <!-- e.g. "2016-01-02-this-is-a-post" -->
  <input name="options[slug]" type="hidden" value="{{ page.slug }}">
  <input name="fields[title]" type="text" value="Emilia">
  <input name="fields[type]" type="text" value="parent">
  
  
  <button type="submit">Go!</button>
</form>
</div>