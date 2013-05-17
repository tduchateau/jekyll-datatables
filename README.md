# jekyll-datatables

This is a Liquid block for Jekyll sites that allows you to generate table using the jQuery DataTables plugin.

## How to install

Just download the `datatables.rb` file and place it in the `_plugins/` inside your Jekyll project directory.

## Usage

    {% table test /datatables/arrays.txt %}
       {% column Id %}
       {% column FirstName %}
       {% column LastName %}
       {% column LastName %}
       {% column LastName %}
    {% endtable %}

