# İKA 2026 Proje Sitesi

İnsansız Kara Aracı yarışma projesinin Türkçe tanıtım ve tasarım rehberi.

## GitHub Pages

1. Bu klasörün içeriğini `ika-2026-sitesi` adlı public GitHub deposunun köküne aktarın.
2. GitHub'da `Settings > Pages > Build and deployment` alanında `GitHub Actions` seçin.
3. `main` dalına gönderilen commit, `.github/workflows/pages.yml` ile otomatik yayınlanır.

## Supabase

Site, son 12 geliştirme notunu `project_updates` tablosundan public REST API ile okur. Gerekli public URL ve publishable key, `index.html` içine yerleştirilmiştir. Publishable key tarayıcıda kullanılmak üzere tasarlanmıştır; secret/service-role anahtarı kullanılmaz.

Tablo şeması ve RLS, `supabase/migrations/20261017101753_create_public_project_updates.sql` dosyasında bulunur. Public ziyaretçiler yalnızca okuyabilir. Yeni güncellemeleri Supabase Dashboard'da `project_updates` tablosuna yetkili takım üyesi eklemelidir. Bu yol, siteden anonim içerik yazılmasını engeller.
