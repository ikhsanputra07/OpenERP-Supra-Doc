DELIVERY NOTE
=============


Contents:

Merupakan modul untuk melakukan input surat jalan oleh sales.
Modul ini dapat di akses pada menu "Sales" -> "Sales" -> "Delivery Note"


Flow Delivery Note

.. image:: /img/dnflow.png


#. Flow dimulai setelah melewati proses **Order Preparation** dimana barang telah dipacking oleh warehouse staff. 
#. Selanjutnya sales melakukan penginputan surat jalan melalui ERP pada modul menu Delivery Note. 
#. Setelah proses penginputan sudah lengkap maka sales dapat mencetak draft surat jalan di kertas dengan meng-submit dokumen terlebih dahulu. 
#. Selanjutnya sales terlebih dahulu meminta approve (persetujuan) dan tanda tangan dari manager atau bagian lain yang bersangkutan.
#. Selanjutnya setelah surat jalan disetujui maka akan ada proses negosiasi dengan customer, dari proses tersebut ada beberapa kemungkinan yaitu meng-cancel surat jalan karena adanya pembatalan pemesanan, meng-postpone surat jalan karena customer meminta barang untuk di tunda pengirimannya terlebih dahulu, atau validasi surat jalan kepada bagian warehouse yang berarti barang telah keluar dari gudang dan dikirim pada customer. 

Pada saat customer memilih untuk menunda (postpone) pengiriman barang, maka terdapat flow dari proses postpone tersebut  

.. image:: /img/dnpostponeflow.png

#. Flow dimulai dengan bagian warehouse mendapatkan surat jalan penundaan dari barang yang akan dikirim.
#. Selanjutnya proses dilanjutkan dengan negosiasi kembali dengan user, dari proses tersebut ada beberapa kemungkinan yaitu pembatalan (cancel) pengiriman barang, Re-packing item dimana pada proses ini paket dibongkar ulang untuk melakukan penambahan atau mengganti barang yang akan dikirim sesuai dengan permintaan customer, untuk proses Re-packing harus kembali melakukan proses Order preparation, dan kemungkinan terakhir yaitu melanjutkan kembali proses dari surat jalan.   
#. Dalam melanjutkan kembali proses surat jalan terdapat dua kemungkinan sebelum meminta tanda tangan dan approve (persetujuan) kembali kepada pihak manager atau bagian lain yang bersangkutan, dimana sales dapat tetap menggunakan nomor surat jalan yang lama atau menggantinya dengan surat jalan yang baru dengan me-reload nomor dokumen.
#. Setelah surat jalan disetujui maka akan ada proses negosiasi kembali dengan customer, dari proses tersebut ada beberapa kemungkinan yaitu meng-cancel surat jalan karena adanya pembatalan pemesanan, meng-postpone kembali surat jalan, atau validasi surat jalan kepada bagian warehouse yang berarti barang telah keluar dari gudang dan dikirim pada customer.

Form Delivery Note :

 .. image:: /img/dn-1-edit.png



Penjelasan Field:

+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                               |
+===+=======================+===============+==========================================================================================+
|1  | Delivery Note         | Ya            |Dokumen yang digunakan untuk Surat Jalan                                                  |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|2  | SPK                   | Ya            |Nomor SPK (Surat Perintah Kerja)                                                          |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|3  | Order Packaging       | Ya            |Pemesanan pengemasan                                                                      |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|4  | Customer Reference    | Ya            |Nomor PO                                                                                  |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|5  | Delivery Date         | Ya            |Tanggal Pengiriman Barang                                                                 |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|6  | Note Return           | Tidak         |Informasi Pengembalian Barang                                                             |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|7  | Special WO            | Tidak         |Informasi yang menunjukkan  Special Order                                                 |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|8  | SPK Internal          | Tidak         |Nomor SPK Internal                                                                        |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|9  | Customer              | Ya            |Nama / Data Customer, nama perusahaan Customer                                            |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|10 | Delivery Address      | Ya            |Nama Site / Alamat tempat Pengiriman yang akan dituju                                     |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|11 | Attention             | Tidak         |Nama Orang yang dituju untuk penawaran                                                    |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|12 | Note Line             | Ya            |Dokumen mengenai item sell yang telah disiapkan                                           |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|13 | Packing Lines         | Ya            |Dokumen mengenai detail kemasan item                                                      |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|14 | Notes                 | Tidak         |Dokumen catatan internal                                                                  |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|15 | Others                | Tidak         |                                                                                          |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|16 | Proses Return Products| Tidak         |Dokumen mengenai pengembalian barang                                                      |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+
|17 | Terms and Condition   | Tidak         |Catatan mengenai Ketentuan dan Syarat yang berlaku                                        |
+---+-----------------------+---------------+------------------------------------------------------------------------------------------+


Pada form tersebut terdapat **5 Tab**, yaitu :

Note Lines
----------

Note Lines merupakan item sale yang telah disiapkan dari suatu penawaran.
Pada Note Lines berisi pula informasi mengenai material tambahan yang merupakan paket dari item tersebut.
Item yang dimaksud adalah merupakan **Produk, ataupun Jasa** yang ditawarkan kepada Customer.



.. image:: /img/dn-2-edit.png

(Gambar Note Lines - Form / Detail)


Field yang ada pada **Note Lines**:


+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                                                         |
+===+=======================+===============+====================================================================================================================+
|1  | No                    | Ya            | Id dari item                                                                                                       |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|2  | Quantity              | Ya            | Banyaknya item yang ditawarkan                                                                                     |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|3  | Packaging             | Ya            | Pengemasan                                                                                                         |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|4  | Product               | Ya            | Item yang ditawarkan                                                                                               |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|5  | UoM                   | Tidak         | Satuan pengukuran unit                                                                                             | 
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|6  | Description           | Tidak         | Deksripsi item yang ditawarkan                                                                                     |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|7  | Refunded Item         | Tidak         | Pengembalian item                                                                                                  |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|8  | Note Line Material    | Tidak         | List dari material yang merupakan paket dari item                                                                  |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+


Note Lines Material
^^^^^^^^^^^^^^^^^^^

Note Lines Material berisi daftar material yang merupakan paket dari item.



.. image:: /img/dn-3-edit.png

(Gambar Note Lines Material - Tree)



.. image:: /img/dn-note-lines-material.png

(Gambar Note Lines Material - Form / Detail)


Field yang ada pada **Note Line Material**:


+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                                                         |
+===+=======================+===============+====================================================================================================================+
|1  | Refunded Item         | Ya            | Pengembalian Item                                                                                                  |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|2  | UoM                   | Ya            | Satuan pengukuran unit                                                                                             |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|3  | Serial Number         | Tidak         | No Batch Stock                                                                                                     |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|4  | State                 | Tidak         | Status                                                                                                             |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|5  | Stock Move            | Tidak         | Perpindahan Stock                                                                                                  | 
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|6  | Description           | Tidak         | Deksripsi item yang ditawarkan                                                                                     |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|7  | Product               | Ya            | Item yang ditawarkan                                                                                               |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|8  | Delivery Note Line    | Ya            | Catatan pemesanan                                                                                                  |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|9  | Qty                   | Ya            | Banyaknya item yang ditawarkan                                                                                     | 
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|10 | OP Line               | Tidak         |                                                                                                                    |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|11 | unknown               | Tidak         |                                                                                                                    |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+


Packing Lines
-------------

Packing Lines merupakan list mengenai detail kemasan.

.. image:: /img/dn-packaging-list.png

(Gambar Packing Lines - Form / Detail)


Field yang ada pada **Packing Lines**:


+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                                                         |
+===+=======================+===============+====================================================================================================================+
|1  | Package               | Ya            | Paket                                                                                                              |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|2  | Color Code            | Ya            | Kode Warna                                                                                                         |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|3  | Urgent                | Tidak         | Menunjukkan tingkat urgent dari paket                                                                              |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|4  | No                    | Ya            | Id dari item                                                                                                       |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|5  | Description           | Ya            | Deksripsi item yang ditawarkan                                                                                     | 
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|6  | Product               | Ya            | Item yang ditawarkan                                                                                               |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|7  | Quantity              | Ya            | Banyaknya item yang ditawarkan                                                                                     |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|8  | Uom                   | Ya            | Satuan pengukuran unit                                                                                             |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|9  | measurement           | Ya            | Banyaknya item yang ditawarkan                                                                                     | 
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|10  | Weight               | Ya            | Berat dari item                                                                                                    |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+


Notes
-----

Notes berisi catatan internal.

.. image:: /img/dn-notes.png

(Gambar Packing Lines - Form / Detail)


Field yang ada pada **Notes**:


+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                                                         |
+===+=======================+===============+====================================================================================================================+
|1  | Note                  | Ya            | Catatan internal                                                                                                   |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+


Others
------

.. image:: /img/dn-others.png

(Gambar Others - Form / Detail)


Field yang ada pada **Others**:


+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                                                         |
+===+=======================+===============+====================================================================================================================+
|1  | Stock Picking         | Tidak         |                                                                                                                    |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|2  | Postpone Picking      | Tidak         |                                                                                                                    |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+


Proses Return Products
----------------------

Proses Return Products berisi informasi mengenai pengembalian barang.

.. image:: /img/dn-proses-return-products.png

(Gambar Proses Return Products - Form / Detail)


Field yang ada pada **Proses Return Products**:


+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|NO | Fileds                | Harus Diisi   | Keterangan                                                                                                         |
+===+=======================+===============+====================================================================================================================+
|1  | Reference             | Ya            | Referensi                                                                                                          |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|2  | Supplier              | Ya            | Penyedia produk                                                                                                    |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|3  | Back Order of         | Ya            |                                                                                                                    |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|4  | Source Document       | Ya            | Sumber Dokumen                                                                                                     |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|5  | Creation Date         | Ya            |                                                                                                                    | 
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|6  | Scheduled Time        | Ya            |                                                                                                                    |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|7  | Invoice Control       | Ya            |                                                                                                                    |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|8  | Stock Journal         | Ya            |                                                                                                                    |
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+
|9  | Status                | Ya            | Status                                                                                                             | 
+---+-----------------------+---------------+--------------------------------------------------------------------------------------------------------------------+