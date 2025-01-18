# 线下赛

{% assign data = site.data.real_cert | sort: 'date' %}
<table>
    <thead>
        <tr>
            <th>比赛</th>
            <th>日期</th>
            <th>净成绩</th>
            <th>奖牌收纳瓶编号</th>
            <th>成绩证书</th>
        </tr>
    </thead>
    <tbody>
        {% for item in data %}
        <tr>
            <td>{{ item.name }}</td>
            <td>{{ item.date}}</td>
            <td>{{ item.time}}</td>
            <td>{{ item.medal}}</td>
            <td><iframe src="https://m.mararun.com/html/certificate.html?id={{ item.cert }}"></iframe></td>
        </tr>
        {% endfor %}
    </tbody>
</table>
