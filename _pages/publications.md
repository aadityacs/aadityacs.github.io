---
layout: page
permalink: /publications/
title: publications
nav: true
nav_order: 2
---

<style>
  .publications h2.bibliography { color: var(--global-text-color-light); }
</style>

<div class="publications">

{% bibliography %}

</div>

<h2 id="patents" class="mt-5">patents</h2>

<div class="publications">

{% bibliography --file patents --group_by none %}

</div>
