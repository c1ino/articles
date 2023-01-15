
[test-cmt]
{{site.data.test_cmt|size}}




<table>
{% for x in site.data.test_cmt -%}
  <tr>
    <td> {{x.id}} / {{x.issue_url}} </td>
    <td> {{x.updated_at}} / {{x.created_at}} </td>
    <td> 
      
{{x.body}} </td>
  </tr>
{%endfor%}
</table>
