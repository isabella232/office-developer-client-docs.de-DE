---
title: Cache für Spitznamen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 2813c102-6778-4443-ab4b-b573f3568705
description: 'Last modified: January 30, 2013'
ms.openlocfilehash: 6c1074086f4aec413c09fdfe3ca8e7b879f083e4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579453"
---
# <a name="nickname-cache"></a>Cache für Spitznamen

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Microsoft Office Outlook 2007 interagieren Microsoft Outlook 2010 und Microsoft Outlook 2013 mit dem Spitznamencache, der auch als "AutoVervollständigen-Datenstrom" bezeichnet wird. Im Stream für automatisches Vervollständigen wird Outlook die AutoVervollständigen-Liste beibehalten. Dabei handelt es sich um die Liste der Namen, die in den Bearbeitungsfeldern **"An",** **"Cc"** und **"Bcc"** angezeigt werden, während ein Benutzer eine E-Mail erstellt. In diesem Thema wird beschrieben, wie Outlook 2007, Outlook 2010 und Outlook 2013 mit dem Stream für automatisches Vervollständigen interagieren und außerdem das Binärformat der Datei und die empfohlenen Möglichkeiten für die Interaktion mit dem Datenstrom für die automatische Vervollständigen erläutert. 
  
Bei Anwendungen, die mit Outlook 2010 oder Outlook 2013 interagieren, wird der Stream für die automatische Vervollständigen als MAPI-Eigenschaft gespeichert und kann mithilfe der MAPI oder des **PropertyAccessor-Objekts** der Nachricht geändert werden. Das **PropertyAccessor-Objekt** wird in den Outlook 2010- oder Outlook 2013-Objektmodellen verfügbar gemacht. 
  
Es gibt keine Abhängigkeiten vom Outlook 2007-Objektmodell oder MAPI-APIs. Daher können Anwendungen, die Änderungen am Stream für automatisches Vervollständigen innerhalb Outlook 2007 vornehmen, mit jeder Programmiersprache geschrieben werden.
  
## <a name="interacting-with-the-autocomplete-stream"></a>Interagieren mit dem Stream für automatisches Vervollständigen

Wenn **in** einer Nachricht auf die An-, **Cc-** oder **Bcc-Bearbeitungsfelder** zugegriffen wird, wird der Stream für die automatische Vervollständigen geladen, und die Liste der Benutzernamen wird angezeigt. Outlook interagiert auf zwei Arten mit dem Stream für automatisches Vervollständigen: 
  
1. Laden des Datenstroms für automatisches Vervollständigen 
    
2. Speichern von Änderungen an den Daten im Stream für automatisches Vervollständigen
    
Die Möglichkeiten zum Speichern der AutoVervollständigen-Daten unterscheiden sich zwischen Outlook 2007 und Outlook 2010 oder Outlook 2013 wie folgt: 
  
 **Outlook 2007**
  
For Outlook 2007, the autocomplete stream is stored in a file with the same name as the profile and an extension of .nk2. Wenn beispielsweise das Standardprofil "outlook" verwendet wird, wird die Datei "outlook.nk2" genannt. Die NK2-Datei wird in %APPDATA%\Microsoft\Outlook gespeichert. Weitere Informationen zum Binärdateiformat für den Spitznamencache finden Sie unter [Outlook 2003/2007 NK2 File Format and Developer Guidelines.](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
  
 **Outlook 2010 und Outlook 2013**
  
Outlook 2010 oder Outlook 2013 liest den Stream für die automatische Vervollständigen aus einer Nachricht in der Tabelle "Zugeordnete Inhalte" des Posteingangs des Übermittlungsspeichers des E-Mail-Kontos. Diese ausgeblendete Nachricht hat eine Nachrichtenklasse und den Betreff von IPM. Configuration.Autocomplete. Der AutoVervollständigen-Datenstrom wird in dieser Nachricht in der PR_ROAMING_BINARYSTREAM-Eigenschaft ([PidTagRoamingBinary (kanonische Eigenschaft)](pidtagroamingbinary-canonical-property.md)gespeichert. Die AutoVervollständigen-Daten können vorübergehend in einer DAT-Datei mit automatischer Vervollständigen zwischengespeichert werden, die sich in %USERPROFILE%\AppData\Local\Microsoft\Outlook\RoamCache befindet. Die DAT-Datei ist jedoch nur ein Cache und wird nicht zum Zurückschreiben in den Übermittlungsspeicher verwendet, wenn der Benutzer Outlook 2010 oder Outlook 2013 beendet wird.
  
## <a name="loading-the-autocomplete-stream"></a>Laden des Stream für automatisches Vervollständigen

Outlook lädt den Datenstrom für automatisches Vervollständigen, sobald ein Element mit Adressierungsfunktionalität initialisiert wird. E-Mail-Adressen werden beispielsweise in einer neuen E-Mail, einer E-Mail-Antwort, einem Kontaktelement, einer Besprechungsanfrage usw. verwendet. Um die Daten zu laden, liest Outlook den gesamten Inhalt des Datenstroms in den Arbeitsspeicher.
  
Bei AutoVervollständigen-Vorgängen interagiert Outlook für die Dauer der outlook.exe Prozesslebensdauer ausschließlich mit dieser Speicherstruktur. Outlook speichert die Struktur nur beim Herunterfahren. Weitere Informationen zu diesem Vorgang finden Sie im folgenden Abschnitt "Speichern des Stream für automatisches Vervollständigen".
  
## <a name="saving-the-autocomplete-stream"></a>Speichern des Stream für automatisches Vervollständigen

Outlook speichert den AutoVervollständigen-Datenstrom beim Herunterfahren, wenn sich die Liste der automatischen Vervollständigen auf eine der folgenden Arten geändert hat:
  
- Ein neuer Spitznameeintrag wird hinzugefügt, indem ein Name aufgelöst, ein Empfänger aus dem Adressbuchdialogfeld ausgewählt oder E-Mails an einen Empfänger gesendet werden, der noch nicht in der Liste enthalten war.
    
- Ein Eintrag wird geändert, indem E-Mails an einen vorhandenen Empfänger in der Liste gesendet werden.
    
- Ein Eintrag wird vom Benutzer über die Benutzeroberfläche entfernt.
    
- Andere kleinere Szenarien, die für dieses Thema nicht relevant sind.
    
Das Speichern von Änderungen an den AutoVervollständigen-Daten umfasst das Zurückschreiben der speicherinternen Struktur in einen Stream für [automatisches Vervollständigen.](autocomplete-stream.md) Bei der Interaktion mit Outlook 2007 wird der Datenstrom in einer lokalen NK2-Datei gespeichert. For Outlook 2010 or Outlook 2013, the autocomplete stream writes back to the Associated Contents table of the Inbox of the Mail account's delivery store.
  
## <a name="recommendations"></a>Empfehlungen

- Ändern Sie den Datenstrom für automatisches Vervollständigen niemals teilweise. Die unterstützte Interaktion besteht darin, 1) den gesamten AutoVervollständigen-Datenstrom in den Speicher zu lesen, 2) die Speicherstruktur zu ändern und 3) den gesamten Datenstrom zurück in die Tabelle "Zugeordnete Inhalte" des Posteingangs des Übermittlungsspeichers des E-Mail-Kontos (für Outlook 2010 oder Outlook 2013) oder in die lokale NK2-Datei (Outlook 2007) zu schreiben.
    
- Interagieren Sie nicht mit dem Stream für automatisches Vervollständigen, während Outlook ausgeführt wird. Wenn Outlook während der Änderung des Datenstroms ausgeführt wird, werden die Änderungen beim Herunterfahren wahrscheinlich überschrieben.
    
- Schreiben Sie keine Eigenschaften vom Typ PT_MV_UNICODE und PR_MV_STRING8 in einen Datenstrom für automatisches Vervollständigen, der von Microsoft Outlook 2003 genutzt werden soll. Diese Eigenschaften werden nur von Outlook 2007, Outlook 2010 und Outlook 2013 verstanden.
    
- Bei der Entwicklung von Code, der mit Outlook 2007 interagiert, empfehlen wir, die NK2-Datei während des Lesens und Schreibens mithilfe standardmäßiger APIs zum Sperren von Dateien zu sperren (z. B. **LockFile** in C/C++ und **FileStream.Lock** in C#). 
    
- Ändern Sie nur die Eigenschaften von Typen, die aus dem Zeilensatz des Datenstroms für automatisches Vervollständigen stammen. Weitere Informationen zu den Eigenschaften und Eigenschaftstypen des AutoVervollständigen-Datenstroms finden Sie unter "Stream für [automatisches Vervollständigen".](autocomplete-stream.md)
    
## <a name="see-also"></a>Siehe auch



[Stream für automatisches Vervollständigen](autocomplete-stream.md)
  
[MAPI-Profile](mapi-profiles.md)


[Outlook 2003/2007 NK2-Dateiformat und Entwicklerrichtlinien](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)

