[test-data]
{{site.data|size}}

/*
{%for x in site.data%}
[x]
{{x[0]}} / {{x[1]|size}}
[forloop]
{{forloop|inspect}}
{%endfor%}
*/

[test-folder]
{{site.data.folder|size}}


[test-cmt]
{{site.data.test_cmt|size}}



[md]
|id/time|body| 
|-|-|
{% for x in site.data.test_cmt reversed-%}
| [{{x.id}}]({{x.html_url}}) <br>{{x.created_at}}<br>{{x.updated_at}} | {{x.body|markdownify|strip_newlines-}} | 
{%endfor%}



{%comment%}
[tablerow]
<table>
{% tablerow x in site.data.test_cmt %}
  {{ product.title }}
{% endtablerow %}
</table>
{%endcomment%}


[html]
<table>
{% for x in site.data.test_cmt reversed-%}
  <tr>
    <td> 
      
[{{x.id}}]({{x.html_url}})

{{x.created_at}}<br>{{x.updated_at}}</td>
    <td> 
      
{{x.body}}</td>
  </tr>
{%endfor%}
</table>
