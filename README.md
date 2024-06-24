# Django-Debug-Toolbar
Django Debug Toolbar menyediakan berbagai panel yang bisa Anda gunakan untuk menganalisis aplikasi Anda. Beberapa panel yang paling berguna termasuk:

- SQL: Menunjukkan semua query database yang dijalankan untuk halaman tersebut, termasuk waktu eksekusi setiap query.
- Timer: Menampilkan waktu yang dihabiskan di berbagai bagian request-response cycle.
- Headers: Menampilkan HTTP headers dari request dan response.
- Settings: Menampilkan semua setting Django yang sedang aktif.
= Static Files: Menunjukkan informasi tentang static files yang digunakan.
- Templates: Menampilkan informasi tentang template yang dirender, termasuk waktu rendering dan variabel konteks.

###Contoh Penggunaan
- SQL Panel: Anda bisa melihat query SQL yang dijalankan untuk halaman yang sedang Anda lihat. Ini sangat berguna untuk mengidentifikasi query yang lambat atau tidak efisien.
- Timer Panel: Anda bisa melihat berapa lama waktu yang dihabiskan untuk memproses berbagai bagian dari request, termasuk middleware, view, dan template rendering.
- Templates Panel: Anda bisa melihat template yang dirender dan waktu yang dihabiskan untuk setiap template, membantu Anda mengidentifikasi bagian mana dari aplikasi yang mungkin membutuhkan optimasi.

###Tips untuk Penggunaan di Produksi
Django Debug Toolbar sebaiknya hanya digunakan di lingkungan pengembangan. Pastikan untuk menonaktifkannya di produksi dengan memeriksa setting DEBUG di settings.py.

dokumentasi resmi : https://django-debug-toolbar.readthedocs.io/

## setup
- 📗&nbsp;&nbsp;Install
```bash
pip install django-debug-toolbar
```
- 📗&nbsp;&nbsp;Komfigurasi
```bash
INSTALLED_APPS = [
    ...
    'debug_toolbar',
]
```
```bash
MIDDLEWARE = [
    'debug_toolbar.middleware.DebugToolbarMiddleware',
    ...
]
```
```bash
INTERNAL_IPS = [
    '127.0.0.1',
]
```
- 📗&nbsp;&nbsp;URL Project
```bash
from django.urls import include, path

urlpatterns = [
    ...
    path('__debug__/', include('debug_toolbar.urls')),
]
```


