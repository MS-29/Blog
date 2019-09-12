## SQL Server Data Type

In SQL Server, each column, local variable, expression and parameter has a related data type. It describes the type of data that the object can hold; interger, character, date, binary and so forth. SQL Server provides a set of system data types that can be used with SQL Server. You can also define your own data types in Transact-SQL.<!--more-->

To save space in the database, use the smallest data type that can reliably contain all possible values. For example, tinyint would be sufficient for a persons age because no one lives to be more than 255 years old. But tinyint would not be sufficient for a building's age because a building can be more than 255 years old.

Data types in SQL Server are organized into the following categories:

* [Exact Numerics](#exact-numerics)
* [Approximate Numerics](#approximate-numerics)
* [Date and Time](#date-and-time)
* [Character Strings](#character-strings)
* [Unicode Character Strings](#unicode-character-strings)
* [Binary Strings](#binary-strings)
* [Miscellaneous](#miscellaneous)

## Exact Numerics

<dl>
  <dt>bit</dt>
  <dd>An integer data type that can take a value of 1, 0, or NULL. The string values TRUE and FALSE can be converted to bit values: TRUE is converted to 1 and FALSE is converted to 0. Converting to bit promotes any nonzero value to 1.</dd>
  <dt>decimal</dt>
  <dd>Fixed precision and scale numbers, which means that all the values in the data type can be represented exactly with precision and scale. The maximum total number of decimal digits to be stored is called precision which includes both the left and the right sides of the decimal point. The precision must be a value from 1 through the maximum precision of 38. The default precision is 18. The number of decimal digits that are stored to the right of the decimal point is called scale.</dd>
  <dt>numeric</dt>
  <dd>decimal and numeric are synonyms and can be used interchangeably.</dd>
</dl>
  
## Approximate Numerics
Approximate numeric data types do not store the exact values specified for many numbers; they store an extremely close approximation of the value.

<dl>
  <dt>float</dt>
  <dd>float is used to store approximate values, not exact values. Do not use float data type when exact numeric behavior is required, use decimal or numeric instead.</dd>
  <dt>real</dt>
  <dd>real is identical to float(24).</dd>
</dl>  

## Date and Time
The most difficult part when working with dates is to be sure that the format of the date you are trying to insert, matches the format of the date column in the database.

<dl>
  <dt>date</dt>
  <dd>Define date only. Default value (1900-01-01) is used for the appended date part for implicit conversion from time to datetime2 or datetimeoffset.</dd>
  <dt>time</dt>
  <dd>Defines a time of a day. The time is without time zone awareness and is based on a 24-hour clock. Default value (00:00:00) is used for the appended time part for implicit conversion from date to datetime2 or datetimeoffset.</dd>
  <dt>smalldatetime</dt>
  <dd>Defines a date that is combined with a time of day. The time is based on a 24-hour day, with seconds always zero (:00) and without fractional seconds.</dd>
  <dt>datetime</dt>
  <dd>Defines a date that is combined with a time of day with fractional seconds that is based on a 24-hour clock. datetime values are rounded to increments of .000, .003, or .007 seconds. For example, user specify value as 1998-01-01 23:59:59.999, system will store as 1998-01-02 00:00:00.000.</dd>
  <dt>datetime2</dt>
  <dd>Defines a date that is combined with a time of day that is based on 24-hour clock. datetime2 can be considered as an extension of the existing datetime type that has a larger date range, a larger default fractional precision, and optional user-specified precision.</dd>
  <dt>datetimeoffset</dt>
  <dd>Defines a date that is combined with a time of a day that has time zone awareness and is based on a 24-hour clock. Time zone offset specifies the zone offset from UTC for a time or datetime value.</dd>
</dl>

## Character Strings
<dl>
  <dt>char</dt>
  <dd>Fixed length string data. Use char when the sizes of the column data entries are consistent. The storage size of the char value is equal to the maximum size for this column.</dd>
  <dt>varchar</dt>
  <dd>Variable length string data. Use varchar when the sizes of the column data entries vary considerably. The storage size of the varchar value is the actual length of the data entered, not the maximum size for this column.</dd>
</dl>

## Unicode Character Strings

<dl>
  <dt>nchar</dt>
  <dd>nchar is pretty much identical to char. Unlike char, nchar can store unicode characters.</dd>
  <dt>nvarchar</dt>
  <dd>nvarchar is pretty much identical to varchar. Unlike varchar, nvarchar can store unicode characters.</dd>
</dl>  

## Miscellaneous

<dl>
  <dt>xml</dt>
  <dd>xml is the data type that stores XML data. You can store xml instances in a column, or a variable of xml type.</dd>
  <dt>sql_variant</dt>
  <dd>A data type that stores values of various SQL Server-supported data types. For example, a column defined as sql_variant can store int, binary, and char values. A sql_variant data type must first be cast to its base data type value before participating in operations such as addition and subtraction.</dd>
</dl>
