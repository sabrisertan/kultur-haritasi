# Nehir ve göl geometrileri

2026-11-15 · Britain Today, Chapter I, basılı s. 5–24.

Kitabın 23 nehir grubu ve sekiz gölü kaynak geometriyle gösterilir. Bütün 107 çalışma konusu korunur. Yeni coğrafi çizgiler ve yakınlaştırma sırası ★ kitap dışı görselleştirme olarak açıklanır; ek sınav konusu oluşturmaz.

## Kullanılan veri

- Büyük Britanya: [OS Open Rivers](https://www.ordnancesurvey.co.uk/products/os-open-rivers), 2026-10, GeoPackage. OGL v3.0. Contains OS data © Crown Copyright and database rights 2026.
- İrlanda adası: [Geofabrik / OpenStreetMap, 2026-11-14](https://download.geofabrik.de/europe/ireland-and-northern-ireland-261114-free.shp.zip), yalnız waterways katmanı. © OpenStreetMap contributors, ODbL 1.0. Büyük ZIP bütünüyle indirilmedi; HTTP byte-range ile yalnız ilgili üyeler alındı ve ZIP CRC doğrulaması yapıldı.
- Göller: Taylor, P. J. (2021), [Spatial inventory of UK waterbodies](https://doi.org/10.5285/b6b92ce3-dcd7-4f0b-8e43-e937ddf1d4eb), UKCEH v3.6. OGL v3.0, UKCEH; contains OS data © Crown copyright and database right.
- `water.geojson`: haritada kullanılan sadeleştirilmiş geometri, kaynak kayıt kimlikleri, lisanslar ve açıklamalar. OSM türevi İrlanda nehirleri ODbL 1.0 koşullarıyla sağlanır; OS/UKCEH kayıtlarının ayrı OGL lisansı korunur.

## Eşleştirme ve sadeleştirme

OS ad/alternatif ad alanları ile nehir adları eşleştirildi. Aynı adlı farklı akarsuları önlemek için Bristol Avon, English Tyne, Cardiff Taff, Conwy ve Trent konum sınırlarıyla süzüldü. İrlanda Bann için de aynı kontrol yapıldı. North/South Tyne, Tay–Tummel ve Trent–Humber kitap panel gruplarına bağlı tutuldu.

OS adlarının bent, havuz veya göl geçişinde değiştiği yerlerde yalnız yayımlanmış start/end node bağlantıları izlenerek kaynak ağın gerçek çizgileri alındı. Bağlantı başına arama sınırı 15 km; yeni düz çizgi veya tahmini güzergâh üretilmedi. Eklenen her kaynak parça `topologicalConnector` ile işaretlidir.

Aynı koordinattaki uçlar birleştirilir; dallar korunur. Douglas–Peucker toleransı yaklaşık 40 m, çıktıda koordinatlar beş ondalığa yuvarlanır. OSGB36/BNG koordinatları WGS84'e dönüştürülür; yayımlanmış referans koordinatla kontrol edildi. ★ Çizgi kalınlığı gerçek nehir genişliği değildir.

Kaynak ağ kusursuz bir navigasyon ağı değildir. Tyne'nin North Tyne üzerindeki göl geçişinde yaklaşık 9 km, Mersey'nin kanal geçişinde yaklaşık 1,4 km kaynak boşluğu korunur ve ilgili panelde ★ ile belirtilir. Bazı diğer nehirlerde bent/kısa kol geçişlerinde küçük kesintiler bulunur. Bu aralıklar tahmini çizgiyle kapatılmaz. Kaynak geometrisinin ana güzergâhları görünür; tüm kolların eksiksiz olduğu iddia edilmez.

Önceki küçük `uk-osm-network.geojson` arşivi ciddi parça eksikleri nedeniyle kullanılmadı. Natural Earth su geometrileri de bu sürümün nehir/göl verisine dahil edilmedi; Natural Earth yalnız mevcut ülke/kıyı zemininde kalır.

## Göl kimlikleri

Bütün göl kayıtları seçildi; yakın göletler veya Loch Lomond'un tek bir havzası kullanılmadı.

| Harita | UKCEH WBID |
|---|---:|
| Loch Ness | 18767 |
| Loch Lomond | 24447 |
| Lough Neagh | 50001 |
| Bala / Llyn Tegid | 34987 |
| Windermere | 29233 |
| Ullswater | 28955 |
| Derwent Water | 28965 |
| Coniston Water | 29321 |

## Çıktı denetimi

| Konu | Kaynak köşe sayısı | Gösterilen köşe sayısı |
|---|---:|---:|
| clyde | 1349 | 484 |
| tyne | 1485 | 530 |
| tay | 1257 | 418 |
| forth | 996 | 402 |
| wear | 928 | 344 |
| tees | 1420 | 489 |
| thames | 3210 | 1144 |
| trent | 2786 | 948 |
| mersey | 684 | 257 |
| clwyd | 879 | 260 |
| ouse | 2698 | 933 |
| severn | 2956 | 1078 |
| taff | 401 | 131 |
| avon | 1734 | 540 |
| mawddach | 406 | 119 |
| exe | 1172 | 402 |
| conwy | 672 | 190 |
| dwyryd | 205 | 83 |
| teifi | 1457 | 506 |
| shannon | 2988 | 629 |
| bann | 2468 | 390 |
| lagan | 3695 | 377 |
| foyle | 276 | 57 |
| loch-ness | 2227 | 147 |
| loch-lomond | 4332 | 771 |
| neagh | 6019 | 1364 |
| bala | 295 | 51 |
| windermere | 1229 | 250 |
| ullswater | 613 | 97 |
| derwentwater | 388 | 89 |
| coniston | 414 | 75 |

## Arşiv SHA-256

- `os-open-rivers.zip`: `abc676f979424772a9f52525b6acb30e1ae8ff6baa178e89c72a8a17e4f80678`
- `ireland-gis_osm_waterways_free_1.shp`: `1873e60cfb4118d41f718358bcdcf1f42ba75f4a766efa0ee1206629a5d03e02`
- `ireland-gis_osm_waterways_free_1.dbf`: `c78edc58c8e24c1e5fad317724db7a9891715ed23356d1859651db3f5f8da40d`
- `ukceh-lakes.zip`: `7396dc17b3c915eb4d8ad49ce4367444823ccc91db7098c77b23903c9516e60b`

Tam kaynak parça dökümü: `water.geojson`. Ham veri ve ara denetim: `/tmp/gop-map/hydro-sources/water-source-audit.json`.
