# jekyll-datatables

My attempt to write a Liquid block for Jekyll sites that allows you to generate table using the awesome [jQuery DataTables plugin](http://datatables.net/).

## How to install

Just download the `datatables.rb` file and place it in the `_plugins/` directory of your Jekyll project.

## Usage

    {% table <table_dom_id> <data_source_url> %}
       {% column <column_title> %}
       {% column <column_title> %}
       {% column <column_title> %}
    {% endtable %}

For example:

    {% table myTableId /arrays.txt %}
       {% column 'Rendering engine' %}
       {% column 'Browser' %}
       {% column 'Platform(s)' %}
       {% column 'Engine version' %}
       {% column 'CSS grade' %}
    {% endtable %}

where arrays.txt contains:

    { "aaData": [
	   ["Trident","Internet Explorer 4.0","Win 95+","4","X"],
	   ["Trident","Internet Explorer 5.0","Win 95+","5","C"],
	   ["Trident","Internet Explorer 5.5","Win 95+","5.5","A"],
	   ...
	]}
    
## Features

For now, the plugin only supports AJAX sources (array of arrays) and no other additional configuration.

## How it works

Jekyll-Datatables generates all the HTML markup needed to make DataTables work:

 * `<table>` and all nested tags
 * `<script>` and `<link>` tags pointing to the last available release hosted on the Microsoft's CDN
 * The DataTables initialization code
