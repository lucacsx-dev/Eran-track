# Multi-Channel Earnings Tracker - PWA

## ✅ Implementato

### 📱 Mobile-Friendly
- **Layout responsive**: Card a colonna singola su mobile
- **Header adattivo**: Si riorganizza verticalmente su schermi piccoli
- **Tab scorrevoli**: Scorrimento orizzontale invece di compressione
- **Tabelle scrollabili**: Scroll orizzontale per tabelle larghe
- **Form responsivi**: Campi al 100% della larghezza su mobile

### 🚀 PWA (Progressive Web App)
- **Manifest**: File `manifest.webmanifest` configurato
- **Icone**: 
  - 192x192 px per dispositivi standard
  - 512x512 px per alta risoluzione
  - 512x512 px maskable per Android
- **Service Worker**: Cache offline degli asset principali
- **Installabile**: L'app può essere installata come app nativa
- **Theme color**: Integrazione con la UI del sistema (#0b1220)
- **iOS Support**: Meta tag Apple per installazione su iOS

## 🧪 Test

### Avvia il server di sviluppo:
```bash
cd /home/luca/Desktop/try
python3 -m http.server 8888
```

### Accedi all'app:
```
http://localhost:8888/Earn.html
```

### Test PWA su Chrome/Edge:
1. Apri DevTools (F12)
2. Vai su **Application** > **Manifest**
3. Verifica che il manifest sia caricato correttamente
4. Vai su **Service Workers** e verifica che sia registrato
5. Cerca l'icona "Installa" nella barra degli indirizzi

### Test PWA su mobile:
1. Apri l'app nel browser mobile
2. **Android Chrome**: Menu > "Aggiungi a schermata Home" o "Installa app"
3. **iOS Safari**: Condividi > "Aggiungi alla schermata Home"

## 📂 File PWA

- `/manifest.webmanifest` - Configurazione PWA
- `/sw.js` - Service Worker per cache offline
- `/icons/` - Icone app (192, 512, 512-maskable)

## 🔧 Funzionalità Offline

Il Service Worker (sw.js) cache automaticamente:
- La pagina principale (Earn.html)
- Il manifest
- Le icone
- Supporto offline di base

I dati sono già persistiti in LocalStorage, quindi funzionano offline automaticamente.

## 📝 Note

- **HTTPS richiesto**: Per produzione, serve HTTPS (localhost va bene per sviluppo)
- **iOS**: Il prompt di installazione non compare automaticamente, l'utente deve aggiungerlo manualmente
- **Update cache**: Incrementa la versione in `sw.js` (CACHE = 'tracker-v2') per forzare il refresh
