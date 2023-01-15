

test site.data.json

[obj.json]
{{site.data.obj|inspect}}

[test-cmt]
{{site.data.test_cmt|size}}



|id|time|body| 
|-|-|-|
{% for x in site.data.test_cmt -%}
| {{x.id}} | {{x.updated_at}} | {{x.body|markdownify|strip_newlines-}} | 
{%endfor%}


[test escape]

```
{{site.data.test_cmt[0].body|markdownify}}
```

|1|2|
|-|-|
| {{site.data.test_cmt[0].body|markdownify}} |2|


```
{{site.data.test_cmt[0].body|markdownify|strip_newlines}}
```

|1|2|
|-|-|
| {{site.data.test_cmt[0].body|markdownify|strip_newlines}} |2|


```
{{site.data.test_cmt[0].body|markdownify|replace: "\n"," "}}
```

|1|2|
|-|-|
|  {{site.data.test_cmt[0].body|markdownify|replace: "\r\n",""}}  |2|



[test table]

|1|2|
|-|-|
|<img> <input> <button>[but]</button> | eot |
