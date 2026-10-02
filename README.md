<div align="center">
  <img src="favicon/favicon-96x96.png" width="96" height="96" alt="WhatsApp Formatter">
</div>

# WhatsApp Formatter

Type a Turkish phone number, get a `wa.me` link, open the chat.

**[https://wa.reachdevel.com](https://wa.reachdevel.com)**

> **Scope: Turkish numbers (+90) only.** This is deliberate, not a limitation waiting
> to be patched. It normalises the number shapes Turkish numbers actually arrive in and
> stops there. It does not attempt to format numbers from other countries.

---

## What it does

WhatsApp's `wa.me` links want a number in full international form — country code,
subscriber number, **no `+`**, and **no leading trunk zero**. A number written the way
Turks actually write it (`0555 123 45 67`) is rejected. This formats it for you as you
type.

| You type | You get |
| --- | --- |
| `5551234567` | `+905551234567` |
| `05551234567` | `+905551234567` |
| `905551234567` | `+905551234567` |
| `9005551234567` | `+9005551234567` |

- **Live preview** — the normalised number appears under the field as you type.
- **Input validation** — accepts digits, `+`, `(`, `)` and spaces; nothing else.
- **One tap to chat** — hands off to WhatsApp Web on desktop, or the WhatsApp app on mobile.
- **Installable** — ships a web app manifest, so it can be added to your home screen.

## Privacy

Everything happens in the browser. No number you type is transmitted to a server,
logged, or stored — there is no server. The page is a single static file.

## How it works

Formatting happens locally in JavaScript. On submit, the app redirects to
`https://wa.me/<number>`, which is WhatsApp's own link format, and that opens the chat in
WhatsApp Web or the WhatsApp app depending on the device.

## Tech

Plain HTML, CSS and JavaScript in one file. No build step, no framework, no
dependencies, nothing to install. Works in any modern desktop or mobile browser.

## Contributing

Bug reports are welcome. Please don't send code pull requests — this project is not
open source (see [License](#license)).

## License

**MIT.** See [LICENSE](LICENSE). Note that the [original QBlocker licensing
discussion](https://github.com/reachdevel/qblocker4arm) does not apply here — this is an
original work.

---

## Türkçe

Türk telefon numaralarını uluslararası formata (+90) dönüştüren ve tarayıcınızdan
doğrudan WhatsApp sohbetleri açan basit bir web uygulaması.

### 🌐 Canlı Demo

[https://wa.reachdevel.com](https://wa.reachdevel.com)

> **Kapsam: yalnızca Türk numaraları (+90).** Bu bilinçli bir tercihtir. Türk numaralarının
> gerçekte geldiği biçimleri normalleştirir ve orada durur.

### ✨ Özellikler

- **Otomatik Formatlama**: Türk telefon numaralarını uluslararası formata (+90) dönüştürür
- **Çoklu Giriş Formatları**:
  - 10 haneli numaralar (5551234567) → +905551234567
  - Başında 0 olan 11 haneli (05551234567) → +905551234567
  - 90 ile başlayan 12 haneli (905551234567) → +905551234567
  - 90 ile başlayan 13 haneli (9005551234567) → +9005551234567
- **Giriş Doğrulama**: Sadece rakamlar, +, (), ve boşluklara izin verir
- **Gerçek Zamanlı Önizleme**: Yazarken formatlanmış numarayı görün
- **Doğrudan WhatsApp Entegrasyonu**: Tek tıkla WhatsApp sohbeti açar
- **PWA Desteği**: Ana ekrana eklenebilir

### 🚀 Kullanım

1. Desteklenen herhangi bir formatta telefon numarası girin
2. Formatlanmış numara giriş alanının altında görünür
3. Bu numarayla WhatsApp sohbeti açmak için **Gönder**'e tıklayın

### 📝 Nasıl Çalışır

Uygulama, sohbet açmak için WhatsApp `wa.me` API'sini kullanır. Formatlanmış bir telefon
numarası gönderdiğinizde `https://wa.me/[numara]` adresine yönlendirir ve bu da WhatsApp
Web'i (masaüstü) veya WhatsApp uygulamasını (mobil) açar.

Tüm işlemler tarayıcıda gerçekleşir. Girilen numaralar hiçbir sunucuya
gönderilmez, kaydedilmez veya loglanmaz.

### 💻 Teknoloji

Saf HTML, CSS ve JavaScript. Bağımlılık veya framework gerektirmez. Tek dosyadır;
derleme adımı yoktur.

### 📄 Lisans

**MIT.** Ayrıntılar için [LICENSE](LICENSE) dosyasına bakın.

---

## Trademark notice

WhatsApp is a trademark of WhatsApp LLC. This project is an independent tool and is not
affiliated with, endorsed by, or sponsored by WhatsApp or Meta. It only builds links
that WhatsApp's own `wa.me` scheme already defines.

Part of the [reachdevel](https://github.com/reachdevel) ecosystem —
see [reachdevel.com](https://reachdevel.com).