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

{%
#{{site.collections|inspect}}
%}

{{site.categories|jsonify}}

{{site.pages|jsonify}}

{{site.documents|jsonify}}

{{page|jsonify}}
