---
layout: base
body-class: home
permalink: /home-alt-4/
hero-image: /assets/img/hero-image.jpg
hero-text: "Helping federal agencies accelerate innovation through crowdsourcing and citizen science. "
hero-button-text: Learn more
hero-button-link: /about/
banner-heading: Citizenscience.gov is an official government website designed to accelerate the use of crowdsourcing and citizen science across the U.S. government.
banner-text: In citizen science, the public participates voluntarily in the scientific process, addressing real-world problems.
banner-button-text: 
banner-button-link: /about/
---

<section>
  <div class="hero-unit hero-unit-alt-2" style="background-image: url('{{ page.hero-image | prepend: site.baseurl }}')">
    <div class="usa-grid">
      <div class="usa-width-whole hero-content">
        <h1 style="padding-top: .65em;">{{ page.hero-text }}</h1>
          <div class="usa-grid-whole alt-button-section">
        <a class="usa-button usa-button-big" style="font-size: 22px; line-height: 35px; " href="{{ page.hero-button-link | prepend: site.baseurl }}">Learn</a>
    		<a class="usa-button usa-button-big" style="font-size: 22px; line-height: 35px; " href="{{ page.hero-button-link | prepend: site.baseurl }}">Participate<br> in a Project</a>
    		<a class="usa-button usa-button-big" style="font-size: 22px; line-height: 35px; " href="{{ page.hero-button-link | prepend: site.baseurl }}">Build and<br> Manage a Project</a>
        <a class="usa-button usa-button-big" style="font-size: 22px; line-height: 35px; " href="{{ page.hero-button-link | prepend: site.baseurl }}">Join our<br> Community</a>
  </div>
      </div>
    </div>
  </div>
</section>

<section class="usa-grid">

</section>

{% comment %}
Blog Section
{% endcomment %}
<section class="usa-grid usa-section">
    <h1 class="page-heading">Blog</h1>
    {% for post in site.posts limit: 3 %}
    <div class="usa-grid  blog-section">
        <div class="usa-width-one-third blog-list-image"><img src="{{ post.image | prepend: site.baseurl }}" alt="{{ post.title }}"   title="{{ post.title }}"></div>
        <div class="usa-width-two-thirds">
      <ul>
          <li>
            <h3>
              <a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a>
            </h3>
            By: {{ post.author}}</br>
            {{ post.date | date_to_long_string }}
            {{ post.excerpt | truncatewords: 35 }}
          </li>
      </ul>
    </div>
  </div>
        {% endfor %}
<a class="card-read" href="{{ site.baseurl }}/blog/">
        more blog stories
        <span class="usa-sr-only">about {{ page.title }}</span>
      </a>
</section>

{% include contact.html %}
