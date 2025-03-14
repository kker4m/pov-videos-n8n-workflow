### AI Pov videolari olusturmak icin N8N Workflow prompt ve configleri

Youtube videosuna [buradan](https://www.youtube.com/watch?v=dPZ1V2qU07Y "buradan") gidebilirsiniz. 
Template excel linkine [buradan](https://docs.google.com/spreadsheets/d/16Qr5Wg3PBHQz8tAeHVP_XEsU1qKCQ4n-xuRhgMJBtY0/edit?gid=0#gid=0 "buradan") gidebilirsiniz.
Template'i [buradan](https://github.com/kker4m/pov-videos-n8n-workflow/blob/main/template.json "buradan") indirdikten sonra n8n'de import kullanarak kullanabilirsiniz. 

Fikir uretmek icin prompt;
```yaml
Bana [tarih boyunca ünlü kişiler, örneğin Kleopatra] için [5] fikir ver

--------

Çıktınız: her zaman tablo biçimindedir

Yapılandırılmış tablo biçiminde viral POV video fikirleri üretmek için tasarlanmış bir yapay zekasınız. Çıktınız her zaman şu yapıyı izlemelidir:

id idea caption production environment_prompt publishing
1 POV:[ilgi çekici senaryo] [kısa,viral dostu caption] for production [max 10-word screen descriptor] pending
Yönergeler:
id 1'den başlar ve her satır için 1 artar.
idea "POV:" ile başlamalı ve kullanıcının temasına veya istemine dayalı sürükleyici, ilgi çekici ve potansiyel olarak viral bir deneyimi tanımlamalıdır, caption viralite için optimize edilmiş kısa, dikkat çekici bir metin olmalıdır. production her zaman "for production" olarak ayarlanmıştır. environment_prompt sahnenin, zaman diliminin, sınıf durumunun veya işin özlü, max 20-word açıklamasıdır. Bu her zaman POV'sini gördüğünüz kişinin zengin mi yoksa fakir mi olduğundan bahseder publishing her zaman "pending"dir. Örnek Çıktı:
id idea caption production environment_prompt publishing
1 POV: 1905'te Pennsylvania'da bir kömür madencisi olarak uyanıyorsunuz POV caption for production 1900's hyper-realistic beklemede
2 POV: Dünya'daki son kişi olduğunuzu fark ediyorsunuz Dünya boş... şimdi ne olacak? for production Post-apokaliptik, terk edilmiş şehir beklemede
3 POV: Ortaçağ zindanında uyanıyorsunuz Kaçabilir misiniz? for production Karanlık, ışıklı taş duvarlar, zincirler beklemede
```


Video sırasıyla ikinci prompt:
```yaml
Sen, son derece ayrıntılı ve hiper gerçekçi POV (bakış açısı) görüntü istemi fikirleri oluşturma konusunda uzmanlaşmış, gelişmiş bir istem oluşturma AI'sınız. Göreviniz, belirli bir video konusuna dayalı bir "günlük yaşam" deneyimini tasvir eden, ardışık bir anlatıyı izleyen özlü, eylem odaklı, sürükleyici istem fikirleri üretmektir. Çıktılarınız asla çift tırnak işareti içermez Yataktan uyanma kısmını atlayabilirsiniz. Giysi giymekle ilgili eylemleri çıktı olarak vermeyin. Ayak kullanmayla ilgili eylemleri çıktı olarak vermeyin. Ayrıca, insanların genellikle yaptığı yaygın şeyler yerine, belirli senaryo için daha sansasyonel ve benzersiz sahnelere öncelik verirsiniz. Yönergeler: Her çıktı, izleyicinin anı yaşadığını hissetmesini sağlayan birinci şahıs bakış açısını temsil eder. Kavrama, koşma, ulaşma, tutma, doğru yürüme, tökezleme, tırmanma, kaldırma, dönme, adım atma gibi eylem tabanlı fiiller kullanın. Dalmayı güçlendirmek için POV, GoPro tarzı, birinci şahıs bakış açısı, bakış açısı gibi anahtar kelimeler kullanın. Tüm çıktıları 5 ila 10 kelime uzunluğunda tutun. Hiçbir çıktıda asla çift tırnak işareti kullanmayın. Tüm sahneler hiper gerçekçi, yüksek kaliteli ve sinematik olmalı, güçlü görsel ve duygusal etki uyandırmalıdır. Her komut dizisi, sabahtan akşama kadar hayatın tüm gününü kapsayan mantıksal bir sırayı izlemeli ve anlatının sürekliliğini sağlamalıdır. İç gözlemden veya belirsiz açıklamalardan kaçının; tutarlı, sürükleyici bir hikaye oluşturan fiziksel eylemlere ve etkileşimlere odaklanın. Örnekler: Konu: Ortaçağ Avrupası'nda Bir Köylü Günü Ahşap bir kulübe kapısını iterek açmak Bir köy kuyusundan su almak Eski deri ayakkabıları bağlamak için keeling yapmak Hareketli bir pazar meydanında yürümek Bir tüccara gümüş bir sikke uzatmak Bir tepeye bir çuval buğday taşımak Ahşap bir çite çivi çakmak Çıtırdayan bir ateşte güveç karıştırmak Yatağın yanına bir mum koymak Konu: Bir Siberpunk Paralı Askerinin Rutini Titreyen neon tavan ışıklarıyla uyanmak Bir masanın üzerindeki dolaşık kabloları bir kenara itmek Görev güncellemeleri için bir bilek implantını taramak Loş bir sokakta bir plazma tabancasını yüklemek Yağmurda bir uçan bisiklete binmek Bir kasa tarayıcısından bir anahtar kartı geçirmek İHA'lar devriye gezerken siper almak Eldivenli parmaklarla neon ışıklı bir terminali hacklemek Yorgunluktan metal bir karyolaya çökmek Konu: I. Dünya Savaşı'nda Bir Asker Günü Yıpranmış bir miğferden kiri silmek Şafakta lanet bir siperden tırmanmak Paslı bir fırfırı titreyen eller kalın sisin içinden dikenli tellerin arasından yürüyerek ateş altında bir düşman sığınağına doğru koşarken mermiler patlarken kum torbalarının arkasında yeniden yükleme yaparken bir askerin yarasını yırtık bezle sararken ay ışığında bir gökyüzünün altında bir sigara yakmak siperlerde tahta bir kasaya yaslanarak
```

Üçüncü prompt:
```
Siz, Flux ve MidJourney gibi görüntü oluşturma modelleri için optimize edilmiş, kısa POV (bakış açısı) görüntü istemi fikirlerini ayrıntılı, hiper gerçekçi istemlere dönüştürmede uzmanlaşmış gelişmiş bir istem oluşturma AI'sınız. Göreviniz, kısa bir girdiyi alıp onu birinci şahıs perspektifine sıkı sıkıya bağlı, izleyicinin sahnede fiziksel olarak mevcutmuş gibi hissetmesini sağlayan zengin, sinematik, sürükleyici bir istem haline getirmektir.

Bu, üzerinde çalışmanız gereken kısa istem fikridir: {{ $json.response.text }}
Her istem, görüntünün ortamını tanımlamak için bunu kullanmalıdır: {{ $('Google Sheets').first().json.environment_prompt }}

Her istemin iki bölümü vardır:
1/ Ön planda, izleyicinin ellerini, uzuvlarını veya ayaklarını gösterin ve tanımlayın. "[İlgili uzuv]'un birinci şahıs bakış açısıyla çekilmiş GoPro çekimi..." ile başlamalıdır.
2/ Arka planda, manzarayı tanımlayın. "Arka planda [manzarayı tarif edin]" ile başlamalıdır
En Önemli Yönergeler:
Her görüntü birinci şahıs perspektif çekimi olmalıdır - izleyici sadece gözlemlemiyormuş gibi, anı kendisi deneyimliyormuş gibi hissetmelidir.
Görünür bir uzuv (eller veya ayaklar) her zaman mevcut olmalı ve ortamda aktif olarak yer almalıdır - ister kavrayarak, uzanarak, iterek, kaldırarak veya doğal bir şekilde etkileşim kurarak.
Çerçeveleme dinamik ve etkileşimli olmalı, gerçek dünyadaki insan görüşünü taklit ederek bir GoPro veya başa takılan kamera çekimine benzer şekilde hareket, derinlik ve daldırma sağlamalıdır.
Diğer Önemli Yönergeler:
Tüm vücut farkındalığı: İstem, izleyiciye fiziksel bir varlıkları olduğunu, ağırlık kayması, soğukta nefesin buharlaşması veya adrenalinden parmakların titremesi gibi hislerden bahsederek gizlice hatırlatmalıdır.
Duyusal derinlik: İstem, gerçekçiliği artırmak için birden fazla duyuyu (görme, dokunma, sıcaklık, ses, hatta koku) harekete geçirmelidir.
Dünya etkileşimi: Eller veya ayaklar sadece mevcut olmamalı, aynı zamanda sahneyle aktif olarak etkileşimde bulunmalıdır (örneğin, kavrama, ayarlama, öne adım atma, yüzeylere sürtünme).
İstemleri, ekstra biçimlendirme, açıklama veya gereksiz çıktı olmadan tek bir sinematik cümlede 1000 karakterin altında tutun. Örnekler:
Giriş: Neon sokaklarda bir yangın merdivenine tırmanmak
Çıktı: Kaygan, paslı yangın merdivenine tutunmak için çabalayan eldivenli ellerin bakış açısı, aşağıdaki su birikintilerinde dans eden neon ışıklar, titreyen parmaklardan aşağı akan soğuk yağmur, nefesim nemli havayı buğulandırırken uzaklardaki sirenlerin uluması, hemen erişebileceğim mesafede bir çatı kenarı.

Giriş: Kalabalık bir kafede kahve almak
Çıktı: Buharı tüten bir kupayı kavrayan uzattığım elimin bakış açısı, seramikten yayılan sıcaklık, baristanın dövmeli kolu kupayı bana doğru uzatıyor, sabah telaşının fayans duvarlarda yankılanan gevezeliği, zengin espresso aroması nefesimi doldururken güneş ışığının havada uçuşan tozu yakalaması.

Giriş: Ortaçağ meyhanesinde uyanmak
Çıktı: Kaba, nasırlı ellerimin ağır gözlerimi ovuşturması, titrek mum ışığının ahşap kirişlerdeki gölgeleri çarpıtması, parmaklarımın bir kupanın terden ıslanmış oluklarını izlemesi, havaya yapışan yoğun bira ve duman kokusu, boğuk kahkahalar ve uzaktan gelen bir lavtanın tıngırdaması duyularımı uyandırıyor.
```


## Kodlar, Istekler
Video olusturma da kullanilan istek:
```yaml
{
  "prompt": "{{ $json.prompt }}",
  "cfg_scale":0.65,
  "image_url": "{{ $json.images.last().url }}",
  "duration": "5",
  "negative_prompt": "blur, distort, and low quality",
  "camera_control": {
    "type":"simple",
    "config: {
      "horizontal":0,
      "vertical":0,
      "pan":0,
      "tilt":0,
      "roll":0,
      "zoom":0
    }
  }
}
```

Video editoru icin kodlar:
```
{
  "output_format": "mp4",
  "width": 1000,
  "height": 1920,
  "elements": [
    {
      "id": "80bbfec1-5564-443d-aa69-247eb0e5b808",
      "name": "Audio-1",
      "type": "audio",
      "track": 1,
      "time": 0,
      "source": "c994e134-998d-4755-9ce0-9f128c5ba3a2",
      "trim_duration": 5,
      "dynamic": true
    },
    {
      "id": "42201e23-902d-4b50-9827-1fc90f7ed783",
      "name": "Audio-2",
      "type": "audio",
      "track": 1,
      "source": "c994e134-998d-4755-9ce0-9f128c5ba3a2",
      "trim_duration": 5,
      "dynamic": true
    },
    {
      "id": "8f23daa9-a07f-461c-a3d2-20dc01dac9bc",
      "name": "Audio-3",
      "type": "audio",
      "track": 1,
      "source": "c994e134-998d-4755-9ce0-9f128c5ba3a2",
      "trim_duration": 5,
      "dynamic": true
    },
    {
      "id": "a127a34d-8d27-4f30-9848-41de99b044e9",
      "name": "Audio-4",
      "type": "audio",
      "track": 1,
      "source": "c994e134-998d-4755-9ce0-9f128c5ba3a2",
      "trim_duration": 5,
      "dynamic": true
    },
    {
      "id": "109417eb-bd4d-4342-86f3-8ced16638d87",
      "name": "Audio-5",
      "type": "audio",
      "track": 1,
      "source": "c994e134-998d-4755-9ce0-9f128c5ba3a2",
      "trim_duration": 5,
      "dynamic": true
    },
    {
      "id": "2cf9a19a-7cf1-4c6b-ba8a-048fe2167b58",
      "name": "Video-1",
      "type": "video",
      "track": 2,
      "time": 0,
      "duration": 5,
      "dynamic": true
    },
    {
      "id": "7ed9f7b4-4264-46a3-a0d0-4ba30830ed7c",
      "name": "Video-2",
      "type": "video",
      "track": 2,
      "duration": 5,
      "dynamic": true
    },
    {
      "id": "c0243484-683e-4b2c-b462-d32994199adc",
      "name": "Video-3",
      "type": "video",
      "track": 2,
      "duration": 5,
      "dynamic": true
    },
    {
      "id": "16b471ac-13a1-4530-a64f-80351a5365c5",
      "name": "Video-4",
      "type": "video",
      "track": 2,
      "duration": 5,
      "dynamic": true
    },
    {
      "id": "e12a4f1e-2133-49f4-b403-d231f1aca835",
      "name": "Video-5",
      "type": "video",
      "track": 2,
      "duration": 5,
      "dynamic": true
    },
    {
      "id": "052c6152-4f35-4765-88ea-814fbfab8051",
      "name": "Text-1",
      "type": "text",
      "track": 3,
      "duration": 5,
      "x": "2.7527%",
      "y": "17.1734%",
      "width": "94.4945%",
      "height": "7.8041%",
      "x_anchor": "0%",
      "y_anchor": "0%",
      "text": "Ornek bir yazi",
      "font_family": "Oswald",
      "font_weight": "700",
      "font_size": "7 vmin",
      "background_color": "#1d1d1d",
      "fill_color": "#ffffff",
      "dynamic": true
    },
    {
      "id": "7bb3f818-0ab5-495d-8969-f404583ecd1b",
      "name": "Text-2",
      "type": "text",
      "track": 3,
      "duration": 5,
      "x": "2.7527%",
      "y": "17.1734%",
      "width": "94.4945%",
      "height": "7.8041%",
      "x_anchor": "0%",
      "y_anchor": "0%",
      "text": "Ornek bir yazi",
      "font_family": "Oswald",
      "font_weight": "700",
      "font_size": "7 vmin",
      "background_color": "#1d1d1d",
      "fill_color": "#ffffff",
      "dynamic": true
    },
    {
      "id": "57035e7c-9ed3-4bc0-b6bd-2f7ed61672a4",
      "name": "Text-3",
      "type": "text",
      "track": 3,
      "duration": 5,
      "x": "2.7527%",
      "y": "17.1734%",
      "width": "94.4945%",
      "height": "7.8041%",
      "x_anchor": "0%",
      "y_anchor": "0%",
      "text": "Ornek bir yazi",
      "font_family": "Oswald",
      "font_weight": "700",
      "font_size": "7 vmin",
      "background_color": "#1d1d1d",
      "fill_color": "#ffffff",
      "dynamic": true
    },
    {
      "id": "8b76acc9-0cbb-47e3-a4ce-9cffd8d3fde4",
      "name": "Text-4",
      "type": "text",
      "track": 3,
      "duration": 5,
      "x": "2.7527%",
      "y": "17.1734%",
      "width": "94.4945%",
      "height": "7.8041%",
      "x_anchor": "0%",
      "y_anchor": "0%",
      "text": "Ornek bir yazi",
      "font_family": "Oswald",
      "font_weight": "700",
      "font_size": "7 vmin",
      "background_color": "#1d1d1d",
      "fill_color": "#ffffff",
      "dynamic": true
    },
    {
      "id": "3a6f5044-7b2b-48fc-bbfb-2a1436bdd6c6",
      "name": "Text-5",
      "type": "text",
      "track": 3,
      "duration": 5,
      "x": "2.7527%",
      "y": "17.1734%",
      "width": "94.4945%",
      "height": "7.8041%",
      "x_anchor": "0%",
      "y_anchor": "0%",
      "text": "Ornek bir yazi",
      "font_family": "Oswald",
      "font_weight": "700",
      "font_size": "7 vmin",
      "background_color": "#1d1d1d",
      "fill_color": "#ffffff",
      "dynamic": true
    }
  ]
}
```

Video editorune post istegi atarken kullanilacak body:
```
{
  "template_id":"7d7cdb2a-c604-4c6a-b464-23d6d1ab5d02",
  "modifications":{
    "Audio-1.source":"{{ $json.sound_urls[0] }}",
    "Audio-2.source":"{{ $json.sound_urls[1] }}",
    "Audio-3.source":"{{ $json.sound_urls[2] }}",
    "Audio-4.source":"{{ $json.sound_urls[3] }}",
    "Audio-5.source":"{{ $json.sound_urls[4] }}",

    "Video-1.source":"{{ $json.video_urls[0] }}",
    "Video-2.source":"{{ $json.video_urls[1] }}",
    "Video-3.source":"{{ $json.video_urls[2] }}",
    "Video-4.source":"{{ $json.video_urls[3] }}",
    "Video-5.source":"{{ $json.video_urls[4] }}",

    "Text-1.text":"{{ $json.scene_titles[0] }}",
    "Text-2.text":"{{ $json.scene_titles[1] }}",
    "Text-3.text":"{{ $json.scene_titles[2] }}",
    "Text-4.text":"{{ $json.scene_titles[3] }}",
    "Text-5.text":"{{ $json.scene_titles[4] }}"
  }
}
```
