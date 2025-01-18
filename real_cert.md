# 线下赛

{% assign data = site.data.real_cert | sort: 'date' %}
<table style="width:100%">
    <thead>
        <tr>
            <th>比赛</th>
            <th>日期</th>
            <th>净成绩</th>
            <th style="width:50%">成绩证书</th>
        </tr>
    </thead>
    <tbody>
        {% for item in data %}
        <tr>
            <td>{{ item.name }}</td>
            <td>{{ item.date | date: '%Y-%m-%d' }}</td>
            <td>{{ item.time | date: '%H:%M:%S' }}</td>
            <td><iframe src="https://m.mararun.com/html/certificate.html?id={{ item.cert }}"></iframe></td>
        </tr>
        {% endfor %}
    </tbody>
</table>
