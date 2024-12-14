# digital-ocean-cheat-sheet


# Static websites

Ja, **DigitalOcean** bietet ebenfalls Lösungen für deine Anforderungen, insbesondere über ihr **App Platform** oder das klassische **Spaces + CDN** Setup. Hier ist, wie du das mit DigitalOcean umsetzen kannst:

---

### **1. DigitalOcean App Platform**  
- **Was es ist:** Eine Platform-as-a-Service (PaaS) Lösung, ähnlich wie Vercel oder Netlify, die speziell dafür gebaut wurde, einfache Deployments für statische Webseiten und Anwendungen zu ermöglichen.  
- **Vorteile:**  
  - Automatische Skalierung je nach Traffic.
  - Deployment durch einfaches Hochladen oder direkte Integration mit einem Git-Repo (z. B. GitHub, GitLab).  
  - Integriertes CDN für schnelle Auslieferung.  
  - Minimale Konfiguration: Keine Serververwaltung.  
  - SSL-Zertifikate und Custom Domains werden automatisch gehandhabt.  
- **Wie es funktioniert:**  
  1. Logge dich in DigitalOcean ein.  
  2. Gehe auf "App Platform".  
  3. Wähle dein Git-Repo aus oder lade deine Webseite direkt hoch.  
  4. DigitalOcean erstellt automatisch ein Hosting-Setup für deine statische Seite.  
  5. Optional: Konfiguriere eine eigene Domain (kostenloses HTTPS inklusive).  

- **Kosten:**  
  - Es gibt einen **kostenlosen Starter-Plan**, der schon für viele statische Webseiten ausreicht.  
  - Für höhere Skalierung (z. B. Millionen von Besuchern), könntest du auf einen kostenpflichtigen Plan upgraden, der ab $5/Monat startet.  

- **Ideal für:**  
  Eine "set-it-and-forget-it"-Lösung, bei der du dich nicht um die Infrastruktur kümmern willst.

---

### **2. DigitalOcean Spaces + CDN**  
- **Was es ist:**  
  **Spaces** ist DigitalOcean's Object Storage Lösung (vergleichbar mit Amazon S3). In Kombination mit ihrem globalen **CDN** kannst du damit deine statische Webseite weltweit ausliefern.  

- **Vorteile:**  
  - Sehr skalierbar und robust, ideal für hohen Traffic.  
  - Globales CDN sorgt dafür, dass Inhalte schneller ausgeliefert werden.  
  - Kosten sind vorhersehbar (keine großen Überraschungen bei Traffic-Spitzen).  
  - Einfache Einrichtung und keine Serververwaltung notwendig.  

- **Wie es funktioniert:**  
  1. Erstelle ein **Spaces-Bucket** in deinem DigitalOcean-Account.  
  2. Lade deine Webseite-Dateien (HTML, CSS, JS, Bilder) in den Bucket hoch.  
  3. Aktiviere das integrierte CDN mit wenigen Klicks.  
  4. Optional: Richte eine Custom Domain und HTTPS ein.  

- **Kosten:**  
  - **Spaces** startet bei **$5/Monat** für 250 GB Speicher und 1 TB ausgehenden Traffic.  
  - Zusätzlicher Traffic wird mit **$0.01/GB** abgerechnet.  

- **Ideal für:**  
  Wenn du eine Lösung suchst, die langfristig günstiger ist und volle Kontrolle über deine Dateien möchtest.

---

### **3. Droplets mit NGINX (nur für Bastler)**  
- Wenn du trotz allem lieber auf einem klassischen Server arbeiten willst, kannst du auch ein **Droplet** nutzen (DigitalOceans VPS).  
- Kombiniere das mit **NGINX** oder einem ähnlichen Webserver, der statische Dateien blitzschnell ausliefern kann.  
- Dies ist jedoch nicht empfehlenswert, wenn du dich nicht regelmäßig um die Serververwaltung kümmern willst.  

---

### **Fazit für DigitalOcean:**  
Die **App Platform** ist die beste Wahl, wenn du eine einfache und skalierbare Lösung ohne viel Aufwand suchst. Sie ist vergleichbar mit Vercel und Netlify, aber speziell für DigitalOcean-Nutzer optimiert. Wenn du jedoch maximale Kontrolle und Kosteneffizienz möchtest, sind **Spaces + CDN** eine solide Alternative.  

**Top-Empfehlung für dich:** **App Platform** – minimaler Aufwand, maximaler Output. 🚀
