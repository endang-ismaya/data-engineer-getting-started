## WHERE + OPERATOR PERBANDINGAN
```sql
electronic_store=# SELECT * FROM products WHERE price>100;
 product_id |           product_name           |  brand  | price  | in_stock
------------+----------------------------------+---------+--------+----------
         13 | BLU G70                          | BLU     | 199.00 | t
         43 | Unnecto Drone Z                  | Unnecto | 149.99 | t
         72 | Samsung Galaxy Ace Advance S6800 | Samsung | 109.99 | t
(3 rows)

electronic_store=#

electronic_store=# SELECT * FROM customers WHERE city='Jakarta';
 customer_id |        name         | date_of_birth | gender |  city   |            email             |   phone
-------------+---------------------+---------------+--------+---------+------------------------------+------------
           5 | Manuel Marunchak    | 1981-07-09    | Male   | Jakarta | mmarunchak4@weibo.com        | 7618901331
          11 | Shurlocke Dudbridge | 1971-02-11    | Male   | Jakarta | sdudbridgea@redcross.org     | 6486650150
          24 | Berny Leatherbarrow | 1998-08-04    | Male   | Jakarta | bleatherbarrown@alexa.com    | 6736754805
          27 | Kelley Ockwell      | 1985-06-02    | Female | Jakarta | kockwellq@purevolume.com     | 4842301750
          32 | Camala Arthur       | 1970-05-20    | Female | Jakarta | carthurv@google.it           | 1753682600
          65 | Jody Askaw          | 1970-06-19    | Male   | Jakarta | jaskaw1s@pbs.org             | 4581084017
         132 | Gail Colloff        | 1960-07-18    | Female | Jakarta | gcolloff3n@google.fr         | 5825127404
         134 | Darline Gooday      | 1971-08-09    | Female | Jakarta | dgooday3p@domainmarket.com   | 4807239439
         167 | Phillipp Gullefant  | 1990-05-30    | Male   | Jakarta | pgullefant4m@jimdo.com       | 5299669617
         172 | Mathew Skelton      | 1989-10-04    | Male   | Jakarta | mskelton4r@howstuffworks.com | 5823251878
         201 | Tallia Poile        | 1968-11-20    | Female | Jakarta | tpoile5k@4shared.com         | 8375898360
         203 | Clarence Flight     | 1983-12-23    | Male   | Jakarta | cflight5m@123-reg.co.uk      | 8707364664
         206 | Garald Stapforth    | 1985-01-12    | Male   | Jakarta | gstapforth5p@prweb.com       | 6975891381
         221 | Dela Bitten         | 1991-11-13    | Female | Jakarta | dbitten64@yahoo.com          | 5634605743
(14 rows)

electronic_store=#
```

## WHERE + OPERATOR LOGIKA
```sql
electronic_store=# SELECT * FROM products WHERE price>100 AND price<150;
 product_id |           product_name           |  brand  | price  | in_stock
------------+----------------------------------+---------+--------+----------
         43 | Unnecto Drone Z                  | Unnecto | 149.99 | t
         72 | Samsung Galaxy Ace Advance S6800 | Samsung | 109.99 | t
(2 rows)

electronic_store=#

electronic_store=# SELECT * FROM products WHERE NOT in_stock = TRUE;
 product_id |      product_name       |  brand   | price | in_stock
------------+-------------------------+----------+-------+----------
         21 | vivo Z3i                | vivo     | 39.99 | f
         23 | Motorola C115           | Motorola | 22.99 | f
         33 | Philips Fisio 610       | Philips  | 49.99 | f
         34 | Wiko Lenny2             | Wiko     |  1.29 | f
         50 | Samsung P730            | Samsung  |  3.99 | f
         52 | alcatel Fire 7          | alcatel  |  5.49 | f
         53 | Motorola M3788          | Motorola |  3.79 | f
         70 | HTC One (M8i)           | HTC      |  3.99 | f
         78 | Motorola Moto G 5G Plus | Motorola | 39.99 | f
         81 | verykool T7445          | verykool | 30.00 | f
         85 | Samsung I100 Gem        | Samsung  |  3.79 | f
         95 | NIU Pana N105           | NIU      | 19.99 | f
         99 | Micromax A90            | Micromax | 14.99 | f
(13 rows)

electronic_store=#
```

## WHERE + BETWEEN
```sql
electronic_store=# SELECT * FROM products WHERE price BETWEEN 1 AND 5;
 product_id |         product_name          |   brand    | price | in_stock
------------+-------------------------------+------------+-------+----------
          3 | Samsung R260 Chrono           | Samsung    |  3.29 | t
          4 | Yezz Andy YZ1100              | Yezz       |  2.29 | t
          8 | LG X Skin                     | LG         |  4.99 | t
         11 | LG X4+                        | LG         |  2.99 | t
         17 | ZTE Blade G                   | ZTE        |  4.49 | t
         22 | Micromax A63 Canvas Fun       | Micromax   |  4.29 | t
         25 | Samsung Galaxy A42 5G         | Samsung    |  3.99 | t
         27 | BlackBerry Curve 8330         | BlackBerry |  1.99 | t
         29 | Samsung Galaxy Express Prime  | Samsung    |  2.99 | t
         31 | Samsung Propel Pro            | Samsung    |  3.49 | t
         34 | Wiko Lenny2                   | Wiko       |  1.29 | f
         35 | Samsung T369                  | Samsung    |  3.49 | t
         36 | Honor 20 lite                 | Honor      |  3.99 | t
         37 | BLU Dash L3                   | BLU        |  2.79 | t
         38 | Gionee S6 Pro                 | Gionee     |  2.69 | t
         39 | Celkon C337                   | Celkon     |  4.49 | t
         46 | verykool i130                 | verykool   |  1.89 | t
         50 | Samsung P730                  | Samsung    |  3.99 | f
         51 | Huawei G7002                  | Huawei     |  2.79 | t
         53 | Motorola M3788                | Motorola   |  3.79 | f
         56 | Realme C1                     | Realme     |  2.99 | t
         61 | ZTE Grand X LTE T82           | ZTE        |  3.99 | t
         63 | Samsung E2230                 | Samsung    |  2.99 | t
         65 | Samsung Galaxy Tab 4 7.0 3G   | Samsung    |  3.99 | t
         66 | Motorola One 5G UW            | Motorola   |  3.99 | t
         70 | HTC One (M8i)                 | HTC        |  3.99 | f
         74 | Maxwest Blade                 | Maxwest    |  3.29 | t
         79 | Apple iPad 3 Wi-Fi + Cellular | Apple      |  2.29 | t
         80 | Oppo A73                      | Oppo       |  4.29 | t
         83 | Wiko Sunny3 Plus              | Wiko       |  3.99 | t
         85 | Samsung I100 Gem              | Samsung    |  3.79 | f
         92 | Panasonic VS7                 | Panasonic  |  3.99 | t
         97 | ZTE Maven                     | ZTE        |  2.49 | t
(33 rows)

electronic_store=#
```

## WHERE + LIKE or ILIKE
```sql
electronic_store=# SELECT * FROM customers WHERE email LIKE '%@weibo.com';
 customer_id |       name       | date_of_birth | gender |  city   |         email         |   phone
-------------+------------------+---------------+--------+---------+-----------------------+------------
           5 | Manuel Marunchak | 1981-07-09    | Male   | Jakarta | mmarunchak4@weibo.com | 7618901331
         126 | Kip Ketley       | 1973-05-18    | Female | Bandung | kketley3h@weibo.com   | 8741790737
(2 rows)

electronic_store=#

electronic_store=# SELECT * FROM customers WHERE city ILIKE 'jakarta';
 customer_id |        name         | date_of_birth | gender |  city   |            email             |   phone
-------------+---------------------+---------------+--------+---------+------------------------------+------------
           5 | Manuel Marunchak    | 1981-07-09    | Male   | Jakarta | mmarunchak4@weibo.com        | 7618901331
          11 | Shurlocke Dudbridge | 1971-02-11    | Male   | Jakarta | sdudbridgea@redcross.org     | 6486650150
          24 | Berny Leatherbarrow | 1998-08-04    | Male   | Jakarta | bleatherbarrown@alexa.com    | 6736754805
          27 | Kelley Ockwell      | 1985-06-02    | Female | Jakarta | kockwellq@purevolume.com     | 4842301750
          32 | Camala Arthur       | 1970-05-20    | Female | Jakarta | carthurv@google.it           | 1753682600
          54 | Julius Mapes        | 1978-03-09    | Male   | jakarta | jmapes1h@wunderground.com    | 5391908016
          57 | Billie Emsley       | 1962-06-08    | Female | jakarta | bemsley1k@webnode.com        | 2568023046
          63 | Adore Banke         | 1987-07-05    | Female | jakarta | abanke1q@seattletimes.com    | 9451296136
          65 | Jody Askaw          | 1970-06-19    | Male   | Jakarta | jaskaw1s@pbs.org             | 4581084017
         111 | Angil Mac Giany     | 1988-05-19    | Female | jakarta | amac32@ebay.co.uk            | 9705751316
         132 | Gail Colloff        | 1960-07-18    | Female | Jakarta | gcolloff3n@google.fr         | 5825127404
         134 | Darline Gooday      | 1971-08-09    | Female | Jakarta | dgooday3p@domainmarket.com   | 4807239439
         167 | Phillipp Gullefant  | 1990-05-30    | Male   | Jakarta | pgullefant4m@jimdo.com       | 5299669617
         172 | Mathew Skelton      | 1989-10-04    | Male   | Jakarta | mskelton4r@howstuffworks.com | 5823251878
         201 | Tallia Poile        | 1968-11-20    | Female | Jakarta | tpoile5k@4shared.com         | 8375898360
         203 | Clarence Flight     | 1983-12-23    | Male   | Jakarta | cflight5m@123-reg.co.uk      | 8707364664
         206 | Garald Stapforth    | 1985-01-12    | Male   | Jakarta | gstapforth5p@prweb.com       | 6975891381
         221 | Dela Bitten         | 1991-11-13    | Female | Jakarta | dbitten64@yahoo.com          | 5634605743
(18 rows)

electronic_store=#
```

## WHERE + IN / NOT IN
```sql
electronic_store=# SELECT * FROM customers WHERE city IN ('Jakarta', 'Bandung', 'Surabaya');
 customer_id |        name         | date_of_birth | gender |   city   |              email              |   phone
-------------+---------------------+---------------+--------+----------+---------------------------------+------------
           5 | Manuel Marunchak    | 1981-07-09    | Male   | Jakarta  | mmarunchak4@weibo.com           | 7618901331
          11 | Shurlocke Dudbridge | 1971-02-11    | Male   | Jakarta  | sdudbridgea@redcross.org        | 6486650150
          24 | Berny Leatherbarrow | 1998-08-04    | Male   | Jakarta  | bleatherbarrown@alexa.com       | 6736754805
          27 | Kelley Ockwell      | 1985-06-02    | Female | Jakarta  | kockwellq@purevolume.com        | 4842301750
          31 | Tucky Geibel        | 1980-10-26    | Male   | Surabaya | tgeibelu@youtu.be               | 6868312481
          32 | Camala Arthur       | 1970-05-20    | Female | Jakarta  | carthurv@google.it              | 1753682600
          37 | Dominic Burk        | 1989-02-12    | Male   | Surabaya | dburk10@multiply.com            | 4098119128
          65 | Jody Askaw          | 1970-06-19    | Male   | Jakarta  | jaskaw1s@pbs.org                | 4581084017
          84 | Patsy Rettie        | 1976-06-17    | Female | Surabaya | prettie2b@gravatar.com          | 5731540657
          85 | Brandtr Blackall    | 1983-02-26    | Male   | Surabaya | bblackall2c@businessinsider.com | 1173000070
          97 | Pablo Abele         | 1997-05-24    | Male   | Bandung  | pabele2o@msn.com                | 5942175524
         105 | Steffen Haxley      | 1994-12-25    | Male   | Bandung  | shaxley2w@oracle.com            | 7015821105
         126 | Kip Ketley          | 1973-05-18    | Female | Bandung  | kketley3h@weibo.com             | 8741790737
         132 | Gail Colloff        | 1960-07-18    | Female | Jakarta  | gcolloff3n@google.fr            | 5825127404
         134 | Darline Gooday      | 1971-08-09    | Female | Jakarta  | dgooday3p@domainmarket.com      | 4807239439
         167 | Phillipp Gullefant  | 1990-05-30    | Male   | Jakarta  | pgullefant4m@jimdo.com          | 5299669617
         172 | Mathew Skelton      | 1989-10-04    | Male   | Jakarta  | mskelton4r@howstuffworks.com    | 5823251878
         201 | Tallia Poile        | 1968-11-20    | Female | Jakarta  | tpoile5k@4shared.com            | 8375898360
         203 | Clarence Flight     | 1983-12-23    | Male   | Jakarta  | cflight5m@123-reg.co.uk         | 8707364664
         206 | Garald Stapforth    | 1985-01-12    | Male   | Jakarta  | gstapforth5p@prweb.com          | 6975891381
         218 | Dyanne Lailey       | 1974-12-27    | Female | Bandung  | dlailey61@mysql.com             | 6385846739
         221 | Dela Bitten         | 1991-11-13    | Female | Jakarta  | dbitten64@yahoo.com             | 5634605743
         229 | Gratia Cleland      | 1992-09-13    | Female | Bandung  | gcleland6c@amazonaws.com        | 5826578611
(23 rows)

electronic_store=#


electronic_store=# SELECT * FROM customers WHERE city ILIKE ANY (ARRAY['Jakarta', 'Bandung', 'Surabaya']);
 customer_id |        name         | date_of_birth | gender |   city   |              email              |   phone
-------------+---------------------+---------------+--------+----------+---------------------------------+------------
           5 | Manuel Marunchak    | 1981-07-09    | Male   | Jakarta  | mmarunchak4@weibo.com           | 7618901331
          11 | Shurlocke Dudbridge | 1971-02-11    | Male   | Jakarta  | sdudbridgea@redcross.org        | 6486650150
          24 | Berny Leatherbarrow | 1998-08-04    | Male   | Jakarta  | bleatherbarrown@alexa.com       | 6736754805
          27 | Kelley Ockwell      | 1985-06-02    | Female | Jakarta  | kockwellq@purevolume.com        | 4842301750
          31 | Tucky Geibel        | 1980-10-26    | Male   | Surabaya | tgeibelu@youtu.be               | 6868312481
          32 | Camala Arthur       | 1970-05-20    | Female | Jakarta  | carthurv@google.it              | 1753682600
          37 | Dominic Burk        | 1989-02-12    | Male   | Surabaya | dburk10@multiply.com            | 4098119128
          54 | Julius Mapes        | 1978-03-09    | Male   | jakarta  | jmapes1h@wunderground.com       | 5391908016
          57 | Billie Emsley       | 1962-06-08    | Female | jakarta  | bemsley1k@webnode.com           | 2568023046
          63 | Adore Banke         | 1987-07-05    | Female | jakarta  | abanke1q@seattletimes.com       | 9451296136
          65 | Jody Askaw          | 1970-06-19    | Male   | Jakarta  | jaskaw1s@pbs.org                | 4581084017
          84 | Patsy Rettie        | 1976-06-17    | Female | Surabaya | prettie2b@gravatar.com          | 5731540657
          85 | Brandtr Blackall    | 1983-02-26    | Male   | Surabaya | bblackall2c@businessinsider.com | 1173000070
          97 | Pablo Abele         | 1997-05-24    | Male   | Bandung  | pabele2o@msn.com                | 5942175524
         105 | Steffen Haxley      | 1994-12-25    | Male   | Bandung  | shaxley2w@oracle.com            | 7015821105
         111 | Angil Mac Giany     | 1988-05-19    | Female | jakarta  | amac32@ebay.co.uk               | 9705751316
         126 | Kip Ketley          | 1973-05-18    | Female | Bandung  | kketley3h@weibo.com             | 8741790737
         132 | Gail Colloff        | 1960-07-18    | Female | Jakarta  | gcolloff3n@google.fr            | 5825127404
         134 | Darline Gooday      | 1971-08-09    | Female | Jakarta  | dgooday3p@domainmarket.com      | 4807239439
         167 | Phillipp Gullefant  | 1990-05-30    | Male   | Jakarta  | pgullefant4m@jimdo.com          | 5299669617
         172 | Mathew Skelton      | 1989-10-04    | Male   | Jakarta  | mskelton4r@howstuffworks.com    | 5823251878
         201 | Tallia Poile        | 1968-11-20    | Female | Jakarta  | tpoile5k@4shared.com            | 8375898360
         203 | Clarence Flight     | 1983-12-23    | Male   | Jakarta  | cflight5m@123-reg.co.uk         | 8707364664
         206 | Garald Stapforth    | 1985-01-12    | Male   | Jakarta  | gstapforth5p@prweb.com          | 6975891381
         218 | Dyanne Lailey       | 1974-12-27    | Female | Bandung  | dlailey61@mysql.com             | 6385846739
         221 | Dela Bitten         | 1991-11-13    | Female | Jakarta  | dbitten64@yahoo.com             | 5634605743
         229 | Gratia Cleland      | 1992-09-13    | Female | Bandung  | gcleland6c@amazonaws.com        | 5826578611
(27 rows)

electronic_store=#
```