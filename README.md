# Grundriss Annotator

## 🌐 [**Live Demo starten**](https://michburkhalter.github.io/GrundrissAnnotator/grundriss-annotator) ⚡

*Ein moderner, browser-basierter Annotator für Grundrisse und architektonische Pläne. Mit diesem Tool können Fenster, Heizkörper und Türen in PDF-Dokumenten markiert und nummeriert werden.*

---

## 🚀 Hauptfunktionen

### 📄 PDF-Verwaltung
- **Mehrere PDFs laden**: Gleichzeitiges Laden mehrerer PDF-Dateien
- **Alphabetische Sortierung**: PDFs werden automatisch alphabetisch zusammengefügt
- **Seitenübergreifende Navigation**: Nahtloses Navigieren durch alle Seiten

### 🏷️ Annotationstypen
- **🪟 Fenster (F01, F02, ...)**: Blaue Markierungen für Fenster
- **🔥 Heizkörper (HK01, HK02, ...)**: Rote Markierungen für Heizkörper
- **🚪 Türen (T01, T02, ...)**: Grüne Markierungen für Türen

### 💾 Projektverwaltung
- **Projekt speichern**: Komplettes Projekt inklusive PDF-Dateien als JSON speichern
- **Projekt laden**: Volle Wiederherstellung von gespeicherten Projekten
- **Automatische Nummerierung**: Eindeutige IDs über alle Seiten hinweg

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
2. Klicken Sie auf die gewünschte Position im PDF
3. Annotation wird automatisch nummeriert und hinzugefügt

### Annotationen bearbeiten
- **✥ Verschieben**: Annotationen verschieben
- **✕ Löschen**: Annotationen löschen (automatische Neu-Nummerierung)
- **↩ Rückgängig**: Letzte Aktion rückgängig machen

### Navigation
- **◀▶ Seiten**: Zwischen den Seiten navigieren
- **+− Zoom**: Ansicht vergrößern/verkleinern
- **📍 Legende**: Klicken Sie auf eine Annotation in der Liste, um zur entsprechenden Seite zu springen

### Export
- **📤 PDF exportieren**: Annotiertes PDF mit allen Markierungen exportieren
- **💾 Projekt speichern**: Komplettes Projekt als JSON speichern
- **📂 Projekt laden**: Gespeichertes Projekt wiederherstellen

### Neu-Nummerierung
- **🔢 Neu nummerieren**: Lücken in der Nummerierung automatisch entfernen
- **Automatisch**: Beim Löschen oder Rückgängig-Machen werden IDs automatisch angepasst

## 📋 Dateiformate

### Projektdatei (.json)
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
  "tCount": {...}
}
```

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

### v2.0 (Aktuell)
- **PDF-Integration**: PDFs direkt in Projektdateien gespeichert
- **Mehrfach-PDF**: Unterstützung für mehrere PDFs gleichzeitig
- **Neu-Nummerierung**: Automatische Lückenentfernung in Annotationen

### v1.0 (Legacy)
- **Basisfunktionen**: Grundlegende Annotationen
- **Manueller PDF-Reload**: PDFs mussten neu geladen werden

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
