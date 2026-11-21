---
layout: page
permalink: /cv/
title: cv
nav: true
nav_order: 3
---

{% assign cv_url = '/assets/pdf/CV_Aaditya_Chandrasekhar.pdf' | relative_url %}

<p>
  <a class="btn btn-sm z-depth-0" role="button" href="{{ cv_url }}" target="_blank" rel="noopener">
    <i class="fa-solid fa-up-right-from-square"></i> Open in new tab
  </a>
  <a class="btn btn-sm z-depth-0" role="button" href="{{ cv_url }}" download>
    <i class="fa-solid fa-file-pdf"></i> Download PDF
  </a>
</p>

<div style="width: 100%; height: 85vh; min-height: 600px;">
  <iframe src="{{ cv_url }}#view=FitH" title="CV of Aaditya Chandrasekhar" style="width: 100%; height: 100%; border: 1px solid var(--global-divider-color);">
  </iframe>
</div>

<p class="mt-2"><small>If the CV does not display on your device, use the buttons above to open or download it.</small></p>
