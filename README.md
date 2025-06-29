
# ![icon](.github/icon.png) user.js – Fork mit Upstream-Automation und Custom-Mods

**Dieses Projekt ist ein Fork, der automatisch die aktuellen Einstellungen aus [Betterfox](https://github.com/yokoffing/Betterfox) und [arkenfox/user.js](https://github.com/arkenfox/user.js) übernimmt und individuelle Anpassungen ermöglicht.**

---

## 🚀 Konzept

- **Upstream-Sync:**  
  Branches `arkenfox-upstream` und `betterfox-upstream` werden automatisiert aktualisiert.
- **Eigene Anpassungen:**  
  Im Branch `custom-mods` können eigene Einstellungen vorgenommen werden.  
  Diese werden bei jedem Upstream-Update durch einen speziellen **Custom-Mods-Block** in `user.js` geschützt.
- **Haupt-Branch (`main`):**  
  Enthält die produktive Version und die eigene Projektdokumentation (wie diese README.md).  
  Wird nie automatisch von Upstream überschrieben!

---

## 🛠️ Eigene Einstellungen (Custom-Mods-Block)

Trage individuelle Änderungen an `user.js` immer zwischen folgende Marker ein:

```js
// ==BEGIN CUSTOM MODS==
// Eigene user_pref(...) Einstellungen hier!
user_pref("mein.eigener.pref", true);
// ==END CUSTOM MODS==
```

**Hinweis:**  
Alles zwischen diesen Markern bleibt bei jedem automatischen Update erhalten!

---

## 🤖 Automatisierte Updates

Dieses Repo nutzt GitHub Actions, um:

- Die beiden Upstream-Repos regelmäßig zu synchronisieren.
- Nach Updates aus Betterfox die aktuelle `user.js` in den eigenen Custom-Branch (`custom-mods`) zu übernehmen.
- Deine individuellen Einstellungen automatisch zu erhalten.

---

## 📝 Lizenz

Siehe Lizenzhinweise der jeweiligen Upstreams und Ergänzungen in diesem Fork.

---

## 🔗 Links

- [arkenfox/user.js](https://github.com/arkenfox/user.js)
- [yokoffing/Betterfox](https://github.com/yokoffing/Betterfox)
- [mildman1848/user.js (dieses Repo)](https://github.com/mildman1848/user.js)

---

> **Hinweis für Forks & Actions:**  
> Für automatisierte Branch-Übernahmen nutze einen Fine-grained Personal Access Token (PAT) mit „Contents: Read and write“-Rechten (siehe GitHub Actions und README).
