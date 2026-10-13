# Nabila-Pertiwi-Putri_09011382530165_Tugas-6

# 1. Eksekusi seluruh profile yang ada :
a. Edit file profile /etc/profile dan tampilkan pesan sebagai berikut :
echo “Profile dari /etc/profile”
<img width="1280" height="800" alt="1a" src="https://github.com/user-attachments/assets/04bf3cfb-ee9a-4427-be5e-1091638b6ac2" />


b. Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu :
/home/stD02001/.bash_profile
/home/. stD02001/.bash_login
/home/mahasiswa/.profile
/home/mahasiswa/.bashrc
Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap
file tersebut, cantumkan instruksi echo, misalnya pada /home/
mahasiswa/.bash_profile :
echo “Profile dari .bash_profile”
Lakukan hal yang sama untuk file lainnya, sesuaikan tampilan dengan nama file
yang bersangkutan.
<img width="1280" height="800" alt="1b" src="https://github.com/user-attachments/assets/f6d46d3a-1a27-4a23-a493-8481880c89f7" />


c. Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai
berikut:
$ su mahasiswa
$ exit
kemudian gunakan opsi – sebagai berikut :
$ su – mahasiswa
$ exit
Jelaskan perbedaan kedua utilitas tersebut.
<img width="1280" height="800" alt="1c" src="https://github.com/user-attachments/assets/52b9e119-51c0-46bf-b4ec-2fb8fce68bf6" />


# 2. Prompt String (PS)
a. Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan
dengan parameter nama variable tersebut, agar perubahan variable PS1 dikenal
oleh semua shell
PS1=’> ‘
export PS1
<img width="1280" height="800" alt="2a" src="https://github.com/user-attachments/assets/cfacdce6-8d18-4438-b26d-82c8a3745ea2" />


b. Eksperimen hasil PS1 :
$ PS1=“\! > “
69 > PS1=”\d > “
Mon Sep 23 > PS1=”\t > “
10:10:20 > PS1=”Saya=\u > “
Saya=mahasiswa > PS1=”\w >”
~ > PS1=\h >”
<img width="1280" height="800" alt="2b" src="https://github.com/user-attachments/assets/c6eab4ab-01b4-4118-ae2d-71c27056caef" />


# 3. Logout
logout
Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi
Echo “Terima kasih atas sesi yang diberikan”
Sleep 5
clear
<img width="1280" height="800" alt="3" src="https://github.com/user-attachments/assets/857323fb-71d2-49d0-bbd6-47b5a0b1148f" />


# 4. Bash script
a. Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing :
p1.sh
#! /bin/bash
echo “Program p1” ls –l
p2.sh
#! /bin/bash
echo “Program p2” who
p3.sh
#! /bin/bash
echo “Program p3” ps x
<img width="1280" height="800" alt="4a" src="https://github.com/user-attachments/assets/307c3f4b-5fc0-4f99-ab99-45cae0961fe6" />


b. Jalankan script tersebut sebagai berikut :
$ ./p1.sh ; ./p3.sh ; ./p2.sh
$ ./p1.sh &
$ ./p1.sh $ ./p2.sh & ./p3.sh &
$ ./p1.sh ; ./p3.sh ) &
<img width="1280" height="800" alt="4b" src="https://github.com/user-attachments/assets/83926c22-e969-449d-9919-9776359a9c5a" />
<img width="1280" height="800" alt="4b" src="https://github.com/user-attachments/assets/a2040f34-e682-4cf3-a904-aff58c73a2f7" />
<img width="1280" height="800" alt="4b" src="https://github.com/user-attachments/assets/8182e3ec-037a-43d4-ad83-446b4a94d48c" />
<img width="1280" height="800" alt="4b" src="https://github.com/user-attachments/assets/7c4e414a-906c-4ed7-9d4c-89cea47d498e" />

# 5. Jobs
a. Buat shell-script yang melakukan loop dengan nama pwaktu.sh, setiap 10 detik,
kemudian menyimpan tanggal dan jam pada file hasil.
#!/bin/bash
while [ true ]
do
date >> hasil
sleep 10
done
<img width="1280" height="91" alt="5a" src="https://github.com/user-attachments/assets/45c6b4da-88c4-4f0c-97f0-705195f52d19" />


b. Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di
background sebagai berikut :
$ jobs
$ find / -print > files 2>/dev/null &
$ jobs
<img width="1280" height="139" alt="5b" src="https://github.com/user-attachments/assets/bc568394-b6d3-4ab8-b09d-455e6a6669bd" />


c. Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program
tersebut ke background
$ fg %1
$ bg
<img width="1280" height="125" alt="5c" src="https://github.com/user-attachments/assets/9144e519-48e7-468f-8da3-cdc168db1703" />


d. Stop program background dengan utilitas kill
$ ps x
$ kill [Nomor PID]
<img width="1280" height="627" alt="5d" src="https://github.com/user-attachments/assets/bfcd8acf-ed16-42ab-8c95-e48b85f60a50" />
<img width="1280" height="800" alt="5d" src="https://github.com/user-attachments/assets/c6ca41bd-45ef-4539-aaae-50b3e44a42c0" />


# 6. History
a. Ganti nilai HISTSIZE dari 1000 menjadi 20
$ HISTSIZE=20
$ h
<img width="1280" height="376" alt="6a" src="https://github.com/user-attachments/assets/b334f017-87df-4c7e-8d92-bf05a811876f" />

b. Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang
terakhir dilakukan
$ !-5
<img width="1280" height="800" alt="6b" src="https://github.com/user-attachments/assets/d9480a3d-96fc-4933-8194-79e2c13dbfc6" />


c. Ulangi instruksi yang terakhir. Gunakan juga ^P dan ^N untuk bernavigasi pada
history bufer
$ !!
<img width="1280" height="800" alt="6c" src="https://github.com/user-attachments/assets/dfa2a060-e883-415b-bcc6-9c87dcf548c8" />


d. Ulangi instruksi pada history bufer nomor 150
$ !150
<img width="1280" height="800" alt="6d" src="https://github.com/user-attachments/assets/a8e15b95-33c8-4096-9560-6dd70b341658" />


e. Ulangi instruksi dengan prefix “ls”
$ !ls
<img width="1280" height="800" alt="6e" src="https://github.com/user-attachments/assets/2bbd786a-96b7-4c83-a1ae-3c499c7e94d2" />
