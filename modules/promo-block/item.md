{% extends 'docs/modules/item-default.md' %}

{% block method_list %}
{{ parent() }}

### getPageUrl(_[$sPageCode = 'promo-block'']_)
  * $sPageCode - page file name

Method returns URL of promo block page.
Method gets PromoBlockPage component attached on page and compiles parameter :slug to generate page URL.
{% endblock %}