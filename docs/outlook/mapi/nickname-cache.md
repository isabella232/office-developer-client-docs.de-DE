---
title: Cache für Spitznamen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2813c102-6778-4443-ab4b-b573f3568705
description: 'Letzte Änderung: 30. Januar 2013'
ms.openlocfilehash: 841b01ae8dfcf841b0a1d64113ce7258c4c61583
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334517"
---
# <a name="nickname-cache"></a>Cache für Spitznamen

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Microsoft Office Outlook 2007 können Microsoft Outlook 2010 und Microsoft Outlook 2013 mit dem Spitznamencache interagieren, der auch als "Automatischer Vervollständigungsstream" bezeichnet wird. Im Datenstrom für die automatische Vervollständigung bleibt Outlook die Liste der automatischen Vervollständigungen erhalten. Dabei handelt es sich um die Liste der Namen, die in den Bearbeitungsfeldern **An,** **Cc** und **Bcc** angezeigt werden, während ein Benutzer eine E-Mail verfassen. In diesem Thema wird beschrieben, wie Outlook 2007, Outlook 2010 und Outlook 2013 mit dem Datenstrom für die automatische Vervollständigung interagieren. Außerdem werden das Binärformat der Datei und die empfohlenen Möglichkeiten für die Interaktion mit dem Datenstrom für die automatische Vervollständigung erläutert. 
  
Für Anwendungen, die mit Outlook 2010 oder Outlook 2013 interagieren, wird der Datenstrom für die automatische Vervollständigung als MAPI-Eigenschaft gespeichert und kann mithilfe der MAPI oder des **PropertyAccessor-Objekts** der Nachricht geändert werden. Das **PropertyAccessor-Objekt** wird in den Outlook 2010- oder Outlook 2013-Objektmodellen verfügbar gemacht. 
  
Es gibt keine Abhängigkeiten von Outlook 2007-Objektmodell oder MAPI-APIs. Daher können Anwendungen, die Änderungen am Datenstrom für die automatische Vervollständigung innerhalb von Outlook 2007 vornehmen, mit einer beliebigen Programmiersprache geschrieben werden.
  
## <a name="interacting-with-the-autocomplete-stream"></a>Interagieren mit dem AutoComplete Stream

Wenn auf die Bearbeitungsfelder **An**, **Cc** oder **Bcc** in einer Nachricht zugegriffen wird, wird der Datenstrom für die automatische Vervollständigung geladen und die Liste der Benutzernamen angezeigt. Outlook interaktion mit dem Datenstrom für die automatische Vervollständigung auf zwei Arten: 
  
1. Laden des Automatischen Vervollständigungsstreams 
    
2. Speichern von Änderungen an den Daten im Datenstrom für die automatische Vervollständigung
    
Die Mittel zum Speichern der AutoComplete-Daten unterscheiden sich zwischen Outlook 2007 und Outlook 2010 oder Outlook 2013 wie folgt: 
  
 **Outlook 2007**
  
Für Outlook 2007 wird der Datenstrom für die automatische Vervollständigung in einer Datei mit demselben Namen wie das Profil und einer Erweiterung von .nk2 gespeichert. Wenn beispielsweise das Standardprofil von "outlook" verwendet wird, wird die Datei als "outlook.nk2" bezeichnet. Die Datei .nk2 wird in %APPDATA%\Microsoft\Outlook. Weitere Informationen zum Binärdateiformat für den Spitznamencache finden Sie [unter Outlook 2003/2007 NK2 File Format and Developer Guidelines](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf).
  
 **Outlook 2010 und Outlook 2013**
  
Outlook 2010 oder Outlook 2013 liest den Autocomplete-Stream aus einer Nachricht in der Tabelle Zugeordnete Inhalte des Posteingangs des Zustellungsspeichers des E-Mail-Kontos. Diese ausgeblendete Nachricht verfügt über eine Nachrichtenklasse und einen Betreff IPM.ConfigUration. AutoComplete. Der Datenstrom für die automatische Vervollständigung wird in dieser Nachricht in der PR_ROAMING_BINARYSTREAM -Eigenschaft ([PidTagRoamingBinary Canonical Property](pidtagroamingbinary-canonical-property.md)) gespeichert. Die Daten für die automatische Vervollständigung werden möglicherweise vorübergehend in einer datei für die automatische Vervollständigung zwischengespeichert, die sich in %USERPROFILE%\AppData\Local\Microsoft\Outlook\RoamCache befindet. Die DAT-Datei ist jedoch nur ein Cache und wird nicht zum Zurückschreiben in den Übermittlungsspeicher verwendet, wenn der Benutzer Outlook 2010 oder Outlook 2013 beendet.
  
## <a name="loading-the-autocomplete-stream"></a>Laden des Automatischen Vervollständigungsstreams

Outlook lädt den Datenstrom für die automatische Vervollständigung, wenn ein Element mit Adressierungsfunktionalität initialisiert wird. Beispielsweise werden E-Mail-Adressen in einer neuen E-Mail, einer E-Mail-Antwort, einem Kontaktelement, einer Besprechungsanfrage und so weiter verwendet. Zum Laden der Daten liest Outlook alle Inhalte des Datenstroms in den Arbeitsspeicher.
  
Bei AutoComplete-Vorgängen interagiert Outlook ausschließlich mit dieser Speicherstruktur für die Dauer der outlook.exe Prozesslebensdauer. Outlook speichert die Struktur nur beim Herunterfahren. Weitere Informationen zu diesem Prozess finden Sie im folgenden Abschnitt "Speichern des Automatischen Vervollständigungsstreams".
  
## <a name="saving-the-autocomplete-stream"></a>Speichern des Automatischen Vervollständigungsstreams

Outlook speichert den Datenstrom für die automatische Vervollständigung beim Herunterfahren, wenn sich die Liste der automatischen Vervollständigung auf eine der folgenden Arten geändert hat:
  
- Ein neuer Spitznameneintrag wird durch Auflösen eines Namens, Auswählen eines Empfängers aus dem Adressbuchdialogfeld oder Senden von E-Mails an einen Empfänger hinzugefügt, der noch nicht in der Liste enthalten war.
    
- Ein Eintrag wird durch Senden von E-Mails an einen vorhandenen Empfänger in der Liste geändert.
    
- Ein Eintrag wird vom Benutzer über die Benutzeroberfläche entfernt.
    
- Andere kleinere Szenarien, die für dieses Thema nicht relevant sind.
    
Das Speichern von Änderungen an den AutoComplete-Daten umfasst das Zurückschreiben der Speicherstruktur in einen [AutoComplete Stream .](autocomplete-stream.md) Bei der Interaktion mit Outlook 2007 wird der Datenstrom in einer lokalen nk2-Datei gespeichert. Für Outlook 2010 oder Outlook 2013 schreibt der Datenstrom für die automatische Vervollständigung in die Tabelle Zugeordnete Inhalte des Posteingangs des Zustellungsspeichers des E-Mail-Kontos zurück.
  
## <a name="recommendations"></a>Empfehlungen

- Ändern Sie den Datenstrom für die automatische Vervollständigung nie teilweise. Die unterstützte Interaktion besteht in 1) Lesen des gesamten Datenstroms für die automatische Vervollständigung in den Arbeitsspeicher, 2) Ändern der Speicherstruktur und 3) Zurückschreiben des gesamten Datenstroms in die Tabelle Zugeordnete Inhalte des Posteingangs des E-Mail-Übermittlungsspeichers (für Outlook 2010 oder Outlook 2013) oder in die lokale nk2-Datei (Outlook 2007).
    
- Interagieren Sie nicht mit dem Automatischen Vervollständigungsstream, Outlook ausgeführt wird. Wenn Outlook während des Änderns des Datenstroms ausgeführt wird, werden die Änderungen beim Herunterfahren wahrscheinlich überschrieben.
    
- Schreiben Sie keine Eigenschaften vom Typ PT_MV_UNICODE und PR_MV_STRING8 in einen Automatischvervollständigungsstream, der von Microsoft Outlook 2003 verwendet werden soll. Diese Eigenschaften werden nur von Outlook 2007, Outlook 2010 und Outlook 2013 verstanden.
    
- Bei der Entwicklung von Code, der mit Outlook 2007 interagiert, wird empfohlen, die nk2-Datei vor Änderungen durch andere Prozesse zu sperren, während Sie sie mithilfe von standardmäßigen Dateisperren-APIs lesen und schreiben (z. B. **LockFile** in C/C++ und **FileStream.Lock** in C#). 
    
- Ändern Sie nur die Eigenschaften von Typen, die sich aus dem Zeilensatz des Datenstroms für die automatische Vervollständigung befinden. Weitere Informationen zu den Eigenschaften und Eigenschaftentypen des Automatischen Vervollständigungsstreams finden Sie unter [AutoComplete Stream](autocomplete-stream.md).
    
## <a name="see-also"></a>Siehe auch



[Autocomplete Stream](autocomplete-stream.md)
  
[MAPI-Profile](mapi-profiles.md)


[Outlook NK2 File Format and Developer Guidelines 2003/2007](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)

