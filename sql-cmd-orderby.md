## ORDER BY
```sql
electronic_store=# SELECT customer_id, name, city FROM customers ORDER BY city;
electronic_store=#
customer_id |           name           |      city
-------------+--------------------------+-----------------
         149 | Tamqrah Grima            | Ambon
         213 | Thorvald Chapiro         | Ambon
          94 | Karlan Haydon            | Ambon
         212 | Royce Cockshoot          | Balikpapan
           2 | Cozmo Behne              | Balikpapan
          18 | Carmelia Ettritch        | Balikpapan
         116 | Joelynn Conre            | Balikpapan
          40 | Roseline Endle           | Bandar Lampung
         136 | Curran Arkow             | Bandar Lampung
           4 | Wendel Horley            | Bandar Lampung
         166 | Salvidor Drever          | Bandar Lampung
          61 | Maurita Tranfield        | Bandar Lampung
         173 | Atalanta Grayley         | Bandar Lampung
          44 | Jessee Langston          | Bandar Lampung
:
```

## DISTINCT
```sql
electronic_store=# SELECT DISTINCT city FROM customers ORDER BY city;
      city
-----------------
 Ambon
 Balikpapan
 Bandar Lampung
 Bandung
 Banjarmasin
 Batam
 Bekasi
 Bengkulu
 Binjai
 Bogor
 Bontang
 Cilegon
 Cimahi
 Cirebon
 Denpasar
 Depok
 Gorontalo
 jakarta
 Jakarta
 Jambi
 Jayapura
 Kendari
 Kupang
 Lhokseumawe
 Makassar
 Malang
 Manado
 Mataram
 Medan
 Padang
 Palangka Raya
 Palembang
 Palu
 Pangkal Pinang
 Pasuruan
 Pekanbaru
 Pematangsiantar
 Pontianak
 Salatiga
 Samarinda
 Semarang
 Serang
 Solo
 Sukabumi
 Surabaya
 Tangerang
 Tanjung Pinang
 Tarakan
 Tasikmalaya
 Tegal
 Yogyakarta
(51 rows)

electronic_store=#
```