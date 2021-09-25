---
title: Bestimmen des Endes einer Tabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 91a79512991cc5ece2b2792cecb2e6d9f90c7c41
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576394"
---
# <a name="determining-a-tables-end"></a>Bestimmen des Endes einer Tabelle

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 Ein häufiger Fehler besteht darin, davon auszugehen, dass das Ende der Tabelle erreicht wurde, wenn: 
  
- [IMAPITable::QueryRows](imapitable-queryrows.md) wurde in einer Schleife aufgerufen, wobei das Ende der Schleife durch die von IMAPITable zurückgegebene Zeilenanzahl bestimmt [wird::GetRowCount](imapitable-getrowcount.md). Die von **GetRowCount** zurückgegebene Anzahl stellt nicht immer die genaue Anzahl von Zeilen in der Tabelle dar. es handelt sich um eine ungefähre Anzahl. 
    
- **QueryRows** wurde mit einer festen Anzahl von Zeilen aufgerufen, und es werden weniger Zeilen zurückgegeben. Erst wenn **QueryRows** einen Zeilensatz mit einer Zeilenanzahl gleich Null zurückgibt, gibt es keine weiteren abzurufenden Zeilen. 
    
> [!IMPORTANT]
> Der Aufrufer kann nur dann davon ausgehen, dass der Cursor am Ende der Tabelle für eine positive Zeilenanzahl oder am Anfang der Tabelle für eine negative Zeilenanzahl positioniert wird, wenn der Wert S_OK und Nullzeilen zurückgegeben werden. Der Wert MAPI_E_NOT_FOUND wird nie zurückgegeben. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

