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
    Dari cobebase atau landingpage ini saya ingin membuat website company profile toko sembako.
    selain itu website tersebut harus memiliki halaman admin panel yang berfungsi untuk manajemen kontennya.
    untuk databasenya gunakan supabase dan saya sudah menghubungkan konfigurasi MCP nya, jadi kamu sudah bisa langsung akses. apakah kamu bisa bantu? tanyakan jika kamu ada pertanyaan.
    ```
8.    
