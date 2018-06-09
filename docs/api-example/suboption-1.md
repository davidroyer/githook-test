---
description: Subpage for page 1
---

# Suboption 1

{% hint style="info" %}
This is an info block
{% endhint %}



{% hint style="warning" %}
Warning message!
{% endhint %}

### Code Example 1

{% code-tabs %}
{% code-tabs-item title="MainWrapper.vue" %}
```markup
<template>
    <div class="container mx-auto max-w-md px-4 py-16">
        <slot></slot>
    </div>
</template>
```
{% endcode-tabs-item %}

{% code-tabs-item title=undefined %}
```

```
{% endcode-tabs-item %}
{% endcode-tabs %}

### Code Example 2 - Multiple Files

{% code-tabs %}
{% code-tabs-item title="NavLinks.vue" %}
```markup
<template>
  <ul class="flex justify-end list-reset">
    <template v-for="(link, i) in links">
      <nav-link :key="i" :to="link.path" :name="link.name"></nav-link>
    </template>
  </ul>
</template>

<script>
import NavLink from "./NavLink.vue";

export default {
  name: 'NavLinks',
  components: {
    NavLink
  },
  props: ["links"]
};
</script>

```
{% endcode-tabs-item %}

{% code-tabs-item title="NavLink.vue" %}
```markup
<template>
  <li class="block px-4">
    <nuxt-link :to="to" class="nav-link hover:border-grey">{{ name }}</nuxt-link>
  </li>
</template>

<script>
export default {
  name: 'NavLink',
  props: ["to", "name"]
};
</script>
```
{% endcode-tabs-item %}
{% endcode-tabs %}



