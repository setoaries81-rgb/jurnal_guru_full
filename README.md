# Jurnal Guru (Full) - Flutter

Ini project Flutter sederhana untuk Jurnal Guru (role Guru & Admin) yang:
- Menyimpan data kehadiran (lokal, memory)
- Guru bisa isi kehadiran: jam, kelas, materi, foto (path), keterangan
- Admin bisa lihat rekap, export CSV harian & bulanan
- Bisa dibuild jadi APK (Android) dan Web

## Cara pakai (singkat)
1. Ekstrak folder `jurnal_guru_full`
2. (Local dev) di mesin dengan Flutter terpasang:
   ```bash
   cd jurnal_guru_full
   flutter pub get
   flutter run -d chrome    # untuk web
   flutter run              # untuk device
   ```
3. Upload ke GitHub repo (upload semua isi folder).
4. Di Codemagic: hubungkan repo -> Start build. Workflow `build-android-web` akan:
   - menjalankan `flutter pub get`
   - menjalankan `flutter create .` (agar android/ios dir dibuat jika belum ada)
   - build APK release dan web

## Catatan
- Data saat ini disimpan di memory (DataService). Untuk produksi, hubungkan Firebase/Supabase/MySQL.
- CSV exporter membuat format CSV harian/bulanan sesuai kebutuhan.
