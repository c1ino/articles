

test site.data.json

[obj.json]
{{site.data.obj|inspect}}

[test-cmt]
{{site.data.test_cmt|size}}




<table>
{% for x in site.data.test_cmt -%}
  <tr>
    <td> {{x.id}} </td>
    <td> {{x.updated_at}} </td>
    <td> 
{{x.body}} </td>
  </tr>
{%endfor%}
</table>



{%comment%}
|id|time|body| 
|-|-|-|
{% for x in site.data.test_cmt -%}
| {{x.id}} | {{x.updated_at}} | {{x.body|markdownify|strip_newlines-}} | 
{%endfor%}
{%endcomment%}



{%comment%}
|id|time|body| 
|-|-|-|
{% for x in site.data.test_cmt -%}
| {{x.id}} | {{x.updated_at}} | {{x.body|newline_to_br|strip_newlines-}} | 
{%endfor%}
{%endcomment%}


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

|1|2|
|-|-|
|3<br>4| eot |

|1|2|
|-|-|
|- 3 <br/> - 4| eot |
