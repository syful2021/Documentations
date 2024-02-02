# Documentations

# PHP date() Function
==========^^==========
The date() function formats a local date and time, and returns the formatted date string.
Syntax:
date(format, timestamp)

Parameter Values

Parameter with description

d - The day of the month (from 01 to 31)
D - A textual representation of a day (three letters)
j - The day of the month without leading zeros (1 to 31)
l (lowercase 'L') - A full textual representation of a day
N - The ISO-8601 numeric representation of a day (1 for Monday, 7 for Sunday)
S - The English ordinal suffix for the day of the month (2 characters st, nd, rd or th. Works well with j)
w - A numeric representation of the day (0 for Sunday, 6 for Saturday)
z - The day of the year (from 0 through 365)
W - The ISO-8601 week number of year (weeks starting on Monday)
F - A full textual representation of a month (January through December)
m - A numeric representation of a month (from 01 to 12)
M - A short textual representation of a month (three letters)
n - A numeric representation of a month, without leading zeros (1 to 12)
t - The number of days in the given month
L - Whether it's a leap year (1 if it is a leap year, 0 otherwise)
o - The ISO-8601 year number
Y - A four digit representation of a year
y - A two digit representation of a year
a - Lowercase am or pm
A - Uppercase AM or PM
B - Swatch Internet time (000 to 999)
g - 12-hour format of an hour (1 to 12)
G - 24-hour format of an hour (0 to 23)
h - 12-hour format of an hour (01 to 12)
H - 24-hour format of an hour (00 to 23)
i - Minutes with leading zeros (00 to 59)
s - Seconds, with leading zeros (00 to 59)
u - Microseconds (added in PHP 5.2.2)
e - The timezone identifier (Examples: UTC, GMT, Atlantic/Azores)
I (capital i) - Whether the date is in daylights savings time (1 if Daylight Savings Time, 0 otherwise)
O - Difference to Greenwich time (GMT) in hours (Example: +0100)
P - Difference to Greenwich time (GMT) in hours:minutes (added in PHP 5.1.3)
T - Timezone abbreviations (Examples: EST, MDT)
Z - Timezone offset in seconds. The offset for timezones west of UTC is negative (-43200 to 50400)
c - The ISO-8601 date (e.g. 2013-05-05T16:34:42+00:00)
r - The RFC 2822 formatted date (e.g. Fri, 12 Apr 2013 12:01:05 +0200)
U - The seconds since the Unix Epoch (January 1 1970 00:00:00 GMT)
and the following predefined constants can also be used (available since PHP 5.1.0):

==========^^==========

Q: How to get the current date and time in PHP?
Ans: The time would go by your server time. An easy workaround for this is to manually set the timezone by using date_default_timezone_set before the date() or time() functions are called to.
I'm in dhaka, Bangladesh so I have something like this:
date_default_timezone_set('Asia/dhaka');
Or another example of Nepal
date_default_timezone_set('Asia/Kathmandu');
You can also see what timezone the server is currently in via:
date_default_timezone_get();
So something like:
$timezone = date_default_timezone_get();
echo "The current server timezone is: " . $timezone;
So the short answer to your question would be:
// Change the line below to your timezone!
date_default_timezone_set('Asia/Kolkata');
$date = date('m/d/Y h:i:s a', time());

Then all the times would be to the timezone you just set :)

==========^^==========

Q: How to check the current timezone in PHP?
Ans: Here is the code 

$timezone = date_default_timezone_get();
echo "The current server timezone is: " . $timezone;

NOTES:  Here is the Location that you can use to set your default dates and times.
==========^^==========

Asia/Aden	, Asia/Almaty,	Asia/Amman,	Asia/Anadyr,
Asia/Aqtau,	Asia/Aqtobe,	Asia/Ashgabat,	Asia/Atyrau,
Asia/Baghdad,	Asia/Bahrain,	Asia/Baku,	Asia/Bangkok,
Asia/Barnaul,,	Asia/Beirut,	Asia/Bishkek,	Asia/Brunei,
Asia/Chita,	Asia/Choibalsan,	Asia/Colombo,	Asia/Damascus,
Asia/Dhaka,	Asia/Dili,	Asia/Dubai	,Asia/Dushanbe,
