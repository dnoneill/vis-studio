---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: reveal
---
{% for slide in site.slides %}

{% if slide.website %}

<section data-background-iframe="{{slide.website}}" data-background-interactive>
</section>
{% elsif slide.type == 'script' %}
<section>
	{{slide.content}}
</section>
{% else %}
<section class="center">
	<h1>{{slide.title}}</h1>
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
	font-size: calc(1.5vh + 1.5vh);
	}
</style>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.4.1/jquery.js" integrity="sha256-WpOohJOqMqqyKL9FccASB9O0KwACQJpFTUBLTYOVvVU=" crossorigin="anonymous"></script>