

test site.data.json

[obj.json]
{{site.data.obj|inspect}}

[test-cmt]
{{site.data.test_cmt|size}}



|id|time|body| 
{% for x in site.data.test_cmt -%}
| {{x.id}} | {{x.updated_at}} | {{x.body|markdownify|strip_newlines-}} | 
{%endfor%}


[test escape]
```
{{site.data.test_cmt[0]|markdownify}}
```
```
{{site.data.test_cmt[0]|markdownify|strip_newlines}}
```
```
{{site.data.test_cmt[0]|markdownify|newline_to_br}}
```
