---
title: "Columns (document template)"
parent: "Data+Grid+Document+Template"
space: "Reference Guide 5"
---


## Appearance Properties

### Caption

The caption of a column is the text that appears as a header above the rows. This is a translatable text. See [Internationalization](Translatable+Texts).

### Enumeration Format (only for attributes of type Enumeration)

A column can show its contexts as text (default) or as image.

<table><thead><tr><th class="confluenceTh">Value</th><th class="confluenceTh">Description</th></tr></thead><tbody><tr><td class="confluenceTd">Text</td><td class="confluenceTd">Show the contents of the connected attribute as a text.</td></tr><tr><td class="confluenceTd">Image</td><td class="confluenceTd">Show the image of the enumeration value.</td></tr></tbody></table>

### Decimal precision (only for numeric attributes)

The precision of a value is defined by the number of digits that is used to express that value. This property indicates the number of decimal places (the number of digits following the decimal point).

_Default value:_ 2

### Group digits (only for numeric attributes)

For ease of reading, numbers with many digits before the decimal separator may be divided into groups using a delimiter. This property defines whether the end user will see these groups, or not.

_Default value:_ False

### Date format (only for attributes of type DateTime)

The date format determines whether the date part, the time part or both are shown. How the date and time parts are formatted depends on the localization of the user using the application. Alternatively, as of version 2.5.3 you can completely customize the format of the date and/or time by supplying a date format string.

Possible values: 'Date', 'Time', 'Date and time' and in 2.5.3 'Custom'.

_Default value:_ Date

### Custom date format (only for attributes of type DateTime)

If you choose 'Custom' as the date format (see above) the custom date format determines the way date and/or time are formatted. The custom date format is a string that follows the rules described in
[http://download.oracle.com/javase/6/docs/api/java/text/SimpleDateFormat.html](http://download.oracle.com/javase/6/docs/api/java/text/SimpleDateFormat.html).

<div class="alert alert-info">{% markdown %}

The custom date format
`EEE, MMM d, ''yy`
results in the following text
`Wed, Jul 4, '01`

{% endmarkdown %}</div>

## Data Source Properties

### Attribute (path)

The attribute (path) property specifies the attribute whose value will be displayed in the column. It can be an attribute of the grid entity, or it can be an attribute of an associated entity. The path over which an associated object is accessed is referred to as an attribute path. The path can follow multiple associations of type reference, and at the end (optionally) one of type reference set. If you show a reference set in a column the values will be separated by a comma.