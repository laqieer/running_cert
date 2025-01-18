# 线下赛

| 比赛 | 日期 | 净成绩 | 成绩证书 |
| --- | --- | --- | --- |
{% for item in site.data.real_cert %}
| {{ item.name }} | {{ item.date }} | {{ item.time | time: '%H:%M:%S' }} | <iframe src="https://m.mararun.com/html/certificate.html?id={{ item.cert }}"></iframe> |
{% endfor %}
