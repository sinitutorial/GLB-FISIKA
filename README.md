# GLB-FISIKA
class glb:
    def menu(self):
        menu = '''
>>>MENU GLB<<<
Hi, saya adalah FisPy, akan membantumu mengerjakan soal GLB. Silakan pilih salah satu (dengan angka):
[1] menghitung kecepatan
[2] menghitung jarak
[3] menghitung waktu
[4] keluar
        '''
        return menu
    def menghitung_kecepatan(self, jarak, waktu):
        hasil = int(jarak)/int(waktu)
        return hasil
    def menghitung_jarak(self, kecepatan, waktu):
        hasil = int(kecepatan)*int(waktu)
        return hasil
    def menghitung_waktu(self, kecepatan, jarak):
        hasil = int(jarak)/int(kecepatan)
        return hasil
 
while True:
    print(glb().menu())
    pilih = input('Saya pilih nomor :')
    if pilih == '1':
        print('Oke Bos, FisPy akan menghitung kecepatan')
        while True:
            benda = input('masukkan nama benda :')
            jarak = input('masukkan jarak (dalam meter) :')
            waktu = input('masukkan waktu (dalam sekon) :')
            hasil_kecepatan = f'besar kecepatan yang diperlukan {benda} untuk menempuh jarak {jarak} meter selama {waktu} sekon adalah {glb().menghitung_kecepatan(jarak, waktu)} m/s'
            print(hasil_kecepatan)
            print('[1] Lagi \n[2] Kembali')
            pilih2 = input('Saya pilih :')
            if pilih2 == '1': continue
            else: break
 
    elif pilih == '2':
        print('Oke Bos, FisPy akan menghitung jarak')
        while True:
            benda = input('masukkan nama benda :')
            kecepatan = input('masukkan kecepatan (dalam m/s) :')
            waktu = input('masukkan waktu (dalam sekon) :')
            hasil_jarak = f'jarak yang ditempuh oleh {benda} selama {waktu} sekon dengan kecepatan {kecepatan} m/s adalah {glb().menghitung_jarak(waktu=waktu, kecepatan=kecepatan)} meter'
            print(hasil_jarak)
            print('[1] Lagi \n[2] Kembali')
            pilih2 = input('Saya pilih :')
            if pilih2 == '1': continue
            else: break
 
    elif pilih == '3':
        print('Oke Bos, FisPy akan menghitung waktu')
        while True:
            benda = input('masukkan nama benda :')
            kecepatan = input('masukkan kecepatan (dalam m/s) :')
            jarak = input('masukkan jarak (dalam meter) :')
            hasil_waktu = f'waktu yang diperlukan oleh {benda} untuk menempuh jarak {jarak} meter dengan kecepatan {kecepatan} adalah {glb().menghitung_waktu(jarak=jarak, kecepatan=kecepatan)} sekon'
            print(hasil_waktu)
            print('[1] Lagi \n[2] Kembali')
            pilih2 = input('Saya pilih :')
            if pilih2 == '1': continue
            else: break
    else: break
