# 线上赛

{% for group in site.data.virtual_cert %}
## 奖牌收纳罐编号：{{ group.group }}
{% for race in group.races %}
### {{ race.race }}
{% if race.note != null %}
{{ race.note }}
{% else %}

{% for medal in race.medals %}
- {{ medal }}
{% endfor %}

![]({{ site.baseurl }}/assets/images/成绩证书/{{ group.group }}/{{ race.race }}.jpg)
{% if group.group | starts_with: "数字心动" %}
![]({{ site.baseurl }}/assets/images/电子号码布/{{ group.group }}/{{ race.race }}.jpg)
{% if race.hasVirtualMedal %}
![]({{ site.baseurl }}/assets/images/电子奖牌/{{ group.group }}/{{ race.race }}.jpg)
{% endif %}
{% endif %}

{% endif %}
{% endfor %}
{% endfor %}
