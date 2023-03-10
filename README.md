# Automobile Gas Analysis
Complete the specification of the Date class as defined below.Driver.py program can be used to test the Date class.
<pre>
class Date:
	# Constructor
	def __init__(self, month, day, year):
		self._month = month
		self._day = day
		self._year = year

	def leap_year(self):
		return ((self._year%4 == 0) and not (self._year%100 == 0 and self._year%400 != 0))

	# Returns the Date object one day after self
	def tomorrow(self):
		pass

	# Returns the Date object obtained by adding ndays to self
	def add(self,ndays):
		pass

	# Returns True if self is after d
	def after(self,d):
		pass

	# Returns True if self is same as d
	def equals(self,d):
		pass

	# Returns True if self is before d
	def before(self,d):
		pass

	# Returns the number of days between self and d
	def days_between(self,d):
		pass

	def __str__(self):
		pass
    </pre>
The above template for Date class is available in Date.py.
Write a program, called AutoMileageAnalysis.py, which reads data from an input file (file name provided as command line input) containing a log of visits to the gas station to fill up full tanks of gas for an entire year. A sample input (available in text file car1.dat) is given below:
<pre>
Honda Accord
1989
1/1/1989   & 13.07   & 13.19 & 6895
1/7/1989   & 10.25   & 10.44 & 7235
1/14/1989  & 12.90   & 16.70 & 7626
1/30/1989  & 10.00   & 9.59  & 7959
2/10/1989  & 10.00   & 10.10 & 8132
2/11/1989  & 10.08   & 9.68  & 8475
3/3/1989   & 11.50   & 13.00 & 8781
3/26/1989  & 10.71   & 10.91 & 9028
4/16/1989  & 13.04   & 14.99 & 9369
5/17/1989  & 13.04   & 16.69 & 9683
5/26/1989  & 8.70    & 10.00 & 10005
6/4/1989   & 11.38   & 13.19 & 10376
6/25/1989  & 12.48   & 14.84 & 10730
7/16/1989  & 12.41   & 16.25 & 11037
7/29/1989  & 10.60   & 12.86 & 11367
8/11/1989  & 12.26   & 14.45 & 11713
9/3/1989   & 13.07   & 14.61 & 12052
9/29/1989  & 12.41   & 15.14 & 12359
10/21/1989 & 11.87   & 13.52 & 12659
11/11/1989 & 12.48   & 13.59 & 13015
12/8/1989  & 12.32   & 12.30 & 13306
12/28/1989 & 11.51   & 13.11 & 13565
0/0/0 & 0 & 0 & 0
</pre>
We will assume that the first line lists the car model, the second line lists the year, and subsequent lines list details of visits to the gas station (date, gallons, cost, and odometer reading separated by &). The last line begins with the date 0/0/0 which indicates end of log.
A sample run is shown below:
<pre>
Mac-mini:Date sb$ python3 AutoMileageAnalysis.py car1.dat

Auto Gas Analysis, Year 1989
Honda Accord

Date                Gallons   $Spent MilesDriven DaysToNextFill    MPG
----------------------------------------------------------------------
1 January, 1989       13.07    13.19         340         6       26.01
7 January, 1989       10.25    10.44         391         7       38.15
14 January, 1989      12.90    16.70         333        16       25.81
30 January, 1989      10.00     9.59         173        11       17.30
10 February, 1989     10.00    10.10         343         1       34.30
11 February, 1989     10.08     9.68         306        20       30.36
3 March, 1989         11.50    13.00         247        23       21.48
26 March, 1989        10.71    10.91         341        21       31.84
16 April, 1989        13.04    14.99         314        31       24.08
17 May, 1989          13.04    16.69         322         9       24.69
26 May, 1989           8.70    10.00         371         9       42.64
4 June, 1989          11.38    13.19         354        21       31.11
25 June, 1989         12.48    14.84         307        21       24.60
16 July, 1989         12.41    16.25         330        13       26.59
29 July, 1989         10.60    12.86         346        13       32.64
11 August, 1989       12.26    14.45         339        23       27.65
3 September, 1989     13.07    14.61         307        26       23.49
29 September, 1989    12.41    15.14         300        22       24.17
21 October, 1989      11.87    13.52         356        21       29.99
11 November, 1989     12.48    13.59         291        27       23.32
8 December, 1989      12.32    12.30         259        20       21.02
28 December, 1989     11.51    13.11
----------------------------------------------------------------------
Totals               256.08   289.15        6670
Averages                                                17       27.68
----------------------------------------------------------------------

Mac-mini:Date sb$
<pre>
The program should use the Date class developed earlier to do any Date calculations. The formatting should be exactly as shown.
