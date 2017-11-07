---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
---
<a href="#" class="cookie">do we have javascript?</a>

<div style="background: red">
<form  action="https://api.staticman.net/v2/entry/fuselagetown/staticmantest/gh-pages/comments/" id="firstform">
 
  <input name="options[slug]" type="hidden" value="{{ page.slug }}">
  <input name="fields[title]" type="text" value="Emilia">
  <input name="fields[type]" type="text" value="parent">
</form>
<form  action="https://api.staticman.net/v2/entry/fuselagetown/staticmantest/gh-pages/comments/" id="secondform">

  <input name="options[slug]" type="hidden" value="{{ page.slug }}">
  <input name="fields[title]" type="text" value="Torunn" id="kids-first-name">
  <input name="fields[type]" type="text" value="kid">
</form>

  <button type="submit" id="subbut">Go!</button>
</div>

<div id="msg"></div>

<script>

$(document).ready(function() {
    $("#subbut").click(function() {
    	var firstName = $("#kids-first-name").val();
        $.post($("#firstform").attr("action"), $("#firstform").serialize(),
          function(data) {
            $("#msg").append(data);
            $.post($("#secondform").attr("action"), $("#secondform").serialize(),
              function(data) {
                $("#msg").append(data);
                 window.location.href = 'https://stitchfix-prototype.netlify.com/clients/' + firstName;
              });
          });

      });
  });

</script>
