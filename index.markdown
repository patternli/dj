---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---


{% for post in site.data.contentful.davyjones.post %}
# {{ post.title}}
{{ post.body }}
### Related Art
{% for a in post.art%} 
{{ a.title }}
<img src="{{ a.image.url }}" style="max-width: 200px" />
{% endfor %}

### Check out these products
{% for prod in post.product %}
<a href="/{{ prod.slug}}">{{ prod.title }}</a>

{{ prod.short }}
{% endfor %}


{% endfor %}