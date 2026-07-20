{% assign spritz_entries = site.data.spritz | sort: 'sort_order' %}
{% for spritz in spritz_entries %}
{% if spritz.row_type == 'header' %}
| **{{ spritz.name }}** |  |  |  |  |
{% else %}
| {{ spritz.name }} | {% if spritz.telegram_url %}[{{ spritz.telegram_label }}]({{ spritz.telegram_url }}){% endif %} | {% if spritz.x_url %}[{{ spritz.x_label }}]({{ spritz.x_url }}){% endif %} | {% if spritz.website_url %}[{{ spritz.website_label }}]({{ spritz.website_url }}){% endif %} | {% if spritz.nostr_url %}[{{ spritz.nostr_label }}]({{ spritz.nostr_url }}){% endif %} |
{% endif %}
{% endfor %}
