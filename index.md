---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
---
<a href="#" class="cookie">do we have javascript?</a>

<div style="background: red">
<form  action="https://api.staticman.net/v2/entry/fuselagetown/staticmantest/gh-pages/comments/" id="firstform">
  <input name="options[redirect]" type="hidden" value="https://stitchfix-prototype.netlify.com/clients/kid">
  <!-- e.g. "2016-01-02-this-is-a-post" -->
  <input name="options[slug]" type="hidden" value="{{ page.slug }}">
  <input name="fields[title]" type="text" value="Emilia">
  <input name="fields[type]" type="text" value="parent">
</form>
<form  action="https://api.staticman.net/v2/entry/fuselagetown/staticmantest/gh-pages/comments/" id="secondform">
  <input name="options[redirect]" type="hidden" value="https://stitchfix-prototype.netlify.com/clients/kid">
  <!-- e.g. "2016-01-02-this-is-a-post" -->
  <input name="options[slug]" type="hidden" value="{{ page.slug }}">
  <input name="fields[title]" type="text" value="Torunn">
  <input name="fields[type]" type="text" value="kid">
</form>

  <button type="submit" id="subbut">Go!</button>
</div>


<script language="javascript">
$(document).ready(function() {
    $("#subbut").click(function() {
        $.post($("#firstform").attr("action"), $("#firstform").serialize()+$("#secondform").serialize(),
              function() {
                alert('Both forms submitted');
              });
      });
  });
</script>
