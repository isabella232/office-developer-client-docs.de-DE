---
title: Festlegen einer Tabellenposition mit einem Lesezeichen
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
# <a name="setting-a-table-position-with-a-bookmark"></a>Festlegen einer Tabellenposition mit einem Lesezeichen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Textmarke ist eine Ressource, die einen bestimmten Speicherort in einer Tabelle angibt. Das Festlegen einer Textmarke ermöglicht es, zu einem späteren Zeitpunkt an eine Position zurückzukehren, ein Feature, das die Leistung von Tabellenvorgängen erheblich verbessern kann. MAPI definiert drei Standardmarken: 
  
|||
|:-----|:-----|
|BOOKMARK_CURRENT  <br/> |Zeigt auf die aktuelle Zeile in einer Tabelle.  <br/> |
|BOOKMARK_BEGINNING  <br/> |Zeigt auf die erste Zeile in einer Tabelle.  <br/> |
|BOOKMARK_END  <br/> |Zeigt auf die letzte Zeile in einer Tabelle.  <br/> |
   
Tabellen implementierer sind erforderlich, um diese Standardmarken zu unterstützen und können auch andere unterstützen. Da Lesezeichen jedoch Ressourcen sind und Ressourcen begrenzt sind, sollten Lesezeichenbenutzer sie so bald wie möglich frei geben. 
  
 **So legen Sie eine Textmarke an der aktuellen Tabellenposition**
  
- Rufen [Sie IMAPITable::CreateBookmark auf.](imapitable-createbookmark.md) Gelegentlich ist nicht genügend Arbeitsspeicher verfügbar, um die neue Textmarke zuzuordnen, wodurch **CreateBookmark** den Fehlerwert MAPI_E_UNABLE_TO_COMPLETE zurück. 
    
 **So können Sie ein Lesezeichen frei**
  
- Rufen [Sie IMAPITable::FreeBookmark auf.](imapitable-freebookmark.md)
    
 **So verschieben Sie den Cursor an eine Position mit Textmarken**
  
- Rufen [Sie IMAPITable::SeekRow auf.](imapitable-seekrow.md) **SeekRow** richtet einen neuen Wert für die BOOKMARK_CURRENT ein. **SeekRow** kann z. B. verwendet werden, um eine Tabelle zehn Zeilen von der aktuellen Position zu positionieren oder um am Anfang zu beginnen. Clients oder Dienstanbieter können zum aktuellen, Beginnenden oder Ende einer Tabelle oder zu einer beliebigen anderen Position suchen, die einem vordefinierten Lesezeichen zugeordnet ist. Sie können sich vorwärts oder rückwärts bewegen und den Vorgang auf eine angegebene Anzahl von Zeilen beschränken. In der Regel sollten Anrufer mit SeekRow nicht mehr als 50 **Zeilen durchsuchen.** [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) sollte mit einer größeren Anzahl von Zeilen verwendet werden. 
    
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

