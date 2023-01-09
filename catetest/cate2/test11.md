---
date: 2023-01-07
collection: test
---
test cate 11 page


{{page.path}}

[cate]{{page.categories}}

[collection]{{page.collection}}

{{page.dir}}

{{page.name}}

{%comment%}
{{site.collections|inspect}}
{%endcomment%}

[categories]
{{site.categories|jsonify}}

[pages]
{{site.pages|jsonify}}

[documents]
{{site.documents|jsonify}}

[page]
{{page|jsonify}}
