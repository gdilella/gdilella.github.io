---
title: Italian Polls
---

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/1.10.21/css/jquery.dataTables.css">
<script type="text/javascript" charset="utf8" src="https://cdn.datatables.net/1.10.21/js/jquery.dataTables.js"></script>

{% assign polls=site.data.houses %}

<center><h1> Istituti di ricerca </h1></center>
<center><h3> Statistiche e bias dei vari sondaggisti italiani </h3></center>

<center>
<table id="polls" class="display compact" data-order='[[ 11, "desc" ]]' data-page-length='25'>
    <thead>
    <tr>
    <th rowspan="2">Istituto</th>
    <th>Lega</th>
    <th>PD</th>
    <th>M5S</th>
    <th>FdI</th>
    <th>FI</th>
    <th>Sinistra</th>
    <th>+Europa</th>
    <th>Verdi</th>
    <th>Azione</th>
    <th>IV</th>
    <th rowspan="2">Sondaggi</th>
    </tr>
    <tr>
    <th style="background:#a8d291;"></th>
    <th style="background:#f47c8b;"></th>
    <th style="background:#fae3a5;"></th>
    <th style="background:#3d6a99;"></th>
    <th style="background:#afc9fd;"></th>
    <th style="background:#f05b5b;"></th>
    <th style="background:#fcbc7d;"></th>
    <th style="background:#81de81;"></th>
    <th style="background:#2a58b5;"></th>
    <th style="background:#d173aa;"></th>
    </tr>
    </thead>
    <tbody>
    {% for row in polls %}
        <tr>
        {% for cell in row %}
            <td class="dt-body-center">{{ cell[1] }}</td>
        {% endfor %}
        </tr>
    {% endfor %}
    </tbody>
</table>
</center>


<script type="text/javascript">
$(document).ready( function () {
    $('#polls').DataTable({
        "searching": false,
        "lengthChange": false,
        "paging": false,
        "info":     false});
} );
</script>
