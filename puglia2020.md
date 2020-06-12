---
title: Italian Polls
---

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/1.10.21/css/jquery.dataTables.css">
<script type="text/javascript" charset="utf8" src="https://cdn.datatables.net/1.10.21/js/jquery.dataTables.js"></script>

{% assign sondaggi=site.data.puglia_polls %}

# Elezioni Regionali Puglia 2020

<img src="trend_puglia.png" class="center"> 

<table id="past_elections" class="display compact">
<thead>
    <tr>
    <th rowspan="2">Elezioni</th>
    <th>Centrosinistra</th>
    <th>Centrodestra</th>
    <th>Movimento 5 Stelle</th>
    <th rowspan="2">Altri</th>
    <th rowspan="2">Vantaggio</th>
    </tr>
    <tr>
    <th style="background:#f47c8b;"></th>
    <th style="background:#afc9fd;"></th>
    <th style="background:#fae3a5;"></th>
    </tr>
</thead>
<tbody>
<tr>
<td class="dt-body-center">Regionali 2015</td>
<td class="dt-body-center">47,12</td>
<td class="dt-body-center">14,40</td>
<td class="dt-body-center">18,42</td>
<td class="dt-body-center">20,06</td>
<td class="dt-body-center" style="background:#f47c8b; color:white; font-weight: bold;">+27 Centrosinistra</td>
</tr>
<tr>
<td class="dt-body-center">Politiche 2018</td>
<td class="dt-body-center">16,10</td>
<td class="dt-body-center">32,17</td>
<td class="dt-body-center">44,94</td>
<td class="dt-body-center">6,79</td>
<td class="dt-body-center" style="background:#fae3a5; font-weight: bold;">+12 Movimento 5 Stelle</td>
</tr>
<tr>
<td class="dt-body-center">Europee 2019</td>
<td class="dt-body-center">24,6</td>
<td class="dt-body-center">45,29</td>
<td class="dt-body-center">26,29</td>
<td class="dt-body-center">3,82</td>
<td class="dt-body-center" style="background:#afc9fd; color:white; font-weight: bold;">+19 Centrodestra</td>
</tr>
</tbody>
</table>

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
        
    $('#past_elections').DataTable({
        "ordering": false,
        "searching": false,
        "lengthChange": false,
        "paging":   false,
        "info":     false});
});
</script>
