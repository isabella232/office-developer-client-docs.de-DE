---
title: Cache für Spitznamen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 2813c102-6778-4443-ab4b-b573f3568705
description: 'Zuletzt geändert: 30, 2013'
ms.openlocfilehash: 841b01ae8dfcf841b0a1d64113ce7258c4c61583
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334517"
---
# <a name="nickname-cache"></a>Cache für Spitznamen

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Microsoft Office Outlook 2007, Microsoft Outlook 2010 und Microsoft Outlook 2013 interagieren mit dem Spitznamen Cache, der auch als "AutoVervollständigen-Stream" bezeichnet wird. In der AutoVervollständigen-Datenquelle speichert Outlook die AutoVervollständigen-Liste, bei der es sich um die Liste der Namen handelt, die in den Bearbeitungsfeldern **an**, **CC**und **Bcc** angezeigt werden, während ein Benutzer eine e-Mail verfaßt. In diesem Thema wird beschrieben, wie Outlook 2007, Outlook 2010 und Outlook 2013 mit dem AutoVervollständigen-Stream interagiert und auch das Binärformat der Datei und die empfohlenen Methoden für die Interaktion mit dem AutoVervollständigen-Stream erörtert. 
  
Für Anwendungen, die mit Outlook 2010 oder Outlook 2013 interagieren, wird der AutoVervollständigen-Stream als MAPI-Eigenschaft gespeichert und kann mithilfe des MAPI-oder des **propertyAccessor** -Objekts der Nachricht geändert werden. Das **propertyAccessor** -Objekt wird im Outlook 2010-oder Outlook 2013-Objektmodell verfügbar gemacht. 
  
Es gibt keine Abhängigkeiten für das Outlook 2007-Objektmodell oder MAPI-APIs. Daher können Anwendungen, die Änderungen am AutoVervollständigen-Stream in Outlook 2007 vornehmen, mit einer beliebigen Programmiersprache geschrieben werden.
  
## <a name="interacting-with-the-autocomplete-stream"></a>Interagieren mit dem Stream "AutoVervollständigen"

Wenn auf eine Nachricht auf die Bearbeitungsfelder **an**, **CC**oder **Bcc** zugegriffen wird, wird der AutoVervollständigen-Stream geladen, und die Liste der Benutzernamen wird angezeigt. Outlook interagiert auf zweierlei Weise mit dem Stream "AutoVervollständigen": 
  
1. Laden des AutoVervollständigen-Streams 
    
2. Speichern von Änderungen an den Daten im AutoVervollständigen-Stream
    
Die Mittel zum Speichern der AutoVervollständigen-Daten unterscheiden sich zwischen Outlook 2007 und Outlook 2010 oder Outlook 2013 wie folgt: 
  
 **Outlook 2007**
  
Für Outlook 2007 wird der Stream AutoVervollständigen in einer Datei mit dem gleichen Namen wie das Profil und eine Erweiterung von. nk2 gespeichert. Wenn beispielsweise das Standardprofil von "Outlook" verwendet wird, wird die Datei als "Outlook. nk2" bezeichnet. Die NK2-Datei wird in%APPDATA%\Microsoft\Outlook. gespeichert. Weitere Informationen zum Alias Cache-Binärdateiformat finden Sie unter [Outlook 2003/2007 NK2-Dateiformat und Entwicklerrichtlinien](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf).
  
 **Outlook 2010 und Outlook 2013**
  
Outlook 2010 oder Outlook 2013 liest den AutoVervollständigen-Stream aus einer Nachricht in der Tabelle zugehörige Inhalte des Posteingangs des Zustellungs Speichers des e-Mail-Kontos. Diese ausgeblendete Nachricht verfügt über eine Nachrichtenklasse und einen Betreff von IPM. Configuration. autocomplete. Der AutoVervollständigen-Stream wird in dieser Nachricht in der PR_ROAMING_BINARYSTREAM-Eigenschaft ([Pidtagroamingbinary (kanonische Eigenschaft](pidtagroamingbinary-canonical-property.md)) gespeichert. Die AutoVervollständigen-Daten können in einer AutoVervollständigen. dat-Datei in%USERPROFILE%\AppData\Local\Microsoft\Outlook\RoamCache. vorübergehend zwischengespeichert werden. Die DAT-Datei ist jedoch nur ein Cache und wird nicht zum Zurückschreiben in den Zustell Speicher verwendet, wenn der Benutzer Outlook 2010 oder Outlook 2013 beendet.
  
## <a name="loading-the-autocomplete-stream"></a>Laden des AutoVervollständigen-Streams

Outlook lädt den AutoVervollständigen-Stream immer dann, wenn ein Element mit Adressierungs Funktionalität initialisiert wird. E-Mail-Adressen werden beispielsweise in einer neuen e-Mail, einer e-Mail-Nachricht, einem Kontaktelement, einer Besprechungsanfrage usw. verwendet. Zum Laden der Daten liest Outlook den gesamten Inhalt des Streams in den Arbeitsspeicher.
  
Bei AutoVervollständigen-Vorgängen interagiert Outlook exklusiv mit dieser in-Memory-Struktur für die Dauer der Prozesslebensdauer von Outlook. exe. Outlook speichert die Struktur nur beim Herunterfahren. Weitere Informationen zu diesem Prozess finden Sie im folgenden Abschnitt "Speichern des AutoVervollständigen-Streams".
  
## <a name="saving-the-autocomplete-stream"></a>Speichern des AutoVervollständigen-Streams

Outlook speichert den AutoVervollständigen-Stream beim Herunterfahren, wenn die AutoVervollständigen-Liste auf eine der folgenden Arten geändert wurde:
  
- Ein neuer Spitzname-Eintrag wird hinzugefügt, indem ein Name aufgelöst, ein Empfänger aus dem Adressbuch-Dialogfeld ausgewählt oder e-Mails an einen Empfänger gesendet werden, der noch nicht in der Liste vorhanden war.
    
- Ein Eintrag wird geändert, indem e-Mails an einen vorhandenen Empfänger in der Liste gesendet werden.
    
- Ein Eintrag wird vom Benutzer über die benutzerOBERFLÄCHE entfernt.
    
- Andere kleinere Szenarien, die für dieses Thema nicht relevant sind.
    
Beim Speichern von Änderungen an den AutoVervollständigen-Daten wird die in-Memory-Struktur wieder in einen AutoVervollständigen- [Stream](autocomplete-stream.md)geschrieben. Bei der Interaktion mit Outlook 2007 wird der Stream in einer lokalen NK2-Datei gespeichert. Bei Outlook 2010 oder Outlook 2013 schreibt der AutoVervollständigen-Stream zurück in die Tabelle zugeordnete Inhalte des Posteingangs des Zustellungs Speichers des e-Mail-Kontos.
  
## <a name="recommendations"></a>Empfehlungen

- Der AutoVervollständigen-Stream wird nicht teilweise geändert. Die unterstützte Interaktion ist bis 1) lesen Sie den gesamten AutoVervollständigen-Stream in den Arbeitsspeicher, 2) ändern Sie die Speicherstruktur, und 3) schreiben Sie den gesamten Datenstrom zurück in die zugehörige Inhaltstabelle des Posteingangs des Zustellungs Speichers des e-Mail-Kontos (für Outlook 2010 oder Outlook 2013) oder an die lokale NK2-Datei (Outlook 2007).
    
- Interagieren Sie nicht mit dem AutoVervollständigen-Stream, während Outlook ausgeführt wird. Wenn Outlook ausgeführt wird, während Sie den Stream ändern, werden Ihre Änderungen wahrscheinlich beim Herunterfahren überschrieben.
    
- Schreiben Sie keine Eigenschaften vom Typ PT_MV_UNICODE und PR_MV_STRING8 in einen AutoVervollständigen-Stream, der von Microsoft Outlook 2003 verwendet werden soll. Diese Eigenschaften werden nur von Outlook 2007, Outlook 2010 und Outlook 2013 verstanden.
    
- Bei der Entwicklung von Code, der mit Outlook 2007 interagiert, empfiehlt es sich, die. NK2-Datei von anderen Prozessen zu sperren, während Sie diese mit standardmäßigen dateisperrungs-APIs lesen und schreiben (beispielsweise **lockfile** in C/C++ und ** FileStream. Lock** in C#). 
    
- Ändern Sie nur die Eigenschaften von Typen, die sich aus dem Zeilensatz des AutoVervollständigen-Streams befinden. Weitere Informationen zu den Eigenschaftentypen AutoVervollständigen und Eigenschaften finden Sie unter [Auto Complete Stream](autocomplete-stream.md).
    
## <a name="see-also"></a>Siehe auch



[AutoVervollständigen-Stream](autocomplete-stream.md)
  
[MAPI-Profile](mapi-profiles.md)


[Outlook 2003/2007 NK2-Datei Format und Entwicklerrichtlinien](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)

