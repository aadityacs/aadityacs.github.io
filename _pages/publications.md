---
layout: page
permalink: /publications/
title: publications
description: Journal articles, preprints and patents in reverse chronological order. The DOI button opens the published version.
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

{% include bib_search.liquid %}

<div class="publications">

{% bibliography %}

</div>

<h2 id="patents" class="mt-5">patents</h2>

<div class="publications">

{% bibliography --file patents --group_by none %}

</div>
