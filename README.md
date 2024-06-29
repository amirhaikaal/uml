@startuml

(*) --> "Login"

if "Login successful?" then
  --> "Pilih Menu"
  
  if "Menu: Lihat Saldo?" then
    --> "Lihat Saldo"
    --> "Kembali ke Menu"
  else if "Menu: Transfer Dana?" then
    --> "Transfer Dana"
    --> "Kembali ke Menu"
  else if "Menu: Bayar Tagihan?" then
    --> "Bayar Tagihan"
    --> "Kembali ke Menu"
  else if "Menu: Top Up E-Money?" then
    --> "Top Up E-Money"
    --> "Kembali ke Menu"
  else if "Menu: Minta e-Statement?" then
    --> "Minta e-Statement"
    --> "Kembali ke Menu"
  else if "Menu: Ubah Password?" then
    --> "Ubah Password"
    --> "Kembali ke Menu"
  else if "Menu: Kelola Notifikasi?" then
    --> "Kelola Notifikasi"
    --> "Kembali ke Menu"
  else if "Menu: Lihat Riwayat Transaksi?" then
    --> "Lihat Riwayat Transaksi"
    --> "Kembali ke Menu"
  else
    --> "Logout"
    --> (*)
  endif
  
else
  --> "Login Gagal"
  --> (*)
endif

@enduml
