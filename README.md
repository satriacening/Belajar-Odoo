# Belajar-Odoo
Documentation by self

Inherit model yang sudah ada pada odoo
  1. buat dependensi module yang akan di inherit. dengan cara tambah ``depend['nama_modul']`` di dalam __manifest__.py
  2. buat file.py baru pada folder model. buat class dalam file tersebut
  3. buat variabel inherit ke model yang akan di tuju. contoh disini akan meng inherit module hr.expense 
     * atribut super berfungsi untuk mengexecute func original setelah func custom berjalan
     * jika func ori dari module asli tidak akan di exexute maka tidak perly menambahkan atribut super
     
    class HrExpense(models.Model):
      _inherit = ['hr.expense']
  
      def nama_func(self):
        (program custom)
        super(HrExpense, self).nama_func()
