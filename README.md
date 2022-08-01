###### Nama: Fari' Affrizal S.
###### Kelas: RPL 1
###### No.Absen: 25
## modul-3
### Routing
>Tugas soal nomor 1 Buatlah Route yang menuju kehalaman Kategori dan
>Tugas soal nomor 2 Buatlah halaman tambah data disetiap route
dibawah ini codenya
```
<?php

namespace App\Http\Controllers;

use Illuminate\Http\Request;

class KategoriController extends Controller
{
    public function index()
    {
        return '<a href="/kategori/add">Menuju kategori add</a>';
    }

    public function add()
    {
        return 'Membuat halaman tambah data di setiap route kategori<p>
        <a href="/kategori">menuju halaman kategori</a></p>';
    }
}

```
cara melihat hasilnya silahkan mengaktifkan xampp dan cmd server contohnya seperti digambar ini;

![image](https://user-images.githubusercontent.com/109929687/182095439-ca7fa233-ba2c-4648-a7e8-f846da6c4a47.png)
