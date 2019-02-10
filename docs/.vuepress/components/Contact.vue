<template>
<div class="contact">
  <div class="contact-info">
    <a :href="`mailto:${$page.frontmatter.contact.email.value}`"><icon :icon="$page.frontmatter.contact.email.icon"/></a>
    <p>{{ $page.frontmatter.contact.email.value }}</p>
 </div>
 <div class="contact-info">
    <a :href="`tel:${$page.frontmatter.contact.phone.value}`"><icon :icon="$page.frontmatter.contact.phone.icon"/></a>
    <p>{{ $page.frontmatter.contact.phone.value }}</p>
  </div>
  <div class="social">
      <a class="grid" v-for="s in $page.frontmatter.contact.social" :href="s.link">
        <icon :icon="s.icon"/>
        <span v-text="s.text"></span>
      </a>
  </div>
</div>
</template>

<script>
import Icon from './Icon.vue';
export default {
  components: { Icon },
};
</script>

<style>
.main {
  font-size: 14.5px;
}
.main .content {
  max-width: 800px;
  padding: 1em;
}
.main .content > *:first-child {
  margin: 0;
}
.grid {
  display: grid;
}
.contact {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
}
.social {
  display: flex;
  align-items: center;
}
.social > * {
  padding: 1em;
}
.contact-info {
  display: flex;
  justify-items: center;
  align-items: center;
}
.contact-info p {
  margin: 0;
}
.contact-info > * {
  padding: 1em;
  white-space: nowrap;
}
.main-header h1 {
  margin-bottom: 0;
}
</style>