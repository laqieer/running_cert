# 线下赛

{% for group in site.data.real_cert %}
## 奖牌收纳罐编号：{{ group.group }}
{% for medal in group.medals %}
### {{ medal.race }}
比赛日期：{{ medal.date }}{% if medal.time != null and medal.time != "" %}，净成绩：{{ medal.time }}{% endif %}

{% if medal.cert != null and medal.cert != "" %}
成绩证书：
<iframe src="https://m.mararun.com/html/certificate.html?id={{ medal.cert }}"></iframe>
{% endif %}
{% if medal.activity != null and medal.activity != "" %}
运动记录：
<div class="strava-embed-placeholder" data-embed-type="activity" data-embed-id="{{ medal.activity }}" data-style="standard"></div><script src="https://strava-embeds.com/embed.js"></script>
{% endif %}
{% endfor %}
{% endfor %}
