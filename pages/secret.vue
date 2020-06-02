<template>
  <div class="content">
    <img :src="user.picture"/>
    <p>Hi {{ user.email }}!</p>
    <p>This is a super secure page! Try loading this page again using the incognito/private mode of your browser.</p>
    
<link href="//cdn-images.mailchimp.com/embedcode/horizontal-slim-10_7.css" rel="stylesheet" type="text/css">
<style type="text/css">
	#mc_embed_signup{background:#fff; clear:left; font:14px Helvetica,Arial,sans-serif; width:100%;}
	/* Add your own Mailchimp form style overrides in your site stylesheet or in this style block.
	   We recommend moving this block and the preceding CSS link to the HEAD of your HTML file. */
</style>
<div id="mc_embed_signup">
<form action="https://tech.us4.list-manage.com/subscribe/post?u=b7f1f1fabdcb0ea3db6d7bd95&amp;id=f540d4b02e" method="post" id="mc-embedded-subscribe-form" name="mc-embedded-subscribe-form" class="validate" target="_blank" novalidate>
    <div id="mc_embed_signup_scroll">
	<label for="mce-EMAIL">Subscribe</label>
	<input type="email" value="" name="EMAIL" class="email" id="mce-EMAIL" placeholder="email address" required>
    <!-- real people should not fill this in and expect good things - do not remove this or risk form bot signups-->
    <div style="position: absolute; left: -5000px;" aria-hidden="true"><input type="text" name="b_b7f1f1fabdcb0ea3db6d7bd95_f540d4b02e" tabindex="-1" value=""></div>
    <div class="clear"><input type="submit" value="Subscribe" name="subscribe" id="mc-embedded-subscribe" class="button"></div>
    </div>
     </form>
     </div>

  </div>
</template>

<script>
export default {
  middleware: 'auth',
  computed: {
    user() {
      return this.$auth.user
    }
  }
}
</script>

<style scoped>
.content {
  text-align: center;
  padding-top: 20px;
}
img {
  width: 100px;
  height: 100px;
  border-radius: 100px;
  margin: 15px 0;
}
</style>
