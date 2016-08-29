About
===

- locations.sql contains all cities data over the world, getting data from MaxMind csv file http://dev.maxmind.com/geoip/legacy/geolite/
- Useful for an autocomplete using a jQuery Ajax UI front-end and some sort of fast backend
- Columns include: 

```mysql
DROP TABLE IF EXISTS `locations`;
CREATE TABLE IF NOT EXISTS `locations` (
  `_id` int(11) NOT NULL AUTO_INCREMENT,
  `country` varchar(255) DEFAULT NULL,
  `region` varchar(255) DEFAULT NULL,
  `city` varchar(255) DEFAULT NULL,
  `postalCode` varchar(255) DEFAULT NULL,
  `latitude` decimal(8,6) NOT NULL,
  `longitude` decimal(9,6) NOT NULL,
  `metroCode` int(11) DEFAULT NULL,
  `areaCode` int(11) DEFAULT NULL,
  PRIMARY KEY (`_id`)
) ENGINE=MyISAM AUTO_INCREMENT=804010 DEFAULT CHARSET=latin1;
```

- Some sample data:
```mysql
INSERT INTO `locations` (`_id`, `country`, `region`, `city`, `postalCode`, `latitude`, `longitude`, `metroCode`, `areaCode`) VALUES
....
(609, 'US', 'NY', 'New York', '10017', '40.752800', '-73.972500', 501, 212),
(610, 'US', 'PA', 'Bear Lake', '16402', '41.993400', '-79.502800', 516, 814),
(611, 'US', 'NJ', 'Piscataway', '08854', '40.551600', '-74.463700', 501, 732),
(612, 'US', 'NY', 'Keuka Park', '14478', '42.566900', '-77.132500', 555, 315),
(613, 'US', 'VT', 'Brattleboro', '05302', '42.850900', '-72.557900', 506, 802),
(614, 'US', 'MA', 'Hanscom Afb', '01731', '42.458500', '-71.275200', 506, 781),
....
```

MySQL Usage
===
- To create the table, use the `locations.sql` file.

- To import this database you would do via phpmyadmin or mysql command line


License for MaxMind WorldCities Database
===

OPEN DATA LICENSE for MaxMind WorldCities and Postal Code Databases

Copyright (c) 2008 MaxMind Inc.  All Rights Reserved.

All advertising materials and documentation mentioning features or use of
this database must display the following acknowledgment:
"This product includes data created by MaxMind, available from
http://www.maxmind.com/"

Redistribution and use with or without modification, are permitted provided
that the following conditions are met:
1. Redistributions must retain the above copyright notice, this list of
conditions and the following disclaimer in the documentation and/or other
materials provided with the distribution. 
2. All advertising materials and documentation mentioning features or use of
this database must display the following acknowledgement:
"This product includes data created by MaxMind, available from
http://www.maxmind.com/"
3. "MaxMind" may not be used to endorse or promote products derived from this
database without specific prior written permission.

THIS DATABASE IS PROVIDED BY MAXMIND.COM ``AS IS'' AND ANY 
EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED 
WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE 
DISCLAIMED. IN NO EVENT SHALL MAXMIND.COM BE LIABLE FOR ANY 
DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES 
(INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; 
LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND
ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT 
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS 
DATABASE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
