# Grundriss Annotator

## 🌐 [**Live Demo starten**](https://michburkhalter.github.io/GrundrissAnnotator/) ⚡

*Ein moderner, browser-basierter Annotator für Grundrisse und architektonische Pläne. Mit diesem Tool können Fenster, Heizkörper, Türen, Haustechnik und diverse Elemente in PDF-Dokumenten markiert und nummeriert werden.*

---

## 🚀 Hauptfunktionen

### 📄 PDF-Verwaltung
- **Mehrere PDFs laden**: Gleichzeitiges Laden mehrerer PDF-Dateien
- **Alphabetische Sortierung**: PDFs werden automatisch alphabetisch zusammengefügt
- **Seitenübergreifende Navigation**: Nahtloses Navigieren durch alle Seiten
- **Seitenbenennung**: Jede Seite kann individuell benannt werden

### 🏷️ Annotationstypen
- **🪟 Fenster (F01, F02, ...)**: Blaue Markierungen für Fenster
- **🔥 Heizkörper (HK01, HK02, ...)**: Rote Markierungen für Heizkörper
- **🚪 Türen (T01, T02, ...)**: Grüne Markierungen für Türen
- **⚙ Haustechnik (HT01, HT02, ...)**: Orange Markierungen für Haustechnik
- **◆ Diverses (D01, D02, ...)**: Lila Markierungen für diverse Elemente

### 💾 Projektverwaltung
- **Projekt speichern**: Komplettes Projekt inklusive PDF-Dateien speichern
- **Projekt laden**: Volle Wiederherstellung von gespeicherten Projekten
- **Automatische Nummerierung**: Eindeutige IDs über alle Seiten hinweg
- **Datei-Assoziation**: Doppelklick auf .grundrissannotator Dateien öffnet die App

### 📊 Export-Optionen
- **📊 Excel exportieren**: Annotationen als Excel-Datei exportieren
  - Separate Arbeitsblätter pro Annotationstyp
  - Enthält ID, Seite, Seitenname und Koordinaten
- **📤 PDF exportieren**: Annotiertes PDF mit allen Markierungen exportieren

### 📱 PWA-Funktionalität
- **Offline-Nutzung**: App funktioniert auch ohne Internetverbindung
- **Installation**: Als Desktop-App installierbar
- **Automatische Updates**: Immer die neueste Version

### 🎨 Benutzeroberfläche
- **Klickbare Legende**: Annotationen in der Liste direkt ansteuern
- **Hervorhebung**: Temporäre Hervorhebung ausgewählter Annotationen
- **Scrollbare Liste**: Alle Annotationen in einer übersichtlichen Liste

## 🛠️ Bedienung

### PDFs laden
1. Klicken Sie auf **"↑ PDFs laden"**
2. Wählen Sie eine oder mehrere PDF-Dateien aus
3. PDFs werden automatisch alphabetisch sortiert und zusammengefügt

### Annotationen hinzufügen
1. Wählen Sie einen Annotationstyp in der Toolbar:
   - **◻ Fenster**: Fenster markieren
   - **▣ Heizkörper**: Heizkörper markieren
   - **⬡ Tür**: Türen markieren
   - **⚙ Haustechnik**: Haustechnik markieren
   - **◆ Diverses**: Diverse Elemente markieren
2. Klicken Sie auf die gewünschte Position im PDF
3. Annotation wird automatisch nummeriert und hinzugefügt

### Seiten benennen
1. Navigieren Sie zu der gewünschten Seite
2. Geben Sie einen Namen in das "Seitenname" Eingabefeld ein
3. Der Seitenname wird automatisch gespeichert
4. Seitenamen werden in Excel-Exporten und Projektdateien berücksichtigt

### Annotationen bearbeiten
- **✥ Verschieben**: Annotationen verschieben
- **✕ Löschen**: Annotationen löschen (automatische Neu-Nummerierung)
- **↩ Rückgängig**: Letzte Aktion rückgängig machen

### Navigation
- **◀▶ Seiten**: Zwischen den Seiten navigieren
- **+− Zoom**: Ansicht vergrößern/verkleinern
- **📍 Legende**: Klicken Sie auf eine Annotation in der Liste, um zur entsprechenden Seite zu springen

### Export
- **📊 Excel exportieren**: Annotationen als Excel-Datei exportieren
  - Separate Arbeitsblätter für jeden Annotationstyp
  - Enthält ID, Seite, Seitenname, X- und Y-Koordinaten
- **📤 PDF exportieren**: Annotiertes PDF mit allen Markierungen exportieren
- **💾 Projekt speichern**: Komplettes Projekt als .grundrissannotator Datei speichern
- **📂 Projekt laden**: Gespeichertes Projekt wiederherstellen

### Neu-Nummerierung
- **🔢 Neu nummerieren**: Lücken in der Nummerierung automatisch entfernen
- **Automatisch**: Beim Löschen oder Rückgängig-Machen werden IDs automatisch angepasst

## 📋 Dateiformate

### Projektdatei (.grundrissannotator)
```json
{
  "version": "2.0",
  "timestamp": "2026-05-03T...",
  "fileNames": ["plan1", "plan2"],
  "pdfData": ["base64..."],
  "totalPages": 10,
  "currentPage": 3,
  "zoom": 1.25,
  "annotations": {...},
  "fCount": {...},
  "hCount": {...},
  "tCount": {...},
  "htCount": {...},
  "dCount": {...},
  "pageNames": {...}
}
```

### Excel-Export (.xlsx)
- **Format**: Excel-Datei mit mehreren Arbeitsblättern
- **Arbeitsblätter**: Fenster, Heizkörper, Tür, Haustechnik, Diverses
- **Spalten**: ID, Seite, Seitenname, X-Koordinate, Y-Koordinate
- **Dateiname**: `{original}_annotationen.xlsx`

### Exportiertes PDF
- **Format**: Standard PDF mit eingebetteten Annotationen
- **Qualität**: Hochauflösend (2x Zoom für beste Qualität)
- **Dateiname**: `{original}_annotiert.pdf`

## 🎯 Tastenkürzel & Bedienung

### Mausbedienung
- **Linksklick**: Annotation hinzufügen/auswählen
- **Drag & Drop**: Annotationen verschieben (im Verschieben-Modus)
- **Scroll**: Seiten navigieren, in Listen scrollen

### Touch-Unterstützung
- **Touch**: Vollständige Touch-Unterstützung für Tablets
- **Gesten**: Zoomen und navigieren mit Touch-Gesten

## 🔧 Technische Details

### Browser-Kompatibilität
- **Chrome**: Voll unterstützt
- **Firefox**: Voll unterstützt
- **Safari**: Voll unterstützt
- **Edge**: Voll unterstützt

### Abhängigkeiten
- **PDF.js**: PDF-Rendering und -Manipulation
- **jsPDF**: PDF-Erzeugung für den Export
- **SheetJS (XLSX)**: Excel-Export-Funktionalität
- **Vanilla JavaScript**: Keine zusätzlichen Frameworks benötigt

### Leistung
- **Große PDFs**: Optimiert für große Dokumente
- **Memory Management**: Effiziente Speichernutzung
- **Streaming**: Chunked Verarbeitung für große Dateien

## 📝 Anwendungsfälle

### Architekten & Planer
- **Bestandsaufnahme**: Bestehende Elemente dokumentieren
- **Planung**: Neue Elemente im Grundriss markieren
- **Kommunikation**: Klare Kennzeichnung für Bauteams

### Immobilienverwaltung
- **Inventarisierung**: Fenster und Heizkörper erfassen
- **Wartung**: Dokumentation von Wartungsarbeiten
- **Übergabe**: Strukturierte Übergabe an neue Mieter

### Facility Management
- **Dokumentation**: Vollständige Erfassung aller Ausstattung
- **Planung**: Renovierungs- und Modernisierungsplanung
- **Kostenkalkulation**: Mengenermittlung für Angebote

## 🚨 Wichtige Hinweise

### Speicherung
- **Lokal**: Alle Daten werden lokal im Browser gespeichert
- **Kein Server**: Keine Datenübertragung an externe Server
- **Datenschutz**: Vollständige Kontrolle über Ihre Daten

### Kompatibilität
- **PDF-Format**: Standard PDF-Dateien werden unterstützt
- **Größe**: Optimiert für PDFs bis 50MB
- **Qualität**: Beste Ergebnisse mit Vektor-PDFs

## 🔄 Versionierung

### v1.0.2 (Aktuell)
- **🏷️ Neue Annotationstypen**: Haustechnik und Diverses hinzugefügt
- **📊 Excel-Export**: Export von Annotationen als Excel-Datei
- **📝 Seitenbenennung**: Jede Seite kann individuell benannt werden
- **📱 PWA-Verbesserungen**: Network-First Caching und Datei-Assoziation
- **📁 Dateiendung**: Projektdateien verwenden .grundrissannotator Endung

### v1.0.1
- **PWA-Funktionalität**: Progressive Web App mit Offline-Support
- **Service Worker**: Caching für bessere Performance
- **Manifest**: App-Installation möglich

### v1.0.0
- **PDF-Integration**: PDFs direkt in Projektdateien gespeichert
- **Mehrfach-PDF**: Unterstützung für mehrere PDFs gleichzeitig
- **Neu-Nummerierung**: Automatische Lückenentfernung in Annotationen

## 🤝 Unterstützung

### Fehlerbehebung
- **PDF lädt nicht**: Überprüfen Sie Dateiformat und -größe
- **Annotationen nicht sichtbar**: Zoom anpassen oder Seite neu laden
- **Projekt lädt nicht**: JSON-Datei auf Korruption überprüfen

### Tipps & Tricks
- **Strg+Z**: Rückgängig-Funktion nutzen
- **Doppelklick**: Schnelle Navigation in der Legende
- **Auto-Save**: Projekt regelmäßig speichern

## 📄 Lizenz

Dieses Projekt ist unter der **MIT License** lizenziert.

### 📋 Lizenzdetails
- **Erlaubt**: Kommerzielle Nutzung, Modifikation, Verteilung, private Nutzung
- **Erforderlich**: Lizenz- und Copyright-Vermerk beibehalten
- **Verboten**: Haftung übernehmen, Garantieren

### 📄 Lizenztext
Die vollständige Lizenz finden Sie in der [LICENSE](LICENSE) Datei.

### 🎯 Was das für Sie bedeutet
- ✅ **Freie kommerzielle Nutzung**: Perfekt für Unternehmen und Architekturbüros
- ✅ **Anpassung erlaubt**: Tool an spezifische Bedürfnisse anpassen
- ✅ **Keine Einschränkungen**: Volle Funktionalität ohne rechtliche Hürden
- ✅ **Open Source**: Transparenter Code und Community-Beiträge möglich

---

**Grundriss Annotator** - Effiziente Annotation für architektonische Pläne

📧 **Kontakt**: Für Fragen und Anregungen zum Grundriss Annotator
