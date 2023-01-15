

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
{{site.data.test_cmt[0].body|markdownify|replace:"|","\|"}}
```

|1|2|
|-|-|
| {{site.data.test_cmt[0].body|markdownify|replace:"|","\|"}} |2|


```
{{site.data.test_cmt[0].body|markdownify|strip_newlines|replace:"|","\|"}}
```

|1|2|
|-|-|
| {{site.data.test_cmt[0].body|markdownify|strip_newlines|replace:"|","\|"}} |2|


```
{{site.data.test_cmt[0].body|markdownify|replace: "\r",""}}
```

|1|2|
|-|-|
|  {{site.data.test_cmt[0].body|markdownify|replace: "\r",""}}  |2|



[test table]

|1|2|
|-|-|
|<img> <input> <button>[but]</button> | eot |

|1|2|
|-|-|
|<ul><li>3a</li></ul> <ul><li><ul><li>3b</li></ul></li></ul> | eot |

|1|2|
|-|-|
|<ul><li>3a</li></ul>| eot |

|1|2|
|-|-|
| <ul><li><ul><li>3b</li></ul></li></ul> | eot |
