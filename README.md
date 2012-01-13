# Morula
Morula is a simple ruby script which dumps tweets made by a user into an SQLite3 database. It's mostly meant to act like a twitter account backup option, since twitter only holds your last 2600 tweets. Once you have your data on an [SQLite3][] database, you can work on it easily.

## Installation 
In order to install this script you need the following gems:
	
	gem install twitter
	gem install sqlite3

Clone and place morula on **/usr/loca/bin**. Then make it executable like: **chmod +x /usr/local/bin/morula**.

## Usage
First we need to create a database along with a table, which usually is named after user's twitter username. Example:
	
	greyjewel:~ atma$ morula -h
	morula 0.1-alpha (C) 2011

	Usage: morula -t twitter -u dens [options: install, create, stats, update, list, delete]
	    -d, --database FILE              Use specific database file, default is ~/.morula.db
	    -t, --tableid TABLEID            The user table id which will be used to store all his data in the database
	    -u, --userid USER                Userid for the specific protocol [only twitter supported]
	    -s, --sameid USER/TABLE          Use the same tableid and userid. Useful when we want to use aliases as tables in our database
	    -h, --help                       Display help menu
	
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
[Panagiotis Atmatzidis]: http://about.me/atmosx