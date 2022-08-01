###### Nama: Fari' Affrizal S.
###### Kelas: RPL
###### No.Absen: 25
## modul-3
### Routing
Tugas soal nomor 1 Buatlah Route yang menuju kehalaman Kategori
dibawah ini adalah codenya
Tugas soal nomor 2 Buatlah halaman tambah data disetiap route
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
