---
date: 2023-01-07
collection: test
---
test cate 11 page


[path]
{{page.path}}

[cate]
{{page.categories}}

[collection]
{{page.collection}}

[dir]
{{page.dir}}
{{page.dir|split:"/"|inspect}}

[name]
{{page.name}}

{%raw%}
{{site.collections|inspect}}
{%endraw%}

[categories]
{{site.categories|inspect}}

[pages]
{{site.pages|inspect}}

[documents]
{{site.documents|inspect}}

[posts]
{{site.posts|inspect}}

{%raw%}
[static_files]
{{site.static_files|inspect}}
{%endraw%}

[page]
{{page|inspect}}
