# Introduction #
**Package** de.web\_programmer.utils
**Class**	public class PhpDate

Date class inspired on the PHP date function (http://php.net/date).

Based on the fact that the native Date class of AS3 is, in my opinion, not so great for some tasks, I decided to implement the php-Data function for AS3. If you have questions feel free to contact me (jochen.hilgers[at](at.md)gmail.com).

# Example #
There are several ways to use this class.
The first way is to use the static class method format(), such as the follow lines:
```
PhpDate.format( "r" );
PhpDate.format( "r", 1211528051 );
PhpDate.format( "r", new Date() );
```

You also can create a instance of this class and call the public method format(), too.
```
var phpDate:PhpDate = new PhpDate();
phpDate.format( "r" );
 
var phpDate2:PhpDate = new PhpDate( 1211528051 );
phpDate2.format( "r" );

var date:Date = new Date();
var phpDate3:PhpDate = new PhpDate( date );
phpDate3.format( "r" );
```

If you want to take over a given UNIX-Timestamp or AS3 Date-Object to PhpDate you only have to add the timestamp as a parameter. Remember that only the static ```
format()``` method accept this, if you use an instance you should add the timestamp/date-object to the constructor.

# Format Chars #
```
  Day
   d  Day of the month, 2 digits with leading zero  01 to 31
   D  A textual representation of the day, three letters Mon through Sun
   j  Day of the month without leading zeros  1 to 31
   l  A full textual representation of the day of the week  Sunday through Monday
   N  ISO-8601 numeric representation of the day of the week  1 (for Monday) through 7 (for Sunday)
   S   English ordinal suffix for the day of the month, 2 characters  st, nd, rd or th. Works well with j
   w   Numeric representation of the day of the week   0 (for Sunday) through 6 (for Saturday)
   z  The day of the year (starting from 0)  0 through 365
  Week
   W  ISO-8601 week number of year, weeks starting on Monday (added in PHP 4.1.0)  Example: 42 (the 42nd week in the year)
  Month
   F  A full textual representation of a month, such as January or March  January through December
   m  Numeric representation of a month, with leading zeros  01 through 12
   M  A short textual representation of a month, three letters  Jan through Dec
   n  Numeric representation of a month, without leading zeros  1 through 12
   t  Number of days in the given month  28 through 31
  Year
   L  Whether it is a leap year  1 if it is a leap year, 0 otherwise.
   Y  A full numeric representation of a year, 4 digits  Examples: 1999 or 2003
   y  A two digit representation of a year  Examples: 99 or 03
  Time
   a  Lowercase Ante meridiem and Post meridiem  am or pm
   A  Uppercase Ante meridiem and Post meridiem  AM or PM
   B  Swatch Internet time  000 through 999
   g  12-hour format of an hour without leading zeros  1 through 12
   G  24-hour format of an hour without leading zeros  0 through 23
   h  12-hour format of an hour with leading zeros  01 through 12
   H  24-hour format of an hour with leading zeros  00 through 23
   i  Minutes with leading zeros  00 to 59
   s  Seconds, with leading zeros  00 through 59
   u  Milliseconds  Example: 54321
  Timezone
   e  Timezone identifier  Examples: UTC, GMT, Atlantic/Azores
   I (capital i)  Whether or not the date is in daylight saving time  1 if Daylight Saving Time, 0 otherwise.
   O  Difference to Greenwich time (GMT) in hours  Example: +0200
   P  Difference to Greenwich time (GMT) with colon between hours and minutes  Example: +02:00
   T  Timezone abbreviation  Examples: EST, MDT ...
   Z  Timezone offset in seconds. The offset for timezones west of UTC is always negative, and for those east of UTC is always positive.
   c  ISO 8601 date 2004-02-12T15:19:21+00:00
   r  RFC 2822 formatted date  Example: Thu, 21 Dec 2000 16:01:07 +0200
   U  Seconds since the Unix Epoch (January 1 1970 00:00:00 GMT)  See also time()
```