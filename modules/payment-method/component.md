{% extends 'docs/modules/component-default.md' %}

{% block content %}

* [PaymentMethodList](#paymentmethodlist)
  * [make](#makearelementidlist-null)

## PaymentMethodList

Component allows you to render blocks with available payment methods.

### make(_[$arElementIDList = null]_)

**Example:** Get collection of payment methods, apply sorting + filter by flag "active"
{% verbatim %}
```twig
[PaymentMethodList]
==
{# Get PaymentMethodCollection object from PaymentMethodList component #}
{% set obPaymentMethodList = PaymentMethodList.make().sort().active() %}
{% if obPaymentMethodList.isNotEmpty() %}
    <div>
        {% for obPaymentMethod in obPaymentMethodList %}
            <div data-id="{{ obPaymentMethod.id }}">
                <div>{{ obPaymentMethod.name }}</div>
                <div>{{ obPaymentMethod.preview_text }}</div>
            </div>
        {% endfor %}
    </div>
{% endif %}
```
{% endverbatim %}
{% endblock %}