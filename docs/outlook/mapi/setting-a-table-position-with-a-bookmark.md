---
title: Festlegen einer Tabellenposition mit einer Textmarke
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d53f15cb439494ae99ff45509ed14c0928756d8f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795510"
---
# <a name="setting-a-table-position-with-a-bookmark"></a>Festlegen einer Tabellenposition mit einer Textmarke

  
  
**Betrifft**: Outlook 
  
Eine Textmarke ist eine Ressource, die einem bestimmten Standort in einer Tabelle angibt. Festlegen einer Textmarke ermöglicht die, die auf eine Position zu einem späteren Zeitpunkt, ein Feature zurückzugeben, die der Tabellenvorgänge die Leistung erheblich verbessert werden kann. MAPI sind drei standard Textmarken definiert: 
  
|||
|:-----|:-----|
|BOOKMARK_CURRENT  <br/> |Verweist auf die aktuelle Zeile in einer Tabelle.  <br/> |
|BOOKMARK_BEGINNING  <br/> |Verweist auf die erste Zeile in einer Tabelle.  <br/> |
|BOOKMARK_END  <br/> |Verweist auf die letzte Zeile in einer Tabelle.  <br/> |
   
Tabelle Implementierer sind erforderlich, um diese standard Textmarken unterstützt und können auch andere Benutzer unterstützen. Jedoch sollten, da Textmarken Ressourcen sind und Ressourcen beschränkt sind, Textmarke Benutzer sie so bald wie möglich frei. 
  
 **So legen Sie eine Textmarke an der aktuellen Position der Tabelle fest**
  
- Rufen Sie [IMAPITable::CreateBookmark](imapitable-createbookmark.md). Gelegentlich wird nicht genügend Speicher zum Zuweisen der neuen Textmarke verursacht **CreateBookmark** zurückzugebenden den Fehlerwert MAPI_E_UNABLE_TO_COMPLETE vorhanden sein. 
    
 **Eine Textmarke frei**
  
- Rufen Sie [IMAPITable::FreeBookmark](imapitable-freebookmark.md).
    
 **So verschieben Sie den Cursor auf eine Position mit einer Textmarke versehenen**
  
- Rufen Sie [IMAPITable::SeekRow](imapitable-seekrow.md). **SeekRow** stellt einen neuen Wert für die Position BOOKMARK_CURRENT her. **SeekRow** kann, beispielsweise, wenn eine zehn Tabellenzeilen von der aktuellen Position anordnen oder neu am Anfang beginnen verwendet werden. Clients oder Dienstanbieter suchen, um die aktuelle beginnen, oder Beenden einer Tabelle oder einer beliebigen anderen Position, die eine vordefinierte Textmarke zugeordnet ist. Sie können auf eine angegebene Anzahl von Zeilen in einer entweder vorwärts oder rückwärts ausgeführt und Grenzwert der Vorgang verschoben. In der Regel sollten Aufrufer über nicht mehr als 50 Zeilen mit **SeekRow**seek; [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) sollte mit einer größeren Anzahl von Zeilen verwendet werden. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

