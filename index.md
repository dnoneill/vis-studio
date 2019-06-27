---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: reveal
---

{% for slide in site.slides %}
{% if slide.website %}
<section data-background-iframe="{{slide.website}}" data-background-interactive>
</section>
{% else %}
<section>
	<h2>{{slide.title}}</h2>
{{slide.content}}
</section>
{% endif %}
{% endfor %}

<style>
	.iiifannotation {
		height: 100vh;
		overflow: auto;
	}
	section {
	top: 0px!important;
	font-size: calc(1.5vh + 1.5vh);
	}
</style>