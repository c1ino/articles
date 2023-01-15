[test-data]
{{site.data|size}}

{%for x in size.data%}
- {{forloop|inspect}}
{%-endfor%}

[test-folder]
{{site.data.folder|size}}


[test-cmt]
{{site.data.test_cmt|size}}


[md]
|id/time|body| 
|-|-|
{% for x in site.data.test_cmt -%}
| [{{x.id}}]({{x.html_url}}) <br>{{x.created_at}}<br>{{x.updated_at}} | {{x.body|markdownify|strip_newlines-}} | 
{%endfor%}




[html]
<table>
{% for x in site.data.test_cmt -%}
  <tr>
    <td> 
      
[{{x.id}}]({{x.html_url}})

{{x.created_at}}<br>{{x.updated_at}}</td>
    <td> 
      
{{x.body}}</td>
  </tr>
{%endfor%}
</table>
