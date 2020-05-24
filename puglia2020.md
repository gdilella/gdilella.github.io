---
title: Italian Polls
---

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/1.10.21/css/jquery.dataTables.css">
<script type="text/javascript" charset="utf8" src="https://cdn.datatables.net/1.10.21/js/jquery.dataTables.js"></script>

{% assign sondaggi=site.data.puglia_polls %}

# Elezioni Regionali Puglia 2020

<table id="ge_polls" class="display" data-page-length='10' data-order='[[ 3, "desc" ]]'>
    <thead>
    {% for column in sondaggi[0] %}
        <th>{{ column[0] }}</th>
    {% endfor %}
    </thead>
    <tbody>
    {% for row in sondaggi %}
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
