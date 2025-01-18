# 线下赛

|比赛|日期|净成绩|成绩证书|
|---|---|---|---|
{% for item in site.data.real_cert %}
|{{ item.name }}|{{ item.date }}|{{ item.time }}|<iframe title="{{ item.name }}的成绩证书" src="https://m.mararun.com/html/certificate.html?id={{ item.cert }}"></iframe>{{ item.cert }}|
{% endfor %}
