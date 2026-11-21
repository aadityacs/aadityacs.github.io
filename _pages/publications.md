---
layout: page
permalink: /publications/
title: publications
nav: true
nav_order: 2
---

<style>
  .publications h2.bibliography { color: var(--global-text-color-light); }
  .patents .preview { background: #fff; padding: 8px; height: 70px; width: 100%; object-fit: contain; }
</style>

<div class="publications">

{% bibliography %}

</div>

<h2 id="patents" class="mt-5">patents</h2>

<div class="publications patents">

{% bibliography --file patents --group_by none %}

</div>

<p style="text-align: right; font-size: 0.8rem;">* Equal contribution</p>
