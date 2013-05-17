# jekyll-datatables

This is a Liquid block for Jekyll sites that allows you to generate table using the jQuery DataTables plugin.

## How to install

Just download the `datatables.rb` file and place it in the `_plugins/` inside your Jekyll project directory.

## Usage

    {% table <table_dom_id> <data_source_url> %}
       {% column Id %}
       {% column FirstName %}
       {% column LastName %}
       {% column City %}
       {% column Mail %}
    {% endtable %}

For example:

    {% table myTableId /arrays.txt %}
       {% column Id %}
       {% column FirstName %}
       {% column LastName %}
       {% column City %}
       {% column Mail %}
    {% endtable %}

where arrays.txt contains:

    { "aaData": [
	   ["Trident","Internet Explorer 4.0","Win 95+","4","X"],
	   ["Trident","Internet Explorer 5.0","Win 95+","5","C"],
	   ["Trident","Internet Explorer 5.5","Win 95+","5.5","A"],
	   ...
	]}
    
## Features

For now, the plugin only supports AJAX sources (array of arrays) and no other configuration.