# Dokumentasi Instalasi Tools 
Langkah pertama adalah membuka Windows Powershell dengan "run as administrator"
![PBO EU301 - 2 - Part 1 5-7 screenshot](https://user-images.githubusercontent.com/114419446/193272627-599a1d54-1fe0-4139-9e52-be5e9791005f.png)

Langkah kedua, ketikkan "install --wsl" pada tab Windows Powerhell dan tunggu instalasi
![PBO EU301 - 2 - Part 1 5-28 screenshot](https://user-images.githubusercontent.com/114419446/193273832-6704cf9c-f3ed-47e1-bc24-36aaad105ce9.png)

Langkah ketiga, ubah versi wsl ke wsl 2 dengan mengetik " wsl --set-default-version 2" dan tunggu konfirmasi
![PBO EU301 - 2 - Part 2 14-57 screenshot](https://user-images.githubusercontent.com/114419446/193275317-d917a8b4-2820-4d50-9056-afe7e0624e47.png)

Langkah keempat, install ubuntu versi 20.04 pada tab Windows Powershell dengan perintah "wsl --install -d Ubuntu 20.04
![PBO EU301 - 2 - Part 2 14-57 screenshot](https://user-images.githubusercontent.com/114419446/193275317-d917a8b4-2820-4d50-9056-afe7e0624e47.png)

Langkah kelima, sambil menunggu instalasi ubuntu, silahkkan download vscode dan menginstallnya sekaligus
![PBO EU301 - 2 - Part 2 17-57 screenshot](https://user-images.githubusercontent.com/114419446/193276136-664c0dd5-a8c4-46e8-b97b-ac08e1660892.png)

Setelah Ubuntu terinstalasi, akan muncul tab ubuntu yang menyuruh kita untuk membuat username dan password. isi dan lanjut ke tahap selanjutnya

![PBO EU301 - 2 - Part 2 21-40 screenshot](https://user-images.githubusercontent.com/114419446/193279609-e3cad3ee-27c6-49f2-b725-98cf9b0919cf.png)

Langkah keenam, kembali ke tab Windows Powershell dan konfigurasi ubuntu dengan perintah "Ubuntu2004 config --default-user root"
![PBO EU301 - 2 - Part 2 22-15 screenshot](https://user-images.githubusercontent.com/114419446/193281084-de9aee34-0d97-49fd-af8e-ae145553ee76.png)

Langkah ketujuh, tutup Windows Powershell dan buka terminal. lalu, setting terminal dengan mengganti default tab menjadi Ubuntu 20.04
![PBO EU301 - 2 - Part 2 24-50 screenshot](https://user-images.githubusercontent.com/114419446/193281932-ac73c156-3816-4d01-8f65-f572fea9aa1c.png)

# memasukkan plugin

Langkah ketujuh, buka ubuntu pada terminal lalu ketikkan "apt update" dan tunggu hingga selesai
![PBO EU301 - 2 - Part 2 26-0 screenshot](https://user-images.githubusercontent.com/114419446/193282267-11f9ba08-e02d-4b2d-a4fe-c669cd35265e.png)

Langkah kedelapan, buka web browser dan cari [ohmyzsh](https:/github.com/ohmyzsh/ohmyzsh) dan copy command curl
![PBO EU301 - 2 - Part 2 27-6 screenshot](https://user-images.githubusercontent.com/114419446/193283089-aced2027-dabc-442d-9e5a-0291f65de0db.png)

Langkah kesembilan, kembali ke terminal dan ketikkan "install zsh"
![PBO EU301 - 2 - Part 2 27-31 screenshot](https://user-images.githubusercontent.com/114419446/193283926-0abad225-76e5-4a5f-b9f5-f0f139349369.png)

Langkah kesepuluh, setelah selesai, paste perintah curl tadi ke terminal dan ketik "y" pada setiap pertanyaan
![PBO EU301 - 2 - Part 2 28-0 screenshot](https://user-images.githubusercontent.com/114419446/193284296-aced20a2-dc0d-40ec-9de7-1bc898f226fe.png)

Langkah kesebelas, clear terminal dan ketikkan " nano/root/.zshrc". lalu, ganti line ZSH_THEME="robbrussel" ke "agnoster" dan input ctrl+x -> y -> enter

![PBO EU301 - 2 - Part 2 29-17 screenshot](https://user-images.githubusercontent.com/114419446/193285147-06da4a37-1bf0-4947-9d1d-b9cd05185b71.png)

Langkah keduabelas, input lagi "source/root/.zshrc" pada terminal
Buka web browser, cari [oh-my-zsh](https://github.com/zsh-users/zsh-syntax-highlighting) lalu copy no 1 dan pastekan ke terminal
![PBO EU301 - 2 - Part 2 30-34 screenshot](https://user-images.githubusercontent.com/114419446/193285927-bbe7e802-b487-43d2-9d87-c030ee5d7025.png)

Ulang lagi, cari [oh my zsh](https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md)lalu copy no 1 dan pastekan ke terminal
![PBO EU301 - 2 - Part 2 32-30 screenshot](https://user-images.githubusercontent.com/114419446/193286718-9cc4be60-aa8d-4699-a781-8487b0ba9982.png)

Langkah ketigabelas, buka lagi "nano/root/.zshrc" lalu input f5 cari plugin 
Pada baris plugin=(git ), masukkan no 2 yang ada pada web tadi 
![PBO EU301 - 2 - Part 2 33-48 screenshot](https://user-images.githubusercontent.com/114419446/193287218-f5e1439d-74ec-4681-b2e7-0cef512d021c.png)

![PBO EU301 - 2 - Part 2 34-25 screenshot](https://user-images.githubusercontent.com/114419446/193287487-a42de21b-a065-47f6-a1d1-ebf37a574141.png)

ctrl+x -> y -> enter
ketikkan lagi "source/root/.zshrc" dan plugin akan aktif

# connect github

Langkah keempatbelas, masuk atau buat akun github, masuk ke setting -> SSH and GPG keys -> new SSH key
input "ssh-keygen" pada terminal dan kosongkan passphrase
![PBO EU301 - 2 - Part 2 49-30 screenshot](https://user-images.githubusercontent.com/114419446/193289220-fb76d99a-4955-4a49-8399-54e5d9064e81.png)

Langkah kelimabelas input cat /root/.ssh/id_rsa.pub
copy hasil ke key di tab github dan isi tittle dengan "wsl"
konfirmasi untuk mendapat SSH key

![PBO EU301 - 2 - Part 2 50-15 screenshot](https://user-images.githubusercontent.com/114419446/193289798-0c3800c1-a794-4ef4-b3b9-f02afe30b81a.png)

Langkah keenambelas, masih pada setting github, developer setting -> personal access token 
isi:
- note: wsl
- expiration: no
- select scopes: mark all
generate token dan simpan token tersebut


Langkah ketujuhbelas, kembali ke terminal, "mkdir perkuliahan" -> "cd perkuliahan" dan "mkdir bahasapemprograman" -> "cd bahasapemprograman"
lalu input "code .
![PBO EU301 - 2 - Part 2 54-15 screenshot (1)](https://user-images.githubusercontent.com/114419446/193291242-4ad8886e-c837-4b6c-a977-546956b69172.png)

ketika vscode terbuka, pilih "trust author"
![PBO EU301 - 2 - Part 2 54-26 screenshot](https://user-images.githubusercontent.com/114419446/193291512-de27ee25-d108-4adc-8eef-d9158ff38899.png)

Langkah kedelapanbelas, buka setting vscode -> sign in with github -> authorize vscode
![PBO EU301 - 2 - Part 2 55-24 screenshot](https://user-images.githubusercontent.com/114419446/193291887-14a9815d-041c-49de-b973-96f4cfa55237.png)

allow extension

langkah kesembilanbelas, buat folder dan isi dengan file "src.py" 
masukkan print ("hello"), sebagai test file
![PBO EU301 - 2 - Part 2 56-52 screenshot](https://user-images.githubusercontent.com/114419446/193292372-8f2f2fd2-7bf6-4457-8998-4b9c3cb87877.png)

langkah keduapuluh, pergi ke extension lalu search python dan install
open terminal, input "cd pert1" lalu "python3" -> "cd .."
input lagi "git init" -> "git add ." -> 'git commit -m "firstcommit"'
"git branch -M main" -> ketikkan "curl -u **'usergithubmu'** https://api.github.com/user/repos -d '("name":**"namareponya"**,"private":false)"
lalu enter passwordmu
![PBO EU301 - 2 - Part 2 60-21 screenshot](https://user-images.githubusercontent.com/114419446/193293218-c0ca9ab3-ab10-4983-811d-28f493939fbf.png)

![PBO EU301 - 2 - Part 2 1-3-45 screenshot](https://user-images.githubusercontent.com/114419446/193294277-33463bdd-f709-409c-9553-346f9f6219fe.png)

langkah keduapuluh satu, input "git remote add origin git@github.com:**USERGITHUBMU/NAMAREPO**.git
lalu input lagi "git push -u origin main" -> yes

![PBO EU301 - 2 - Part 2 1-4-40 screenshot](https://user-images.githubusercontent.com/114419446/193294700-b57f175a-32d4-4c0a-938b-fef0715d48bf.png)

langkah ke duapuluh dua, cek pada halaman utama githhub, jika sudah tersambung, maka akan ada file pada recent repository

![Screenshot 2022-09-30 214318](https://user-images.githubusercontent.com/114419446/193295359-f652d214-d743-4f42-8509-edd93333efaa.png)
