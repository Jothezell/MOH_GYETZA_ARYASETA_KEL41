class ManajemenMahasiswa: def tampilkan_header(self): 
  print("=========================================") 
  print(" SISTEM PENILAIAN TUGAS MAHASISWA (PBO) ") 
  print(" [kelompok 41] ") 
  print("=========================================")

#daftar menu
def tampilkan_menu(self, daftar_menu):
    print("--- MENU UTAMA ---")
    for i, menu in enumerate(daftar_menu, start=1):
        print(f"{i}. {menu}")

# Menghasilkan nilai bobot dasar default untuk penilaian
def ambil_bobot_default(self):
    return 1.0

# --- RETURN TYPE FUNCTION (Berparameter) ---
# Menghitung nilai akhir dan menentukan status kelulusan berdasarkan pengkondisian & perulangan
def evaluasi_nilai_mahasiswa(self, jumlah_tugas, total_nilai, bobot):
    rata_rata = 0.0
    
    # PENGKONDISIAN: Memastikan tidak terjadi pembagian dengan nol
    if jumlah_tugas > 0:
        #looping
        for _ in range(1):
            rata_rata = (total_nilai / jumlah_tugas) * bobot

    #if statement
    if rata_rata >= 80:
        return f"Lulus dengan Pujian (Nilai Akhir: {rata_rata:.2f})"
    elif rata_rata >= 60:
        return f"Lulus (Nilai Akhir: {rata_rata:.2f})"
    else:
        return f"Tidak Lulus / Perbaikan (Nilai Akhir: {rata_rata:.2f})"
#program utama if name == "main": sistem = ManajemenMahasiswa()

# Memanggil Non-Return Type Method tanpa parameter
sistem.tampilkan_header()

menu = ["Hitung Penilaian Mahasiswa", "Lihat Informasi Bobot", "Keluar"]
pilihan = 0

# PERULANGAN (WHILE) untuk menjalankan program secara berulang
while pilihan != 3:
    sistem.tampilkan_menu(menu)
    try:
        pilihan = int(input("Pilih menu (1/2/3): "))
    except ValueError:
        print("\nInput harus berupa angka!")
        continue

    #navigasi menu
    if pilihan == 1:
        try:
            jml_tugas = int(input("\nMasukkan jumlah tugas yang dikumpulkan: "))
        except ValueError:
            print("Jumlah tugas harus berupa angka.")
            continue
            
        total_nilai_sementara = 0
        
        # perulangan for untuk menginput nilai tugas
        for i in range(1, jml_tugas + 1):
            nilai = float(input(f"Masukkan nilai tugas ke-{i} (0-100): "))
            total_nilai_sementara += nilai

        bobot_dasar = sistem.ambil_bobot_default()

        hasil_akhir = sistem.evaluasi_nilai_mahasiswa(jml_tugas, total_nilai_sementara, bobot_dasar)
        
        print("[HASIL EVALUASI]")
        print(f"Status: {hasil_akhir}")

    elif pilihan == 2:
        bobot = sistem.ambil_bobot_default()
        print(f"\nInformasi: Bobot dasar sistem saat ini adalah {bobot}")

    elif pilihan == 3:
        print("Terima kasih telah menggunakan program ini. [Watermark Kelompok 41]")

    else:
        print("Pilihan tidak valid. Silakan coba lagi.")
