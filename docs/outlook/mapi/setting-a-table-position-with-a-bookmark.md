---
title: Festlegen einer Tabellen Position mit einer textMarke
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 56ab37f9-5aa6-4e9d-9dc8-b3d95aa19f35
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f0b041cecca92c0ced32631c67c72fcafdab2a16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422460"
---
# <a name="setting-a-table-position-with-a-bookmark"></a>Festlegen einer Tabellen Position mit einer textMarke

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Textmarke ist eine Ressource, die eine bestimmte Position in einer Tabelle angibt. Durch das Festlegen einer Textmarke wird es möglich, zu einem späteren Zeitpunkt zu einer Position zurückzukehren, eine Funktion, die die Leistung von Tabellenoperationen erheblich verbessern kann. MAPI definiert drei Standard Lesezeichen: 
  
|||
|:-----|:-----|
|BOOKMARK_CURRENT  <br/> |Zeigt auf die aktuelle Zeile in einer Tabelle.  <br/> |
|BOOKMARK_BEGINNING  <br/> |Zeigt auf die erste Zeile in einer Tabelle.  <br/> |
|BOOKMARK_END  <br/> |Zeigt auf die letzte Zeile in einer Tabelle.  <br/> |
   
Tabellen Implementierer sind erforderlich, um diese Standard Lesezeichen zu unterstützen und andere zu unterstützen. Da Lesezeichen jedoch Ressourcen sind und Ressourcen begrenzt sind, sollten Bookmark-Benutzer Sie so bald wie möglich freigeben. 
  
 **So legen Sie ein Lesezeichen an der aktuellen Tabellenposition fest**
  
- Rufen Sie [IMAPITable:: CreateBookMark](imapitable-createbookmark.md)auf. Gelegentlich ist nicht genügend Arbeitsspeicher verfügbar, um die neue Textmarke zu **** reservieren, wodurch CreateBookMark den MAPI_E_UNABLE_TO_COMPLETE-Fehlerwert zurückgibt. 
    
 **So geben Sie ein Lesezeichen frei**
  
- Rufen Sie [IMAPITable:: FreeBookmark](imapitable-freebookmark.md)auf.
    
 **So bewegen Sie den Cursor an eine Textmarke**
  
- Rufen Sie [IMAPITable:: SeekRow](imapitable-seekrow.md)auf. **SeekRow** legt einen neuen Wert für die BOOKMARK_CURRENT-Position fest. **SeekRow** kann verwendet werden, um beispielsweise eine Tabelle mit zehn Zeilen von der aktuellen Position aus zu positionieren oder am Anfang zu beginnen. Clients oder Dienstanbieter können nach dem aktuellen, Anfang oder Ende einer Tabelle oder einer anderen Position suchen, die mit einer vordefinierten Textmarke verknüpft ist. Sie können entweder vorwärts oder rückwärts navigieren und den Vorgang auf eine bestimmte Anzahl von Zeilen begrenzen. In der Regel sollten Anrufer nicht mehr als 50 Zeilen mit **SeekRow**suchen; [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) sollte mit einer größeren Anzahl von Zeilen verwendet werden. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

