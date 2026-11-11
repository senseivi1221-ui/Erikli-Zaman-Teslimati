# Erikli: Zaman Teslimatı

**Oyunlaştırma** dersi için Unity ile yapılmış 2D fizik tabanlı bir sürüş ve teslimat oyunu. Proje adı: *Sekans Su*.
Hazırlayan: **Yiğit Efe Erkişi** · Stüdyo: **BUDU GAMES** · Sürüm 1.0 · Kasım 2026

Erikli'nin sucusu sabah işe çıkarken bir zaman portalına kapılır. 1850 İstanbul, 1955 Anadolu, Taş Devri, İpek Yolu ve 2026 dağ köyünde o çağın aracıyla kapı kapı damacana teslim eder. Araçların tekerlekleri **WheelJoint2D** ile bağlıdır; sert sürüşte damacanalar zıplar ve su döker. Her evin önünde birinci şahıs kapı sahnesi açılır: zil, ödeme, damacana ve imza.

## Bağlantılar
- **Oyna (itch.io):** https://yigitefeerkisi.itch.io/erikli-zaman-teslima
- **Proje dosyaları (Release):** eklenecek

## Kontroller
| Eylem | Klavye | Fare / dokunmatik |
|---|---|---|
| Gaz | D, W, Sağ ok | Sağ pedal |
| Fren / geri | A, S, Sol ok | Sol pedal |
| Teslim et | E / Enter (evin önünde, yavaşken) | TESLİM ET düğmesi |
| Duraklat | Esc / P | Duraklat düğmesi |
| Kapı sahnesi | — | Zile, paraya / POS'a, damacanaya tıkla, belgeye imza at |

## Sekanslar
| # | Çağ | Araç | Kapı | Not |
|---|---|---|---|---|
| 1 | Eski İstanbul (1850) | At arabası | 2 | Isınma turu |
| 2 | Anadolu Köyü (1955) | Römorklu traktör | 3 | İlk yokuşlar |
| 3 | Taş Devri | Taş tekerlekli araba | 3 | Kaygan tekerlekler, hızlı gidince su çalkalanır |
| 4 | İpek Yolu (1200'ler) | Deve arabası | 4 | Dik kum tepeleri |
| 5 | Bugün: Dağ Köyü (2026) | Kar zincirli kamyon | 4 | Kartla temassız ödeme, son kapıda Emrah Hoca |

## Oyunlaştırma
Mühür (1–3 yıldız), para ve bahşiş, puan, 6 rozet, unvanlar (Stajyer → Sekans Efsanesi), müşteri memnuniyeti, kilit açma ve finalde okunan teslimat belgeleri.

## Projeyi açma
1. Unity Hub → **Add** → bu klasörü seç (Unity 6, 6000.3 sürümü).
2. Üst menüden **Sekans Su → 1 - Oyun Sahnesini Kur** (sahneleri, araç prefablarını ve görselleri kurar).
3. `Assets/Scenes/MainMenu` sahnesini açıp Play'e bas.
4. Build için: **Sekans Su → Build Ayarlarını Yap**, sonra File → Build Profiles (Windows veya Web).

## Klasör düzeni
```
Assets/
  Art/Sprites/     araçlar, çağlar, evler, kapı teslimatı, giriş, arayüz, logolar
  Audio/           müzikler ve efektler
  Fonts/           Poppins, DejaVu Serif, Liberation Mono
  Scenes/          MainMenu, LevelSelect, Intro, Gameplay
  Scripts/
    Core/          GameSession (kayıt, mühür, rozet, unvan), AudioManager
    Data/          LevelDatabase, VehicleDatabase, DeliveryDatabase, GameArt
    Gameplay/      GameplayManager, TruckController (WheelJoint2D), CargoManager, WaterJug, TerrainGenerator
    UI/            MenuDirector, HUDController, DeliveryScene, BrandSplash, UIKit
    Intro/         IntroDirector (giriş), IntroEnding (final ve jenerik)
    Editor/        sahne kurucu, içe aktarma ve build ayarları
  StreamingAssets/ GDD.pdf (menüdeki "GDD" düğmesi açar)
```

## Lisans notu
Oyundaki bütün görseller, müzikler ve efektler bu proje için hazırlandı. Yazı tipleri açık lisanslıdır (Poppins: OFL; DejaVu Serif ve Liberation Mono: serbest lisans). Erikli markası ders kapsamında kullanılmıştır.
