	
	greyjewel:~ atma$ morula -s dens install
	database file: /Users/atma/.morula.db
	userid: dens
	Table 'dens' has been created on database: /Users/atma/.morula.db

You can choose a different database location, username and table name. Example:
	
	greyjewel:~ atma$ morula -d /tmp/testdb -t table1 install
	database file: /tmp/testdb
	userid: table1
	Table 'table1' has been created on database: /tmp/testdb

Now you can dump tweets into your database by the following command:
	
	greyjewel:~ atma$ morula -d /tmp/testdb -t table1 -u dens update
	
Or more simply, if you have used the defualt values:
	
	greyjewel:~ atma$ morula -s dens update

That's most of it. There are a couple of commands like list and stats from which you can retrieve some basic info but the idea is to have your data into an SQLite3 database for further usage with other programs.

[SQLite3]: http://www.sqlite.org/

# License
**The MIT License (MIT)**

Copyright (c) 2012 Panagiotis Atmatizdis

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

# Author
[Panagiotis Atmatzidis]
[Panagiotis Atmatzidis]: http://www.convalesco.org 
