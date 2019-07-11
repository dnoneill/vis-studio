---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: reveal
---
<link rel="stylesheet" href="https://revealjs.com/css/theme/white.css" id="theme">


{% for slide in site.slides %}

{% if slide.website %}

<section>
	{{slide.website}}
</section>
{% elsif slide.type == 'script' %}
<section>
	{{slide.content | replace: "true", "false"}}
</section>
{% else %}
<section class="center">
	<h1>{{slide.title}}</h1>
{{slide.content | replace: "iframe", "div" | replace: "fixed", "relative"}}
</section>
{% endif %}
{% endfor %}
<style>
	.iiifannotation {
		height: 85vh;
		overflow: auto;
	}
	code {
		word-wrap: break-word!important;
		white-space: normal;
		word-break: break-all;
	}
	section {
	font-size: calc(1vw + 2.5vh);
	}
</style>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.4.1/jquery.js" integrity="sha256-WpOohJOqMqqyKL9FccASB9O0KwACQJpFTUBLTYOVvVU=" crossorigin="anonymous"></script>