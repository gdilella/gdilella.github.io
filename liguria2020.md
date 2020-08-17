---
title: Italian Polls
---

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/1.10.21/css/jquery.dataTables.css">
<script type="text/javascript" charset="utf8" src="https://cdn.datatables.net/1.10.21/js/jquery.dataTables.js"></script>

{% assign sondaggi=site.data.liguria_polls %}

<h1> Elezioni Regionali Liguria 2020 </h1>

<img src="prob_Liguria.svg" class="center">

<img src="trend_Liguria.svg" class="center"> 

<table id="polls" class="display compact" data-page-length='10' data-order='[[ 3, "desc" ]]'>
    <thead>
    <tr>
    <th rowspan="2">Istituto</th>
    <th rowspan="2">Committente</th>
    <th rowspan="2">Data iniziale</th>
    <th rowspan="2">Data finale</th>
    <th rowspan="2">Campione</th>
    <th>Toti</th>
    <th>Sansa</th>
    <th>Salvatore</th>
    <th rowspan="2">Altri</th>
    <th rowspan="2">Indecisi</th>
    </tr>
    <tr>
    <th style="background:#afc9fd;"></th>
    <th style="background:#f47c8b;"></th>
    <th style="background:#fae3a5;"></th>
    </tr>
    </thead>
    <tbody>
    {% for row in sondaggi %}
        <tr>
        {% for cell in row %}
            <td class="dt-body-center">{{ cell[1] }}</td>
        {% endfor %}
        </tr>
    {% endfor %}
    </tbody>
</table>

<script type="text/javascript">
$(document).ready( function () {
    $('#polls').DataTable({
        "ordering": false,
        "searching": false,
        "lengthChange": false});
} );
</script>