---
title: Informationen zu MAPI-URLs für Notification-Based-Indizierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 9cb35f0a-267e-2d85-1701-02d52578a0b8
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: f51ddada87a68a13322641b21acda317a8ce5442
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588287"
---
# <a name="about-mapi-urls-for-notification-based-indexing"></a>Informationen zu MAPI-URLs für Notification-Based-Indizierung

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn ein Speicheranbieter einen Indexer benachrichtigt, dass ein Objekt für die Indizierung bereit ist, generiert er eine MAPI-URL, die das Objekt eindeutig mit dem MAPI-Protokollhandler identifiziert. MAPI-URLs werden in Unicode codiert und weisen das folgende Format auf: 
  
`Mapi://SID/StoreDisplayName ($HashNumber)/StoreType/FolderNameA/…/FolderNameN/[EntryIDEncoded[/at=AttachIDEncoded:FileName]]`

In der folgenden Tabelle werden die verschiedenen Teile einer typischen URL beschrieben.

|Teil | Beschreibung|
|:----|:-----------|  
|*SID* |Der Sicherheitsbezeichner des aktuellen Benutzers.| 
|*StoreDisplayName* |Eine Zeichenfolge, die den Anzeigenamen des Benutzers in diesem Speicher angibt.|
|*HashNumber* |Ein **DWORD** in hexadezimaler Darstellung, der basierend auf der Speichereintrags-ID oder der Speicherzuordnungssignatur berechnet wird. Dieser Wert wird in der Registrierung gespeichert und später verwendet, um den Speicher im MAPI-Protokollhandler zu identifizieren.<br/><br/>Diese Zahl muss so berechnet werden, dass Konflikte mit anderen Speichern minimiert werden. Den Algorithmus, den Microsoft Outlook zum Berechnen der Hashnummer verwendet, finden Sie unter [Algorithm to Calculate the Store Hash Number](algorithm-to-calculate-the-store-hash-number.md).|
|*StoreType* |Eine Zahl, die den Typ des Speichers angibt, der das zu indizierte Objekt enthält. Die folgenden Werte sind möglich:<br/>- 0 – Standardspeicher.<br/><br/>- 1 – Delegatspeicher, der für lokal zwischengespeicherte Stellvertretungselemente verwendet wird.<br/><br/>- 2 – Öffentliche Ordner, die für Öffentliche Ordner-Favoriten verwendet werden.<br/><br/>**HINWEIS:** Wenn der Speicher durchforstet wird, anstelle von Push, ist der verwendete Wert das Zeichen *X*.| 
|*FolderNamea/.../FolderNameN* |Der Pfad vom Stamm des IPM_SUBTREE zum Ordner oder der Nachricht. Eine Nachricht im Ordner **"Familie"** unter **"Posteingang"** hat z. B. **"Posteingang/Familie"** für diesen Parameter. |
|*EntryIDEncoded* |MAPI-Eintrags-ID für das Element, das als Unicode-Zeichenfolge codiert ist. Im folgenden Abschnitt "Sonderzeichen" finden Sie Informationen dazu, wie bestimmte Sonderzeichen codiert werden. Weitere Informationen zum Algorithmus zum Codieren der Eintrags-ID finden Sie unter [Algorithm to Encode Entry IDs and Attachment IDs](algorithm-to-encode-entry-ids-and-attachment-ids.md).<br/><br/>**HINWEIS:** Wenn sie als Text angezeigt wird, wird diese codierte Eintrags-ID je nach verfügbaren Schriftarten als zufällige Hangul-Zeichen oder -Felder in Übereinstimmung mit dem Algorithmus angezeigt.  |
|*AttachIDEncoded* |Anlagen-ID, die als Unicode-Zeichenfolge codiert ist. Im folgenden Abschnitt "Sonderzeichen" finden Sie Informationen dazu, wie bestimmte Sonderzeichen codiert werden. Weitere Informationen zum Algorithmus zum Codieren der Eintrags-ID finden Sie unter [Algorithm to Encode Entry IDs and Attachment IDs](algorithm-to-encode-entry-ids-and-attachment-ids.md).<br/><br/>**HINWEIS:** Wenn sie als Text angezeigt wird, wird diese codierte Eintrags-ID je nach verfügbaren Schriftarten als zufällige Hangul-Zeichen oder -Felder in Übereinstimmung mit dem Algorithmus angezeigt. |
|*FileName* |Name der Anlagendatei, wie er in der Nachricht angezeigt wird.|
    
## <a name="examples-of-mapi-urls"></a>Beispiele für MAPI-URLs

Es folgen einige Beispiele für MAPI-URLs.
  
- MAPI-URL für einen Ordner: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($be19928f)/2/Office`
    
- MAPI-URL für eine Nachricht: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Calendar/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾걤곂갠가`
    
- MAPI-URL für eine Anlage: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Inbox/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾간곷갦가/at=겅걋각가:somefile.txt`
    
## <a name="special-characters"></a>Sonderzeichen

Bestimmte Zeichen werden codiert, wenn sie in der Nachricht oder Anlage angezeigt werden. Im Folgenden wird gezeigt, welche Zeichen in einer MAPI-URL codiert sind:
  
- % > %25
    
- / > %2F 
    
- \ > %5C 
    
- \* > %2A 
    
- ? > %3F 
    
## <a name="blob-associated-with-each-mapi-url"></a>Jeder MAPI-URL zugeordnetes Blob

Beim Übertragen einer MAPI-URL für ein zu indiziertes Objekt erstellt ein Speicheranbieter auch ein BLOB (Binary Large Object), das bestimmte Informationen für den MAPI-Protokollhandler enthält. Der Speicheranbieter ordnet dieses BLOB jeder MAPI-URL zu und sendet es, wenn die MAPI-URL an den Indexer übertragen wird. Das Format des BLOB lautet wie folgt: 
  
```cpp
DWORD  dwVersion
DWORD  dwFlags
ULONG  cbProfileName
WCHAR  wszProfileName
ULONG  cbProviderItemID
WCHAR  wszProviderItemID
```

Der Speicheranbieter muss diese Werte in der angegebenen Reihenfolge in das BLOB schreiben. In der folgenden Tabelle werden die einzelnen Felder des BLOB beschrieben.

|Teil | Beschreibung|
|:----|:-----------|  
|*konstanteVersion* |Dies ist die Version der gesendeten Daten. Derzeit ist dieser Wert 1.|
|*Dwflags* |Reserviert für zukünftige Verwendung. Derzeit sollte dieser Wert 0 sein.|
|*cbProfileName* |Die Größe des Profilnamens in Bytes. Diese Informationen sind nützlich, damit der MAPI-Protokollhandler weiß, welches Profil beim Indizieren des Elements verwendet werden soll.|
|*wszProfileName* |Unicode-Zeichenfolge mit Null-Termin, die den Profilnamen enthält.|
|*cbProviderItemID* |Größe der Anbieterelement-ID in Bytes. Der Speicheranbieter sollte nur die Anbieterelement-ID für Ordner senden, um zu verhindern, dass zusätzliche Ordner geöffnet werden, um diese Informationen zu erhalten.|
|*wszProviderItemID* |Unicode-Zeichenfolge mit null terminiertem Wert mit der Anbieterelement-ID, die das Element im Speicher eindeutig identifiziert.|
    
## <a name="see-also"></a>Siehe auch

- [Informationen zur Notification-Based Store Indizierung](about-notification-based-store-indexing.md)
- [MAPI-Konstanten](mapi-constants.md)

