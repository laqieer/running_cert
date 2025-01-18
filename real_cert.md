# 线下赛

```markdown
{% assign data = site.data.real_cert | sort: 'date' %}
| 比赛 | 日期 | 净成绩 | 成绩证书 |
| --- | --- | --- | --- |
{% for item in data %}
| {{ item.name }} | {{ item.date | date: '%Y-%m-%d' }} | {{ item.time | date: '%H:%M:%S' }} | <iframe src="https://m.mararun.com/html/certificate.html?id={{ item.cert }}"></iframe> |
{% endfor %}
```
