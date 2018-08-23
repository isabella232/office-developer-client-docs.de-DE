---
title: Informationen zum asynchronen Tabellenvorgänge
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1c31045e1fc19da63a2d4b61d92b3629afc96a55
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569421"
---
# <a name="about-asynchronous-table-operations"></a>Informationen zum asynchronen Tabellenvorgänge
 
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Die **IMAPITable** -Schnittstelle umfasst drei Methoden, die asynchron arbeiten und drei Methoden zum Steuern einer asynchronen Operation. Die folgende Tabelle enthält die folgenden Methoden: 
  
|**Asynchrone operation**|**Asynchrone Steuerelementmethode**|
|:-----|:-----|
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |[IMAPITable::GetStatus](imapitable-getstatus.md) <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |[IMAPITable::Abort](imapitable-abort.md) <br/> |
|[IMAPITable::SortTable](imapitable-sorttable.md) <br/> |[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) <br/> |
   
**Zum Abrufen von Statusinformationen über den Typ und die aktuelle Vorgang einer Tabelle**
  
- Rufen Sie [IMAPITable::GetStatus](imapitable-getstatus.md). Bei **GetStatus**kann ein Tabelle Benutzer bestimmen, gibt an, ob die Tabelle statische oder dynamische, ist, wenn ein Vorgang noch in Arbeit ist oder abgeschlossen ist, und wenn aus einer abgeschlossenen Vorgangs ein Fehler aufgetreten ist. Beispielsweise wenn ein Client muss einen Sortiervorgang abzubrechen, da es zu lange dauert, kann der Client zunächst Aufrufen **GetStatus** , um festzustellen, ob tatsächlich ein Sortiervorgang zurzeit verarbeitet wird. Der Client kann dann [IMAPITable::Abort](imapitable-abort.md) unterbrochen werden, um aufrufen. 
    
**Um Aktivität anzuhalten, bis eine asynchrone Aufgabe abgeschlossen wurde**
  
- Rufen Sie [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md). Aufrufen von **WaitForCompletion** ermöglicht die Aufgabe ohne Unterbrechung abgeschlossen. 
    
## <a name="see-also"></a>Siehe auch

- [MAPI-Tabellen](mapi-tables.md)

