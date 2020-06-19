---
title: Italian Polls
---

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/1.10.21/css/jquery.dataTables.css">
<script type="text/javascript" charset="utf8" src="https://cdn.datatables.net/1.10.21/js/jquery.dataTables.js"></script>

{% assign sondaggi=site.data.puglia_polls %}

# Elezioni Regionali Puglia 2020

<img src="trend_puglia.png" class="center"> 

<table id="ge_polls" class="display compact" data-page-length='10' data-order='[[ 3, "desc" ]]'>
    <thead>
    <tr>
    <th rowspan="2">Istituto</th>
    <th rowspan="2">Committente</th>
    <th rowspan="2">Inizio</th>
    <th rowspan="2">Fine</th>
    <th rowspan="2">Campione</th>
    <th>Emiliano</th>
    <th>Fitto</th>
    <th>Bellanova</th>
    <th>Laricchia</th>
    <th rowspan="2">Altri</th>
    </tr>
    <tr>
    <th style="background:#f47c8b;"></th>
    <th style="background:#afc9fd;"></th>
    <th style="background:#d173aa;"></th>
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
    $('#ge_polls').DataTable({
        "ordering": false,
        "searching": false,
        "lengthChange": false,
        "paging":   false,
        "info":     false});
        });
</script>
