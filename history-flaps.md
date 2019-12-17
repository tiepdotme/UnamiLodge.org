---
title: Lodge Flaps
layout: page
permalink: /history/flaps
---

<div class="row">
{% for flap in site.data.history-flaps %}
  {% unless flap.variety =='X' %}
  <div class="col-md-3 col-sm-4 mb-3">
    <div class="card h-100">
      {% picture flap /img/flaps/{{ flap.variety | downcase }}{{flap.issue}}.{{flap.extension}} --img class="card-img-top" --link /history/flaps/{{flap.variety}}{{flap.issue}} %}
      <div class="card-body text-center py-2">
        <h4 class="card-title mb-0">
          <a href="/history/flaps/{{flap.variety}}{{flap.issue}}">
          {{flap.variety}}{{flap.issue}}
          </a>
        </h4>
      </div>
    </div>
  </div>
  {% endunless %}
{% endfor %}
</div>
