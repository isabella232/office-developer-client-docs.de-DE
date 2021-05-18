---
title: Informationen zu MAPI-URLs für Notification-Based Indizierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cb35f0a-267e-2d85-1701-02d52578a0b8
description: 'Letzte Änderung: 08. November 2011'
ms.openlocfilehash: 5a3e45809f36b71968560a4b239e268addf00474
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422481"
---
# <a name="about-mapi-urls-for-notification-based-indexing"></a>Informationen zu MAPI-URLs für Notification-Based Indizierung

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn ein Speicheranbieter einen Indexer benachrichtigt, dass ein Objekt für die Indizierung bereit ist, generiert er eine MAPI-URL, die das Objekt eindeutig für den MAPI-Protokollhandler identifiziert. MAPI-URLs werden in Unicode codiert und haben das folgende Format: 
  
`Mapi://SID/StoreDisplayName ($HashNumber)/StoreType/FolderNameA/…/FolderNameN/[EntryIDEncoded[/at=AttachIDEncoded:FileName]]`

In der folgenden Tabelle werden die verschiedenen Teile einer typischen URL beschrieben.

|Teil | Beschreibung|
|:----|:-----------|  
|*SID* |Die Sicherheits-ID des aktuellen Benutzers.| 
|*StoreDisplayName* |Eine Zeichenfolge, die den Anzeigenamen des Benutzers in diesem Speicher angibt.|
|*HashNumber* |Ein **DWORD** in hexadezimaler Darstellung, das basierend auf der Speichereintrags-ID oder der Speicherzuordnungssignatur berechnet wird. Dieser Wert wird in der Registrierung gespeichert und später zum Identifizieren des Speichers im MAPI-Protokollhandler verwendet.<br/><br/>Diese Zahl muss so berechnet werden, dass Kollisionen mit anderen Speichern minimiert werden. Den Algorithmus, mit dem Microsoft Outlook die Hashnummer berechnet, finden Sie unter [Algorithm to Calculate the Store Hash Number](algorithm-to-calculate-the-store-hash-number.md).|
|*StoreType* |Eine Zahl, die den Typ des Speichers identifiziert, der das zu indizierte Objekt enthält. Die folgenden Werte sind möglich:<br/>- 0 – Standardspeicher.<br/><br/>- 1 – Stellvertretungsspeicher, der für lokal zwischengespeicherte Stellvertretungselemente verwendet wird.<br/><br/>- 2 – Öffentliche Ordner, die für Favoriten für öffentliche Ordner verwendet werden.<br/><br/>**HINWEIS**: Wenn der Speicher durchforstet wird, anstatt einen Push zu erhalten, ist der verwendete Wert das Zeichen *X*.| 
|*FolderNamea/.../FolderNameN* |Der Pfad vom Stammverzeichnis der IPM_SUBTREE zum Ordner oder der Nachricht. Beispielsweise verfügt eine Nachricht im Ordner **Familie** unter **Posteingang** **über Posteingang/Familie** für diesen Parameter. |
|*EntryIDEncoded* |MAPI-Eintrags-ID für das Element, das als Unicode-Zeichenfolge codiert ist. Informationen dazu, wie bestimmte Sonderzeichen codiert werden, finden Sie im folgenden Abschnitt "Sonderzeichen". Weitere Informationen zum Algorithmus zum Codieren der Eintrags-ID finden Sie unter [Algorithm to Encode Entry IDs and Attachment IDs](algorithm-to-encode-entry-ids-and-attachment-ids.md).<br/><br/>**HINWEIS**: Wenn diese codierte Eintrags-ID als Text angezeigt wird, wird sie in Übereinstimmung mit dem Algorithmus als zufällige Hangulzeichen oder -felder angezeigt, je nach verfügbaren Schriftarten.  |
|*AttachIDEncoded* |Anlagen-ID, die als Unicode-Zeichenfolge codiert ist. Informationen dazu, wie bestimmte Sonderzeichen codiert werden, finden Sie im folgenden Abschnitt "Sonderzeichen". Weitere Informationen zum Algorithmus zum Codieren der Eintrags-ID finden Sie unter [Algorithm to Encode Entry IDs and Attachment IDs](algorithm-to-encode-entry-ids-and-attachment-ids.md).<br/><br/>**HINWEIS**: Wenn diese codierte Eintrags-ID als Text angezeigt wird, wird sie in Übereinstimmung mit dem Algorithmus als zufällige Hangulzeichen oder -felder angezeigt, je nach verfügbaren Schriftarten. |
|*FileName* |Name der Anlagendatei, wie sie in der Nachricht angezeigt wird.|
    
## <a name="examples-of-mapi-urls"></a>Beispiele für MAPI-URLs

Im Folgenden finden Sie einige Beispiele für MAPI-URLs.
  
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
    
## <a name="blob-associated-with-each-mapi-url"></a>Blob, das jeder MAPI-URL zugeordnet ist

Beim Pushen einer MAPI-URL für ein zu indizierungsorientiertes Objekt erstellt ein Speicheranbieter auch ein binary large object (BLOB), das bestimmte Informationen für den MAPI-Protokollhandler enthält. Der Speicheranbieter ordnet diesen BLOB jeder MAPI-URL zu und sendet ihn, wenn er die MAPI-URL an den Indexer schiebt. Das Format des BLOB lautet wie folgt: 
  
```cpp
DWORD  dwVersion
DWORD  dwFlags
ULONG  cbProfileName
WCHAR  wszProfileName
ULONG  cbProviderItemID
WCHAR  wszProviderItemID
```

Der Speicheranbieter muss diese Werte in der angezeigten Reihenfolge in den BLOB schreiben. In der folgenden Tabelle werden die einzelnen Felde des BLOB beschrieben.

|Teil | Beschreibung|
|:----|:-----------|  
|*dwVersion* |Dies ist die Version der gesendeten Daten. Derzeit ist dieser Wert 1.|
|*dwFlags* |Reserviert für zukünftige Verwendung. Derzeit sollte dieser Wert 0 sein.|
|*cbProfileName* |Die Größe des Profilnamens in Bytes. Diese Informationen sind für den MAPI-Protokollhandler hilfreich, um zu wissen, welches Profil beim Indizierungselement verwendet werden soll.|
|*wszProfileName* |Mit Null beendete Unicode-Zeichenfolge, die den Profilnamen enthält.|
|*cbProviderItemID* |Größe der Anbieterelement-ID in Bytes. Der Speicheranbieter sollte nur die Anbieterelement-ID für Ordner senden, um zu verhindern, dass zusätzliche Ordner geöffnet werden, um diese Informationen zu erhalten.|
|*wszProviderItemID* |Mit Null beendete Unicode-Zeichenfolge mit der Anbieterelement-ID, die das Element im Speicher eindeutig identifiziert.|
    
## <a name="see-also"></a>Siehe auch

- [Informationen Notification-Based Store-Indizierung](about-notification-based-store-indexing.md)
- [MAPI-Konstanten](mapi-constants.md)

