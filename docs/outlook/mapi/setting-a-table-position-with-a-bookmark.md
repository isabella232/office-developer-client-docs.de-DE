---
title: Festlegen einer Tabellenposition mit einer Textmarke
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5db558aa984c3a794517ec61bd04434e99efe13a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566703"
---
# <a name="setting-a-table-position-with-a-bookmark"></a>Festlegen einer Tabellenposition mit einer Textmarke

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Textmarke ist eine Ressource, die eine bestimmte Position in einer Tabelle angibt. Das Festlegen eines Lesezeichens ermöglicht es, zu einem späteren Zeitpunkt zu einer Position zurückzukehren, ein Feature, das die Leistung von Tabellenvorgängen erheblich verbessern kann. MAPI definiert drei Standardlesezeichen: 
  
|||
|:-----|:-----|
|BOOKMARK_CURRENT  <br/> |Zeigt auf die aktuelle Zeile in einer Tabelle.  <br/> |
|BOOKMARK_BEGINNING  <br/> |Zeigt auf die erste Zeile in einer Tabelle.  <br/> |
|BOOKMARK_END  <br/> |Zeigt auf die letzte Zeile in einer Tabelle.  <br/> |
   
Tabellen implementierer müssen diese Standardlesezeichen unterstützen und können auch andere unterstützen. Da Lesezeichen jedoch Ressourcen und Ressourcen sind, sollten Lesezeichenbenutzer sie so schnell wie möglich freigeben. 
  
 **So legen Sie eine Textmarke an der aktuellen Tabellenposition fest**
  
- Aufrufen [von IMAPITable::CreateBookmark](imapitable-createbookmark.md). Gelegentlich ist nicht genügend Arbeitsspeicher verfügbar, um die neue Textmarke zuzuweisen, sodass **CreateBookmark** den MAPI_E_UNABLE_TO_COMPLETE Fehlerwert zurückgibt. 
    
 **So geben Sie ein Lesezeichen frei**
  
- Rufen Sie [IMAPITable::FreeBookmark](imapitable-freebookmark.md)auf.
    
 **So verschieben Sie den Cursor an eine Position mit Lesezeichen**
  
- Rufen Sie [IMAPITable::SeekRow](imapitable-seekrow.md)auf. **SeekRow** richtet einen neuen Wert für die BOOKMARK_CURRENT Position ein. **SeekRow** kann z. B. verwendet werden, um eine Tabelle mit zehn Zeilen von der aktuellen Position zu positionieren oder um am Anfang von vorn zu beginnen. Clients oder Dienstanbieter können nach dem aktuellen Anfang oder Ende einer Tabelle oder einer beliebigen anderen Position suchen, die einer vordefinierten Textmarke zugeordnet ist. Sie können sich entweder vorwärts oder rückwärts bewegen und den Vorgang auf eine bestimmte Anzahl von Zeilen beschränken. Aufrufer sollten in der Regel nicht mehr als 50 Zeilen mit **SeekRow** durchsuchen. [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) sollte mit einer größeren Anzahl von Zeilen verwendet werden. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

