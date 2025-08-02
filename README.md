## Workshop Vibe Code dengan Gemini CLI
# Use Case: Membuat Company Profile Dinamis

Prerequisites
1. Supabase
   Kunjungi link : [supabase](https://supabase.com/), kemudian buat akun.
   - Buat organisasi
   - Buat Projek
   - Simpan Credential-nya
      - Projek ID:
      - anon public:
      - Url Proj:
      - Token:
   -  
3. Visual Code
   [Download](https://code.visualstudio.com/)
5. Gemini CLI
   - [Node.js version 20](https://nodejs.org/en/download) atau yang lebih tinggi
   - Jalankan perintah berikut pada terminal:
     ```bash
     npm install -g @google/gemini-cli
     ```
     kemudian run:
     ```bash
     gemini
     ```
     
   -  Explorasi command yang ada pada gemini cli
6.  Download Template UI

# Praktek
1. Buat folder dan beri nama 'Workshop_tridi'
2. File template UI yang sudah didownload pindahkan ke folder ini, kemudian extract atau unzip.
3. Copy dan Paste folder '.gemini' ke folder ini. Di dalam forlder ini ada file settings.json untuk konfigurasi MCP yang akan menghubungkan ke supabase sebagai basis datanya.
   Edit dan sesuaikan dengan credetnial supabase yang sudah kamu simpan:
    ```bash
     "mcpServers": {
      "supabase": {
        "command": "cmd",
        "args": [
          "/c",
          "npx",
          "-y",
          "@supabase/mcp-server-supabase@latest",
          
          "--project-ref=[isi dengan id projek]"
        ],
        "env": {
          "SUPABASE_ACCESS_TOKEN": "[isi dengan token]"
        }
      }
    }
     ```
   
5. Klik kanan dan pilih terminal,
    kemudian run:
     ```bash
     gemini
     ```
6. Kita akan meminta gemini untuk meng-summary codebase yang ada (UI frontend) dengan memberikan instruksi berikut:
  ```bash
  Tolong berikan saya summary dari codebase ini
  ```
7. Prompt selanjutnya minta gemini untuk membuatkan rencana pengembangan website company profile toko sembako
    ```bash
    Saya ingin membangun sebuah website company profile untuk toko sembako, menggunakan basis dari codebase atau landing page yang sudah tersedia.
   Website ini harus memiliki fitur utama berikut:   
   Produk (menampilkan daftar produk sembako)  
   Testimoni pelanggan   
   Kontak (form atau informasi kontak)   
   Tentang Kami (About)
       
   Selain itu, perlu disediakan halaman admin panel untuk melakukan manajemen konten dari fitur-fitur tersebut (CRUD produk, input testimoni, dll).
   Untuk backend-nya:   
   Gunakan Supabase sebagai database dan object storage.   
   Konfigurasi MCP (Managed Cloud Provider) sudah saya hubungkan, jadi seharusnya kamu sudah bisa langsung mengakses proyek Supabase-nya.   
   Apakah kamu bisa bantu membuatkan struktur proyek dan implementasinya berdasarkan kebutuhan tersebut? Jika ada hal yang perlu ditanyakan sebelum mulai, silakan tanyakan.
    ```
8. AI code akan meminta beberapa data inputan sesuai dengan fitur website yang kita berikan sebelumnya, silahkan sesuaikan dengan kebutuhan website kamu
9. Pada workshop ini kita membangun websitenya menggunakan framework next.js dan untuk menjalankan aplikasinya menggunakan perintah 'npm run dev'. perintah ini biasaya dieksekusi langsung oleh AI, kadang AI suruh kita untuk menjalankan perintah tersebut sendiri di direktori atau folder cobedabse kita. 
