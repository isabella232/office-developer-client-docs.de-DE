---
title: Informationen zu MAPI-URLs für das benachrichtigungsbasierte Indizieren
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cb35f0a-267e-2d85-1701-02d52578a0b8
description: 'Zuletzt geändert: 08 November 2011'
ms.openlocfilehash: 27ad80b9eca8332beeda147a8b2b4204f9f1cd38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791216"
---
# <a name="about-mapi-urls-for-notification-based-indexing"></a>Informationen zu MAPI-URLs für das benachrichtigungsbasierte Indizieren

**Betrifft**: Outlook 
  
Wenn ein Informationsdienst Indexer, den ein Objekt benachrichtigt für die Indizierung bereit ist, generiert er MAPI-URL, die das Objekt, das den MAPI-Protokollhandler eindeutig identifiziert. MAPI-URLs in Unicode codiert sind, und Sie haben das folgende Format: 
  
`Mapi://SID/StoreDisplayName ($HashNumber)/StoreType/FolderNameA/…/FolderNameN/[EntryIDEncoded[/at=AttachIDEncoded:FileName]]`

Die folgende Tabelle beschreibt die verschiedenen Teile der eine URL.

|Teil | Beschreibung|
|:----|:-----------|  
|*SID* |Sicherheits-ID des aktuellen Benutzers.| 
|*Speicheranzeigename* |Eine Zeichenfolge, die den Anzeigenamen des Benutzers auf diesen Speicher angibt.|
|*Hashnummer* |Ein **DWORD-Wert** in hexadezimale Darstellung, der berechnet wird basierend auf den Store-Eintrags-ID oder die Signatur des Store-Zuordnung. Dieser Wert wird in der Registrierung gespeichert und wird zum Identifizieren des Informationsspeichers, in der MAPI-Protokollhandler später verwendet werden.<br/><br/>Diese Nummer muss auf eine Weise berechnet werden, die Konflikte mit anderen speichern minimiert. Der Algorithmus, den Microsoft Outlook wird verwendet, um die Anzahl der Hash zu berechnen, finden Sie unter [Algorithmus für die Anzahl der Store Hash zu berechnen](algorithm-to-calculate-the-store-hash-number.md).|
|*StoreType* |Eine Zahl, die den Typ des Speichers, die das identifiziert zu indizierende Objekt enthält. Die möglichen Werte sind wie folgt:<br/>-0 - Standard-Informationsspeichers.<br/><br/>-1 - Delegaten, verwendeten Speicher für delegierte Elemente lokal zwischengespeichert.<br/><br/>-2 - Öffentliche Ordner, für die Öffentliche Ordner-Favoriten verwendet.<br/><br/>**Hinweis**: Wenn der Store nicht abgelegt durchforstet wird, ist der Wert, der verwendet wird das Zeichen*X*.| 
|*FolderNameA/.../FolderNameN* |Der Pfad vom Stamm des IPM_SUBTREE zu dem Ordner oder Nachricht. Beispielsweise hat eine Nachricht in den Ordner **Familie** unter **Posteingang** **Posteingang-Familie** für diesen Parameter. |
|*EntryIDEncoded* |MAPI-Eintrags-ID für das Element als Unicode-Zeichenfolge codiert. Finden Sie im folgenden Abschnitt "Sonderzeichen" Informationen zu bestimmten Sonderzeichen wie codiert werden. Weitere Informationen zu den Algorithmus zum Codieren der Eintrags-ID finden Sie unter [Algorithmus zum Codieren EntryIDs und Anlage-IDs](algorithm-to-encode-entry-ids-and-attachment-ids.md).<br/><br/>**Hinweis**: bei der Anzeige als Text codiert dieses Eintrags-ID als zufällige Hangul-Zeichen oder Feldern unter Einhaltung der Algorithmus, je nach verfügbaren Schriftarten angezeigt.  |
|*AttachIDEncoded* |Anlagen-ID als Unicode-Zeichenfolge codiert. Finden Sie im folgenden Abschnitt "Sonderzeichen" Informationen zu bestimmten Sonderzeichen wie codiert werden. Weitere Informationen zu den Algorithmus zum Codieren der Eintrags-ID finden Sie unter [Algorithmus zum Codieren EntryIDs und Anlage-IDs](algorithm-to-encode-entry-ids-and-attachment-ids.md).<br/><br/>**Hinweis**: bei der Anzeige als Text codiert dieses Eintrags-ID als zufällige Hangul-Zeichen oder Feldern unter Einhaltung der Algorithmus, je nach verfügbaren Schriftarten angezeigt. |
|*FileName* |Namen der Anlage Datei, die in der Nachricht angezeigt wird.|
    
## <a name="examples-of-mapi-urls"></a>Beispiele für MAPI-URLs

Es folgen einige Beispiele für MAPI-URLs.
  
- MAPI-URL für einen Ordner: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($be19928f)/2/Office`
    
- MAPI-URL für eine Nachricht: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Calendar/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾걤곂갠가`
    
- MAPI-URL für einen Anhang: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Inbox/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾간곷갦가/at=겅걋각가:somefile.txt`
    
## <a name="special-characters"></a>Sonderzeichen

Bestimmte Zeichen sind verschlüsselt, wenn sie in der Nachricht oder Anlage angezeigt werden. Die folgende Abbildung zeigt, welche Zeichen in einem MAPI-URL codiert sind:
  
- % > 25 %
    
- / > % 2f). 
    
- \ > %5 C 
    
- \*> % 2A 
    
- ? > % 3F 
    
## <a name="blob-associated-with-each-mapi-url"></a>Jedes MAPI-URL zugeordnete BLOB

Bei der MAPI-URL für ein Objekt indiziert werden kann, erstellt ein Informationsdienst auch ein binary large Object (BLOB), die bestimmte Informationen für den MAPI-Protokollhandler enthält. Speicheranbieter ordnet diese BLOB jede MAPI-URL und übertragen, wenn die MAPI-URL an die Indizierung pushen. Das Format für den BLOB lautet wie folgt: 
  
```cpp
DWORD  dwVersion
DWORD  dwFlags
ULONG  cbProfileName
WCHAR  wszProfileName
ULONG  cbProviderItemID
WCHAR  wszProviderItemID
```

Speicheranbieter muss diese Werte in den BLOB in der angegebenen Reihenfolge geschrieben werden. Die folgende Tabelle beschreibt die einzelnen Felder des BLOB.

|Teil | Beschreibung|
|:----|:-----------|  
|*dwVersion* |Dies ist die Version der gesendeten Daten. Derzeit ist dieser Wert 1.|
|*dwFlags* |Reserviert für zukünftige Verwendung. Derzeit sollte dieser Wert 0 sein.|
|*cbProfileName* |Die Größe der Profilname in Byte. Diese Informationen sind hilfreich für den MAPI-Protokollhandler wissen, welches Profil verwenden, wenn das Element zu indizieren.|
|*wszProfileName* |NULL terminierte Unicode-Zeichenfolge, die den Namen des Profils enthält.|
|*cbProviderItemID* |Größe der Provider-Element-ID in Byte. Speicheranbieter sollte nur den Anbieter-ID für Ordner, um zu verhindern, zusätzliche Ordnerstruktur, um diese Informationen senden.|
|*wszProviderItemID* |NULL terminierte Unicode-Zeichenfolge mit der Provider-Element-ID, die das Element im Speicher eindeutig identifiziert.|
    
## <a name="see-also"></a>Siehe auch

- [Informationen zum benachrichtigungsbasierten Indizieren von Stores](about-notification-based-store-indexing.md)
- [MAPI-Konstanten](mapi-constants.md)

