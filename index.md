<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/1.10.21/css/jquery.dataTables.css">
<script type="text/javascript" charset="utf8" src="https://cdn.datatables.net/1.10.21/js/jquery.dataTables.js"></script>

{% assign ge_polls=site.data.ge_polls %}

![Image](trend.png)
Fonte: Sondaggi presi da [Europe Elects](https://europeelects.eu/european-union/italy/). Trend ottenuto tramite [LOWESS](https://en.wikipedia.org/wiki/Local_regression) 

![Image](voto.png)



<table id="ge_polls" class="display" data-page-length='25'>
    <thead>
    {% for column in ge_polls[0] %}
        <th>{{ column[0] }}</th>
    {% endfor %}
    </thead>
    <tbody>
    {% for row in ge_polls %}
        <tr>
        {% for cell in row %}
            <td>{{ cell[1] }}</td>
        {% endfor %}
        </tr>
    {% endfor %}
    </tbody>
</table>

<script type="text/javascript">
$(document).ready( function () {
    $('#ge_polls').DataTable();
} );
</script>
