"""
Program ini dibuat untuk mengerjakan project untuk membuat program kasir
"""
#Import library yang akan digunakan
import numpy as np

class Transaction():
  
  """ Function berfungsi untuk menginisialisasi class transaction dan dictionary kosong """

  def __init__(self) :
    print("Transaction success")
    self.items = {}

  """
  Function add item, berfungsi untuk menginput item kedalam dictionary
  Input : nama_item (str) , jumlah_item (int) , harga_item(int)
  output : dictionary
  """
  def add_item(self, nama_item, jumlah_item, harga_item) :
    self.items.update({nama_item : [jumlah_item, harga_item]})

  """
  Function update_item_name, berfungsi untuk merubah nama item yang akan dibeli,
  tanpa mengubah item yang sebelumnya sudah diinput
  Input : update_nama_item (str)
  output : updated dictionary
  """
  def update_item_name(self, nama_item, update_nama_item) :
    self.items[update_nama_item] = self.items.pop(nama_item)

  """
  Function update_item_qty, berfungsi untuk merubah jumlah item yang akan dibeli,
  tanpa merngubah item sebelumnya yang sudah diinput
  Input : update_jumlah_item (int)
  output : updated dictionary
  """
  def update_item_qty(self, nama_item, update_jumlah_item) :
    #value_updated adalah variabel untuk menampung value yang ada didalam dictionary 
    value_updated1 = self.items[nama_item]

    value_updated1[0] = update_jumlah_item
    self.items[nama_item] = value_updated1

  """
  Function update_item_price, berfungsi untuk merubah harga item yang akan dibeli,
  tanpa mengubah item sebelumnya yang sudah diinput
  Input : update_harga_item (int)
  output : updated dictionary
  """
  def update_item_price(self, nama_item, update_harga_item) :
    #value_updated adalah variabel untuk menampung value yang ada didalam dictionary 
    value_updated2 = self.items[nama_item]

    value_updated2[1] = update_harga_item
    self.items[nama_item] = value_updated2

  """Function delete_item, berfungsi untuk menghapus item yang akan dibeli"""
  def delete_item(self, nama_item) :
    self.items.pop(nama_item)

  """Function reset_transaction, berfungsi untuk membatalkan seluruh transaksi"""
  def reset_transaction(self) :
    while(len(self.items)):
      self.items.popitem()

  """
  Function check_order, berfungsi untuk checking apakah item pesanan sudah 
  tersimpan dengan benar
  """
  def check_order(self) :
  #menggunakan loop untuk proses checking
    for key, value in self.items.items():
      nama_item = key
      jumlah_item = value[0]
      harga_item = value[1]

      if type(nama_item) !=str :
        print("Terdapat kesalahan input data")
      elif type(jumlah_item) != int :
        print("Terdapat kesalahan input data")
      elif type(harga_item) !=int :
        print("Terdapat kesalahan input data")
      else :
        print("Pemesanan sudah benar")

    """Function display berfungsi untuk menampilkan pesanan yang sudah diinput"""
    #Diskon rate yang akan didapat
  def total_price(self) :
    diskon_200000 = 5/100
    diskon_300000 = 8/100
    diskon_500000 = 10/100

    total_belanja = 0

    for value1 in self.items.values() :
      harga_barang = value1[0] * value1[1]
      total_belanja = total_belanja + harga_barang

      #menggunakan branching untuk menentukan besaran diskon yang didapatkan
    if total_belanja > 200000 and total_belanja <= 300000 :
      total_belanja_setelah_diskon =  total_belanja - (total_belanja * diskon_200000)
    elif total_belanja > 300000 and total_belanja <= 500000 :
      total_belanja_setelah_diskon =  total_belanja - (total_belanja * diskon_300000)
    elif total_belanja > 500000 :
      total_belanja_setelah_diskon =  total_belanja - (total_belanja * diskon_500000)
    else:
      total_belanja_setelah_diskon =  total_belanja

    print(f"Item yang dibeli antara lain : {self.items} \n Total harga yang harus dibayar adalah Rp. {total_belanja} \n Tagihan setelah diskon adalah Rp. {total_belanja_setelah_diskon}")  
