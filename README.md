# Aplikasi Desktop Apotek - Sistem Manajemen Obat (Java Netbeans dan MySQL)

Aplikasi desktop berbasis **Java Swing** + **MySQL** untuk membantu pengelolaan obat di apotek secara terintegrasi. Mendukung pencatatan stok, pembelian, penjualan, hingga laporan lengkap. Cocok untuk tugas akhir, skripsi, studi kasus bisnis apotek, maupun sistem manajemen inventori obat.

> **Catatan:** File yang dibagikan di sini adalah versi demo. Jika ingin mendapatkan versi lengkap, dapat dibeli di [LYNK.ID KidouCode](https://lynk.id/kidoucode).

---

#### **Preview Aplikasi**

<p align="center">
  <img 
    src="https://pcobvoevxdmgjvpiorua.supabase.co/storage/v1/object/public/apps-manajemen-obat/Screenshot%20Form%20Login.png"
    width="500"
    alt="Preview Form Login"
  />
</p>

#### **Teknologi**
- [MySQL 8.0.40](https://downloads.mysql.com/archives/get/p/25/file/mysql-installer-community-8.0.40.0.msi)  
- [JDK 11](https://www.oracle.com/id/java/technologies/javase/jdk11-archive-downloads.html)  

Untuk menjalankan versi demo, cukup menggunakan **JDK 11**, karena database sudah di-host secara online.  
Namun, koneksi ke database mungkin mengalami keterlambatan.

---

#### **Library / Dependensi**

- **Chart**
    - `jcommon-1.0.23.jar` → Library pendukung JFreeChart yang menyediakan utilitas umum untuk pengolahan data, formatting, dan struktur pendukung grafik.
    - `jfreechart-1.0.19.jar` → Library untuk membuat berbagai jenis grafik (bar, line, pie, area, dll) di Java Swing atau aplikasi desktop lainnya.  

- **DatePicker**
  - `miglayout-core.jar` → Versi inti MigLayout yang digunakan oleh DatePicker untuk penataan layout.  
  - `miglayout-swing.jar` → Implementasi MigLayout untuk komponen Swing, mempermudah pengaturan tata letak DatePicker.  
  - `swing-datetime-picker-1.2.3.jar` → Komponen Swing untuk memilih tanggal dan waktu (date & time picker).  

- **FlatLaf (Java Look and Feel)**
  - `flatlaf-3.5.2-sources.jar` → Source code untuk FlatLaf (Look and Feel modern di Java).  
  - `flatlaf-3.5.2.jar` → FlatLaf core, library Look and Feel modern dan minimalis untuk aplikasi Java Swing.  
  - `flatlaf-extras-3.5.2.jar` → Add-on untuk FlatLaf seperti font customization, color palette, dan icon set tambahan.  
  - `flatlaf-fonts-roboto-2.137.jar` → Font Roboto khusus untuk FlatLaf.  
  - `flatlaf-intellij-themes-3.2.5.jar` → Tema tambahan yang menyerupai IntelliJ IDEA untuk FlatLaf.  
  - `jsvg-1.4.0.jar` → Library untuk menampilkan gambar SVG di aplikasi Swing.  

- **Hashing**
  - `jbcrypt-0.4.jar` → Library untuk melakukan hashing password menggunakan algoritma BCrypt.  

- **Jasper Report**
  - `commons-beanutils-1.9.4.jar` → Utility untuk memanipulasi properti JavaBean (digunakan JasperReports).  
  - `commons-collections4-4.4.jar` → Struktur data tambahan untuk koleksi Java (digunakan JasperReports).  
  - `commons-digester-1.7.jar` → Parser XML berbasis aturan (rule-based XML parser) untuk JasperReports.  
  - `commons-logging-1.3.0.jar` → Library logging generik yang digunakan JasperReports.  
  - `groovy-4.0.16.jar` → Bahasa scripting Groovy, digunakan JasperReports untuk ekspresi dinamis.  
  - `jasperreports-6.20.6.jar` → Core JasperReports untuk membuat laporan PDF, XLS, HTML, dll.  
  - `jasperreports-fonts-7.0.1.jar` → Font tambahan untuk laporan JasperReports.  
  - `opendf-1.3.3.0.jar` → Library untuk mengelola OpenDocument Format (ODF) di JasperReports.  

- **MigLayout**
  - `miglayout-core-5.3.jar` → Core MigLayout untuk pengaturan tata letak fleksibel di Java.  
  - `miglayout-swing-5.3.jar` → Implementasi MigLayout untuk komponen Swing.  

- **Modal Dialog**
  - `modal-dialog-2.1.0.jar` → Library untuk membuat dialog kustom (popup) di Swing.  
  - `modal-dialog-demo-2.1.0.jar` → Contoh implementasi modal dialog untuk referensi.  

- **MySQL Driver**
  - `mysql-connector-j-8.0.31.jar` → Driver JDBC untuk koneksi Java dengan database MySQL.  

---

#### **Fitur Utama**
- Manajemen Merk, Kategori, Satuan, dan Lokasi
- Manajemen Data Supplier
- Manajemen Data Obat
- Pencatatan Stok Obat
- Transaksi Pembelian & Penjualan Obat
- Stock Opname (Pengecekan Stok Fisik)
- Laporan Stok, Laporan Pembelian, Laporan Penjualan, dan Laporan Stock Opname

---

#### **Arsitektur Proyek (Package)**
- **Config** : Menangani konfigurasi koneksi aplikasi dengan database.  
- **DAO** : Implementasi logika akses data ke database, termasuk penerapan antarmuka service.  
- **Form** : Mengatur dan menampilkan data dalam bentuk tabel.  
- **Form Input** : Mengatur tampilan dan fungsi form untuk input data.  
- **Assets** : Menyimpan ikon dan gambar yang digunakan aplikasi.  
- **Main** : Mengatur tampilan dan logika menu utama aplikasi.  
- **Model** : Mewakili struktur entitas sesuai tabel database.
- **Service** : Menyimpan logika bisnis untuk operasi CRUD, menghubungkan DAO dan UI.  
- **TableModel** : Model tabel khusus untuk `JTable`.  
- **Theme** : Menangani tema warna, gaya, dan layout aplikasi.  
- **Util** : Berisi fungsi-fungsi utilitas umum.  
- **Report** : Menyimpan file .jrxml dan .jasper.

---

#### **Instalasi & Menjalankan Aplikasi**

**1. Clone Repository**
```sh
git clone https://github.com/kidoucode/apps-manajemen-stok-obat.git
```

**2. Masuk ke Direktori Proyek** :

```sh
cd apps-manajemen-stok-obat
```

**3. Jalankan Aplikasi** :
```sh
java -jar MedicineManagement.jar
```
Atau Anda bisa langsung mengklik file JAR untuk menjalankan demo aplikasi ini. namun jika terkendala ketika double klik file JAR nya. bisa melalui terminal (CMS/Power Shell) dan jalankan perintah java -jar MedicineManagement.jar. pastikan jalankan perintah tersebut didalam directory file JAR nya.

**4. Login ke Aplikasi** :
```sh
Username : admin
Password : admin
```
Terima kasih

