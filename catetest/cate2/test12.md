

test site.data.json

[obj.json]
{{site.data.obj|inspect}}

[test-cmt]
{{site.data.test_cmt|size}}

|id|time|body|
{% for x in site.data.test_cmt %}
|{{x.id}}|{{x.updated_at}}|{{x.body|strip_newlines}}|
{%endfor%}
