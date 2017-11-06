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
  <label><input name="fields[name-parent]" type="text">Your first name</label>
  <label><input name="fields[name-kid]" type="text">Your first name</label>
  
  <button type="submit">Go!</button>
</form>
</div>