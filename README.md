# VSCode Customizations

Panduan ini membantu Anda menyesuaikan tampilan Visual Studio Code menggunakan ekstensi **Custom CSS and JS Loader**.

---

### Ekstensi yang Digunakan:

- [Github Theme](https://marketplace.visualstudio.com/items?itemName=GitHub.github-vscode-theme)
- [JetBrains Icon Theme](https://marketplace.visualstudio.com/items?itemName=chadalen.vscode-jetbrains-icon-theme)
- [Fluent Icons](https://marketplace.visualstudio.com/items?itemName=miguelsolorio.fluent-icons)
- [Custom CSS and JS Loader](https://marketplace.visualstudio.com/items?itemName=be5invis.vscode-custom-css)

---

### Langkah-langkah:

1. **Install Ekstensi**
   - Install semua ekstensi yang disebutkan di atas melalui marketplace Visual Studio Code.

2. **Modifikasi `settings.json`**
   - Tambahkan konfigurasi berikut ke file `settings.json` di VS Code Anda.  
     **Catatan:** Pastikan untuk mencadangkan pengaturan Anda saat ini untuk mencegah kehilangan data.

    ```jsonc
    "vscode_custom_css.imports": [
        // Path absolut ke file custom CSS/JS Anda
        // Untuk Mac atau Linux:
        // "file:///Users/[your-username]/[path-of-custom-css]/vscode-custom/style.css",
        // "file:///Users/[your-username]/[path-of-custom-css]/vscode-custom/script.js"

        // Untuk Windows:
        // "file:///C:/[path-of-custom-css]/vscode-custom/style.css",
        // "file:///C:/[path-of-custom-css]/vscode-custom/script.js"
    ]
    ```

3. **Atur Izin Akses (Pengguna Linux)**
   - Sebelum mengaktifkan ekstensi, pengguna Linux perlu memberikan izin akses dengan menjalankan perintah berikut di terminal:
     ```bash
     sudo chown -R $(whoami) "$(which code)"
     sudo chown -R $(whoami) /usr/share/code
     ```

4. **Aktifkan "Custom CSS and JS Loader"**
   - Buka command palette (`Ctrl+Shift+P` atau `Cmd+Shift+P`) dan ketik **"Enable Custom CSS and JS"** untuk mengaktifkan kustomisasi.

5. **Sesuaikan File CSS/JS**
   - Modifikasi file `style.css` atau `script.js` Anda untuk mengubah tampilan Visual Studio Code. Berikut beberapa ide kustomisasi:
     - Mengubah warna latar belakang editor.
     - Mengubah gaya font pada sidebar atau tab.
     - Menambahkan animasi khusus untuk tab yang aktif.
     - Menyesuaikan ikon melalui CSS.

6. **Muat Ulang Ekstensi**
   - Setelah melakukan perubahan pada file CSS atau JS, muat ulang ekstensi dengan membuka command palette dan memilih **"Reload Custom CSS and JS"**.

7. **Verifikasi Perubahan**
   - Pastikan kustomisasi Anda telah diterapkan. Jika ada kesalahan atau perubahan tidak terlihat, periksa kembali path file atau sintaks di dalam file CSS/JS Anda.

---


