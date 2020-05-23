![Image](trend.png)
Fonte: Sondaggi presi da [Europe Elects](https://europeelects.eu/european-union/italy/). Trend ottenuto tramite [LOWESS](https://en.wikipedia.org/wiki/Local_regression) 

![Image](voto.png)

{% assign mydata=site.data.ge_polls %}

<table>
    <caption>Table caption</caption>
    <thead>
    {% for column in mydata[0] %}
        <th>{{ column[0] }}</th>
    {% endfor %}
    </thead>
    <tbody>
    {% for row in mydata %}
        <tr>
        {% for cell in row %}
            <td>{{ cell[1] }}</td>
        {% endfor %}
        </tr>
    {% endfor %}
    </tbody>
</table>
