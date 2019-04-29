---
title: Bestimmen des Endes einer Tabelle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 28892e2d351b8dc9aa864c9eff52c94bb0f20e8f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420087"
---
# <a name="determining-a-tables-end"></a>Bestimmen des Endes einer Tabelle

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 Eine häufige Fehlermeldung ist, dass das Ende der Tabelle erreicht wurde, wenn: 
  
- [IMAPITable:: QueryRows](imapitable-queryrows.md) wurde in einer Schleife aufgerufen, wobei das Ende der Schleife durch die von [IMAPITable:: GetRowCount](imapitable-getrowcount.md)zurückgegebene Zeilenanzahl bestimmt wird. Die von **GetRowCount** zurückgegebene Anzahl stellt nicht immer die genaue Anzahl der Zeilen in der Tabelle dar. Es handelt sich um eine ungefähre Anzahl. 
    
- **QueryRows** wurde mit einer festen Anzahl von Zeilen aufgerufen, und es werden weniger Zeilen zurückgegeben. Erst wenn **QueryRows** einen Zeilensatz mit einer Zeilenanzahl gleich 0 (null) zurückgibt, dass keine weiteren Zeilen abgerufen werden sollen. 
    
> [!IMPORTANT]
> Ein Anrufer kann nur davon ausgehen, dass der Cursor am Ende der Tabelle für eine positive Zeilenanzahl oder am Anfang der Tabelle für eine negative Zeilenanzahl positioniert ist, wenn der Wert S_OK und null Zeilen zurückgegeben werden. Der Wert MAPI_E_NOT_FOUND wird nie zurückgegeben. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

