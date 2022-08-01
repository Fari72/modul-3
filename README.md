###### Nama: Fari' Affrizal S.
###### Kelas: RPL 1
###### No.Absen: 25
## modul-3
### Routing

>Tugas soal nomor 1 Buatlah Route yang menuju ke halaman Kategori

>Tugas soal nomor 2 Buatlah halaman tambah data disetiap route

pertama-tama membuat *"class KategoriController"* di VSCode ke terminal cara cepat *"Ctrl+Shift+`"* lalu salin command dibawah ini

```
php artisan make:controller KategoriController
```

dibawah ini tugas 1&2 codenya
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
dan cara memanggil-nya ke dalam halaman dengan url tersebut hasil codenya seperti dibawah ini
```
<?php
use Illuminate\Support\Facades\Route;
use App\Http\Controllers\BarangController;
use App\Http\Controllers\KategoriController;

// Route::get('/home', function (){
//     echo "<a href='".route('create')."'>Akses Route dengan nama</a>";
//     });

// Route::get('/create', function(){
//     echo "Route diakses menggunakan nama";
// })->nama('create');

Route::get('/barang', [BarangController::class, 'index']);
Route::get('/kategori', [KategoriController::class, 'index']);
Route::get('/barang/add', [BarangController::class, 'add']);
Route::get('/kategori/add', [KategoriController::class, 'add']);
```

cara melihat hasilnya silahkan mengaktifkan xampp dan cmd server contohnya seperti digambar bawah ini;

>![image](https://user-images.githubusercontent.com/109929687/182095743-8aa2f45b-32ec-4faa-858e-963ee0767f61.png)

>![image](https://user-images.githubusercontent.com/109929687/182095439-ca7fa233-ba2c-4648-a7e8-f846da6c4a47.png)

setelah mengaktifkan server silahkan menuju ke browser/ chrome salin link dibawah ini. Lalu tempelkan ke browser/ chrome
```
http://localhost:8000/kategori
```
hasilnya akan terlihat seperti ini

>![image](https://user-images.githubusercontent.com/109929687/182098433-f06fafe1-0b9d-4524-8fa5-f50140e38458.png)

jika di klik link tersebut maka akan menuju ke halaman kategori add seperti dibawah ini

>![image](https://user-images.githubusercontent.com/109929687/182098997-7308cfb1-79f6-40f8-a502-d5c490e16389.png)
