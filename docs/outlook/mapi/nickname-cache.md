---
title: Cache für Spitznamen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2813c102-6778-4443-ab4b-b573f3568705
description: 'Zuletzt geändert: 30 Januar 2013'
ms.openlocfilehash: 841b01ae8dfcf841b0a1d64113ce7258c4c61583
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389260"
---
# <a name="nickname-cache"></a>Cache für Spitznamen

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Microsoft Office Outlook 2007, Microsoft Outlook 2010 und Microsoft Outlook 2013 interagieren mit der Nickname-Cache, auch bekannt als "AutoVervollständigen Datenstroms." Der AutoVervollständigen-Stream ist, in denen Outlook weiterhin auftritt, der AutoVervollständigen-Liste wird die Liste der Namen, die in der **an**, **Cc**, anzeigt und **Bcc** Bearbeitungsfelder während ein Benutzer eine e-Mail-Nachricht erstellt wird. In diesem Thema wird beschrieben, wie Outlook 2007, Outlook 2010 und Outlook 2013 mit dem AutoVervollständigen-Stream interagieren und erörtert das binäre Format der Datei und die empfohlenen Maßnahmen für die Interaktion mit dem AutoVervollständigen-Stream. 
  
Für Anwendungen, die Interaktion mit Outlook 2010 oder Outlook 2013, AutoVervollständigen-Datenstroms wird als MAPI-Eigenschaft gespeichert und kann mithilfe der MAPI oder das **PropertyAccessor** -Objekt der Nachricht geändert werden. Das **PropertyAccessor** -Objekt wird in der Outlook 2010 oder Outlook 2013-Objektmodell verfügbar gemacht. 
  
Es gibt keine Abhängigkeiten auf dem Outlook 2007-Objektmodell oder die MAPI-APIs. Anwendungen, die die AutoVervollständigen-Datenstroms in Outlook 2007 ändern können daher mithilfe einer beliebigen Programmiersprache geschrieben werden.
  
## <a name="interacting-with-the-autocomplete-stream"></a>Interaktion mit dem AutoVervollständigen-Stream

Wenn die Bearbeitungsfelder **an**, **Cc**oder **Bcc** für eine Nachricht zugegriffen werden, der AutoVervollständigen-Stream wird geladen, und die Liste der Benutzernamen wird angezeigt. Outlook interagiert mit dem AutoVervollständigen-Stream auf zwei Arten: 
  
1. Laden den AutoVervollständigen-stream 
    
2. Speichern von Änderungen an den Daten im Datenstrom AutoVervollständigen
    
Die Mittel zur Speicherung der Daten AutoVervollständigen unterscheidet zwischen Outlook 2007 und Outlook 2010 oder Outlook 2013 wie folgt: 
  
 **Outlook 2007**
  
Für Outlook 2007 wird der Stream AutoVervollständigen in einer Datei mit dem gleichen Namen wie das Profil und der Erweiterung nk2 gespeichert. Angenommen, wenn das Standardprofil für "Outlook" verwendet wird, wird die Datei "outlook.nk2" aufgerufen. Die NK2-Datei wird in % APPDATA%\Microsoft\Outlook gespeichert. Weitere Informationen zu der Nickname-Cache-Binärdateiformat finden Sie unter [Outlook 2003/2007 NK2-Dateiformat und Richtlinien für Entwickler](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf).
  
 **Outlook 2010 und Outlook 2013**
  
Outlook 2010 oder Outlook 2013 liest den AutoVervollständigen-Stream aus einer Nachricht in der Tabelle verknüpfte Inhalt des Posteingangs von übermittlungsspeicher der e-Mail-Konto. Diese ausgeblendete Nachricht hat eine Nachrichtenklasse und den Betreff der IPM. Configuration.Autocomplete. Der AutoVervollständigen-Stream wird dieser Nachricht in der PR_ROAMING_BINARYSTREAM-Eigenschaft ([PidTagRoamingBinary kanonische-Eigenschaft](pidtagroamingbinary-canonical-property.md)) gespeichert. Die AutoVervollständigen-Daten können in einer AutoVervollständigen .dat-Datei befindet sich im % USERPROFILE%\AppData\Local\Microsoft\Outlook\RoamCache vorübergehend zwischengespeichert werden sollen. Allerdings werden die .dat-Datei ist nur ein Cache und wird nicht verwendet, um die übermittlungsspeicher Zurückschreiben, wenn der Benutzer Outlook 2010 oder Outlook 2013 beendet.
  
## <a name="loading-the-autocomplete-stream"></a>Laden den AutoVervollständigen-Stream

Outlook lädt den AutoVervollständigen-Datenstrom aus, wenn ein Element mit Adressierung Funktionalität initialisiert wird. Beispielsweise werden e-Mail-Adressen in einer neuen e-Mail-Nachrichten, eine e-Mail-Antwort, ein Kontaktelement, einer Besprechungsanfrage usw. verwendet. Um die Daten zu laden, liest Outlook den Inhalt des Datenstroms in den Arbeitsspeicher.
  
Für AutoVervollständigen-Operationen interagiert Outlook ausschließlich diese Struktur im Speicher für die Dauer der Lebensdauer Prozess outlook.exe. Outlook speichert nur die Struktur auf Herunterfahren. Finden Sie im folgenden Abschnitt "AutoVervollständigen-Stream speichern" Weitere Informationen zu diesem Vorgang.
  
## <a name="saving-the-autocomplete-stream"></a>Speichern den AutoVervollständigen-Stream

Outlook gespeichert AutoVervollständigen-Datenstrom beim Herunterfahren, wenn die AutoVervollständigen-Liste in einem der folgenden Methoden geändert wurde:
  
- Ein neuen Eintrag Spitzname wird über das Auflösen von Namen, einen Empfänger aus dem Adressbuch im Dialogfeld Adresse auswählen oder Senden von Nachrichten an einen Empfänger, der nicht bereits in der Liste wurde hinzugefügt.
    
- Ein Eintrag wird durch Senden von Nachrichten an einen vorhandenen Empfänger in der Liste geändert.
    
- Ein Eintrag wird vom Benutzer über die Benutzeroberfläche entfernt.
    
- Andere kleineren Szenarien in diesem Thema nicht relevant.
    
Speichern von Änderungen an den AutoVervollständigen-Daten umfasst das Zurückschreiben in-Memory-Struktur in einer [AutoVervollständigen-Stream](autocomplete-stream.md). Bei der Interaktion mit Outlook 2007, wird der Stream-Objekt in einer lokalen NK2-Datei gespeichert. Für Outlook 2010 oder Outlook 2013 schreibt der AutoVervollständigen-Stream zurück zur Inhalt verknüpften Tabelle mit den Posteingang des übermittlungsspeicher der e-Mail-Konto.
  
## <a name="recommendations"></a>Empfehlungen

- Nie teilweise Ändern des AutoVervollständigen-Streams. Die unterstützte Interaktion wird (1) lesen Sie den gesamten AutoVervollständigen-Stream in den Arbeitsspeicher, (2) ändern die Struktur Arbeitsspeicher und 3) zurückschreiben dem gesamten Datenstrom entweder der verknüpften Inhaltstabelle im Posteingang des übermittlungsspeicher der e-Mail-Konto (für Outlook 2010 oder Outlook 2013) oder der lokalen NK2-Datei (Outlook 2007).
    
- Interagieren Sie sich nicht mit dem AutoVervollständigen-Stream, während Outlook ausgeführt wird. Falls Outlook ausgeführt wird, während Sie den Stream ändern, wird wahrscheinlich die Änderungen überschrieben, wenn er heruntergefahren.
    
- Nicht Schreibeigenschaften von führen Sie PT_MV_UNICODE und PR_MV_STRING8 in ein AutoVervollständigen-Stream, der von Microsoft Outlook 2003 genutzt werden eingeben. Diese Eigenschaften sind nur von Outlook 2007, Outlook 2010 und Outlook 2013 verstanden.
    
- Beim Entwickeln von Code, der mit Outlook 2007 interagiert, wird empfohlen, dass Sie die NK2-Datei vor Änderung durch andere Prozesse sperren, beim Lesen und Schreiben sperren APIs (beispielsweise **Sperrdatei** in C/C++- und **-Standarddatei FileStream.Lock** in c#). 
    
- Ändern Sie nur die Eigenschaften des Typen, die sich aus der Zeile-Gruppe des Datenstroms AutoVervollständigen. Weitere Informationen über die AutoVervollständigen Stream Eigenschaften und Eigenschaftentypen finden Sie unter [AutoVervollständigen-Stream](autocomplete-stream.md).
    
## <a name="see-also"></a>Siehe auch



[Stream für automatisches Vervollständigen](autocomplete-stream.md)
  
[MAPI-Profile](mapi-profiles.md)


[Outlook 2003/2007 NK2 Dateiformat und Richtlinien für Entwickler](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)

