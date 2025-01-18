# 线下赛

{% assign data = site.data.real_cert | sort: 'date' %}
<table>
    <thead>
        <tr>
            <th>比赛</th>
            <th>日期</th>
            <th>净成绩</th>
            <th>奖牌收纳罐编号</th>
            <th>成绩证书</th>
            <th>运动记录</th>
        </tr>
    </thead>
    <tbody>
        {% for item in data %}
        <tr>
            <td>{{ item.name }}</td>
            <td>{{ item.date}}</td>
            <td>{{ item.time}}</td>
            <td>{{ item.medal}}</td>
            <td><iframe style="height: 100%;" src="https://m.mararun.com/html/certificate.html?id={{ item.cert }}"></iframe></td>
            <td>{% if item.activity != null and item.activity != "" %}<div class="strava-embed-placeholder" data-embed-type="activity" data-embed-id="{{ item.activity }}" data-style="standard"></div><script src="https://strava-embeds.com/embed.js">{% endif %}</script></td>
        </tr>
        {% endfor %}
    </tbody>
</table>
