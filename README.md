## 1 PENGOLAHAN DATA KARYAWAN
# Tabel Departement

# Di bawah ini merupakan perintah dan juga hasil yang di minta
````
CREATE TABLE Departemen ( IDDepartemen INT PRIMARY KEY, NamaDepartemen VARCHAR(255) );
````
![gambar1](https://github.com/AbiyanfarasDanuyasa/Smtr2-Tugas3/assets/115562487/27fa865e-1641-435d-b8e3-9a09caeb6263)

## Tabel Karyawan
### Selanjutnya adalah table karyawan dengan menggunakan perintah seperti di bawah ini beserta hasil

````
CREATE TABLE Karyawan ( IDKaryawan INT PRIMARY KEY, NamaKaryawan VARCHAR(255), IDSupervisor INT, IDDepartemen INT, FOREIGN KEY (IDSupervisor) REFERENCES Karyawan(IDKaryawan), FOREIGN KEY (IDDepartemen) REFERENCES Departemen(IDDepartemen) );
````
![gambar2](https://github.com/AbiyanfarasDanuyasa/Smtr2-Tugas3/assets/115562487/d8e8a218-66ec-4773-b349-a7318b8d1da8)

## Tabel Proyek
### Kemudian kita akan melanjutkan pada tabel proyek dengan menggunakan perintah sepert di bawah ini beserta hasilnya

````
CREATE TABLE Proyek ( IDProyek INT PRIMARY KEY, NamaProyek VARCHAR(255), TanggalMulai DATE, TanggalSelesai DATE );
````
![gambar3](https://github.com/AbiyanfarasDanuyasa/Smtr2-Tugas3/assets/115562487/e3046fc5-48c4-4b57-9f51-d15c62ac507c)

## Tabel Supervisor
### Kemudian kita akan melanjutkan pada tabel supervisor dengan menggunakan perintah sepert di bawah ini beserta hasilnya

````
CREATE TABLE Supervisor ( IDSupervisor INT, IDDepartemen INT, FOREIGN KEY (IDSupervisor) REFERENCES Karyawan(IDKaryawan), FOREIGN KEY (IDDepartemen) REFERENCES Departemen(IDDepartemen) );
````
![gambar4](https://github.com/AbiyanfarasDanuyasa/Smtr2-Tugas3/assets/115562487/ee7504f8-245a-445d-aec0-d1639a9cab89)

## Table Partisipasi
### Kemudian kita akan melanjutkan pada tabel partisipasi dengan menggunakan perintah sepert di bawah ini beserta hasilnya

````
CREATE TABLE Partisipasi ( IDKaryawan INT, IDProyek INT, FOREIGN KEY (IDKaryawan) REFERENCES Karyawan(IDKaryawan), FOREIGN KEY (IDProyek) REFERENCES Proyek(IDProyek) );
````
![gambar5](https://github.com/AbiyanfarasDanuyasa/Smtr2-Tugas3/assets/115562487/88f43764-7600-4f6d-bb36-19beb33c48bb)
