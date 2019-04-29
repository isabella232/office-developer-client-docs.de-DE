---
title: Informationen zu MAPI-URLs für die Benachrichtigungs basierte Indizierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cb35f0a-267e-2d85-1701-02d52578a0b8
description: 'Zuletzt geändert: 20 November, 2011'
ms.openlocfilehash: 5a3e45809f36b71968560a4b239e268addf00474
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422481"
---
# <a name="about-mapi-urls-for-notification-based-indexing"></a>Informationen zu MAPI-URLs für die Benachrichtigungs basierte Indizierung

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn ein Informationsspeicher Anbieter einen Indexer benachrichtigt, dass ein Objekt für die Indizierung bereit ist, generiert es eine MAPI-URL, die das Objekt eindeutig für den MAPI-Protokoll Handler identifiziert. MAPI-URLs werden in Unicode codiert und weisen das folgende Format auf: 
  
`Mapi://SID/StoreDisplayName ($HashNumber)/StoreType/FolderNameA/…/FolderNameN/[EntryIDEncoded[/at=AttachIDEncoded:FileName]]`

In der folgenden Tabelle werden die verschiedenen Teile einer typischen URL beschrieben.

|Teil | Beschreibung|
|:----|:-----------|  
|*SID* |Die Sicherheits-ID des aktuellen Benutzers.| 
|*StoreDisplayName* |Eine Zeichenfolge, die den Anzeigenamen des Benutzers in diesem Speicher angibt.|
|*HashNumber* |Ein **DWORD** -Wert in Hexadezimaldarstellung, der basierend auf der Speicher EINTRAGS-ID oder der Store-Zuordnungs Signatur berechnet wird. Dieser Wert wird in der Registrierung gespeichert und später zur Identifizierung des Speichers im MAPI-Protokoll Handler verwendet.<br/><br/>Diese Zahl muss so berechnet werden, dass Kollisionen mit anderen speichern minimiert werden. Informationen zum Algorithmus, der von Microsoft Outlook zum Berechnen der hashzahl verwendet wird, finden Sie unter [Algorithm to calculate the Store Hash Number](algorithm-to-calculate-the-store-hash-number.md).|
|*StoreType* |Eine Zahl, die den Typ des Speichers identifiziert, der das zu indizierende Objekt enthält. Die folgenden Werte sind möglich:<br/>-0-Standardspeicher.<br/><br/>-1-Stellvertreter Speicher, verwendet für Stellvertreter Elemente, die lokal zwischengespeichert werden.<br/><br/>-2-Öffentliche Ordner, die für Öffentliche Ordner-Favoriten verwendet werden.<br/><br/>**Hinweis**: Wenn der Informationsspeicher durchforstet und nicht übertragen wird, ist der verwendete Wert das Zeichen*X*.| 
|*FolderNameA/.../FolderNameN* |Der Pfad vom Stamm des IPM_SUBTREE zum Ordner oder zur Nachricht. Eine Nachricht im **Familien** Ordner unter **Posteingang** hat beispielsweise **Posteingang/Familie** für diesen Parameter. |
|*EntryIDEncoded* |MAPI-Eintrags-ID für das Element, das als Unicode-Zeichenfolge codiert ist. Im folgenden Abschnitt "sonderZeichen" finden Sie Informationen zur Codierung bestimmter Sonderzeichen. Weitere Informationen zum Algorithmus zum Codieren der Eintrags-ID finden Sie unter [Algorithmus zum Codieren von Eintrags-IDs und Anlagen-IDs](algorithm-to-encode-entry-ids-and-attachment-ids.md).<br/><br/>**Hinweis**: Wenn Sie als Text angezeigt werden, wird diese codierte EINTRAGS-ID in Abhängigkeit von den verfügbaren Schriftarten als zufällige Hangul-Zeichen oder-Felder angezeigt.  |
|*AttachIDEncoded* |Als Unicode-Zeichenfolge codierte Anlagen-ID. Im folgenden Abschnitt "sonderZeichen" finden Sie Informationen zur Codierung bestimmter Sonderzeichen. Weitere Informationen zum Algorithmus zum Codieren der Eintrags-ID finden Sie unter [Algorithmus zum Codieren von Eintrags-IDs und Anlagen-IDs](algorithm-to-encode-entry-ids-and-attachment-ids.md).<br/><br/>**Hinweis**: Wenn Sie als Text angezeigt werden, wird diese codierte EINTRAGS-ID in Abhängigkeit von den verfügbaren Schriftarten als zufällige Hangul-Zeichen oder-Felder angezeigt. |
|*FileName* |Der Name der Anlagendatei, wie er in der Nachricht angezeigt wird.|
    
## <a name="examples-of-mapi-urls"></a>Beispiele für MAPI-URLs

Im folgenden finden Sie einige Beispiele für MAPI-URLs.
  
- MAPI-URL für einen Ordner: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($be19928f)/2/Office`
    
- MAPI-URL für eine Nachricht: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Calendar/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾걤곂갠가`
    
- MAPI-URL für eine Anlage: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Inbox/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾간곷갦가/at=겅걋각가:somefile.txt`
    
## <a name="special-characters"></a>Sonderzeichen

Bestimmte Zeichen werden codiert, wenn Sie in der Nachricht oder Anlage angezeigt werden. Im folgenden wird gezeigt, welche Zeichen in einer MAPI-URL codiert sind:
  
- % >% 25
    
- />% 2F 
    
- \ >% 5C 
    
- \*>% 2A 
    
- ? >% 3F 
    
## <a name="blob-associated-with-each-mapi-url"></a>Mit jeder MAPI-URL verknüpftes BLOB

Beim Drücken einer MAPI-URL für ein Objekt, das indiziert werden soll, erstellt ein Speicheranbieter auch ein BLOB (Binary Large Object), das bestimmte Informationen für den MAPI-Protokoll Handler enthält. Der Informationsspeicher Anbieter ordnet diesen BLOB jeder MAPI-URL zu und sendet Sie beim Drücken der MAPI-URL an den Indexer. Das Format des BLOBs lautet wie folgt: 
  
```cpp
DWORD  dwVersion
DWORD  dwFlags
ULONG  cbProfileName
WCHAR  wszProfileName
ULONG  cbProviderItemID
WCHAR  wszProviderItemID
```

Der Informationsspeicher Anbieter muss diese Werte in der angegebenen Reihenfolge in das BLOB schreiben. In der folgenden Tabelle werden die einzelnen Felder des BLOBs beschrieben.

|Teil | Beschreibung|
|:----|:-----------|  
|*dwVersion* |Dies ist die Version der Daten, die gesendet werden. Derzeit ist dieser Wert 1.|
|*dwFlags* |Reserviert für zukünftige Verwendung. Derzeit sollte dieser Wert 0 sein.|
|*cbProfileName* |Die Größe des Profilnamens in Byte. Diese Informationen sind nützlich, wenn der MAPI-Protokoll Handler wissen soll, welches Profil beim Indizieren des Elements verwendet werden soll.|
|*wszProfileName* |Mit NULL endende Unicode-Zeichenfolge, die den Profilnamen enthält.|
|*cbProviderItemID* |Die Größe der Anbieter Element-ID in Byte. Der Informationsspeicher Anbieter sollte nur die Anbieter Element-ID für Ordner senden, um zu verhindern, dass zusätzliche Ordner geöffnet werden, um diese Informationen abzurufen.|
|*wszProviderItemID* |Mit NULL terminierte Unicode-Zeichenfolge mit der Anbieter Element-ID, die das Element im Speicher eindeutig identifiziert.|
    
## <a name="see-also"></a>Siehe auch

- [Informationen zu Benachrichtigungs basierter Speicher Indizierung](about-notification-based-store-indexing.md)
- [MAPI-Konstanten](mapi-constants.md)

