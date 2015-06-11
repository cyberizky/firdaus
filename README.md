# firdaus
bersama - sama masuk syurga
alhamdulillah pada kesempatan ini saya bisa membuat github

mari kita belajar php bersama - sama dengan github, kita akan mencoba membuat program crud(create update delete) : 
1.pertama - tama anda membuat sebuah database, terserah nama database tentukan oleh anda,
create database [nama database];
2.membuat sebuah table, terserah juga untuk membuat nama sebuah table.

create table [namatable](no int(2)not null,kode int(3)not null,pelajaran varchar(30)not null,pengajar varchar(30)not null,kkm int(3));

3.buat sebuah folder, nama folder terserah anda, anda boleh mencobanya di xampp atau boleh menggunakan server di virtual machine menggunakan linux atau windows.

4.buatalah 5 file, bernama index.php(untuk menampilkan data dari database) add.php(menambahkan data ke database) delete.php (menghapus data dari database) update.php (menghapus data dari database).
buatlah index.php
ini adalah contoh sederhana untuk menampilkan sebuah database dengan 5 field yaitu :
<?php
include "connection.php";
$sqlstr = "select * from table";
$result = mysql_query($sqlstr);

echo "<table width='100%' cellpadding='2' cellspacing='1'>";
echo "<tr>
        <td>No</td>
        <td>Code</td>
        <td>Lesson</td>
        <td>Teacher</td>
        <td>Passing Grade</td>
      </tr>
        ";
while($row = mysql_fetch_object($result)){
$no = $row->no;
$kode = $row->kode;
$pelajaran = $row->pelajaran;
$pengajar = $row->pengajar;
$kkm = $row->kkm;
echo "<tr>
        <td>$no</td>
        <td>$kode</td>
        <td>$pelajara</td>
        <td>$pengajar</td>
        <td>$kkm</td>
      </tr>";
}
echo "</table>";
?>
5.tutorial selanjutnya menyusul ok
