# Morula
Morula is a [ruby][] script that dumps tweets into an [SQLite3][] database. It's meant to act like a twitter backup option since twitter only holds your last 2600 tweets. It can be used to gather data for analysis.

## Installation 
In order to install this script you need the following gems:
  
    gem install twitter
    gem install sqlite3

Clone and place morula on **/usr/loca/bin**. Then make it executable like: **chmod +x /usr/local/bin/morula**.

## Usage
First we need to create a database along with a table, which usually is named after user's twitter username. Example:

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
	
You can see database details by using 'info' comand:
	
	greyjewel:~ atma$ morula info
	
That's all, simple & straight forward. Morula does not support auth yet. Support for other protocols - *except twitter* - is something I'm also considering for a future version.

[SQLite3]: http://www.sqlite.org/
[ruby]: http://www.ruby-lang.org/en/

# License
**The MIT License (MIT)**

Copyright (c) 2012 Panagiotis Atmatizdis

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

# Author
[Panagiotis Atmatzidis]
[Panagiotis Atmatzidis]: http://www.convalesco.org 
