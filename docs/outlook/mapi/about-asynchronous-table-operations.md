---
title: Informationen zu asynchronen Tabellenvorgängen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8d073144e079b3059e92a32d4031186726ce304b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588315"
---
# <a name="about-asynchronous-table-operations"></a>Informationen zu asynchronen Tabellenvorgängen
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die **IMAPITable-Schnittstelle** enthält drei Methoden, die asynchron ausgeführt werden, und drei Methoden zum Steuern eines asynchronen Vorgangs. In der folgenden Tabelle sind diese Methoden aufgeführt: 
  
|**Asynchroner Vorgang**|**Asynchrone Steuerelementmethode**|
|:-----|:-----|
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |[IMAPITable::GetStatus](imapitable-getstatus.md) <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |[IMAPITable::Abort](imapitable-abort.md) <br/> |
|[IMAPITable::SortTable](imapitable-sorttable.md) <br/> |[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) <br/> |
   
**So rufen Sie Statusinformationen zum Typ einer Tabelle und zum aktuellen Vorgang ab**
  
- Aufrufen [von IMAPITable::GetStatus](imapitable-getstatus.md). Mit **GetStatus** kann ein Tabellenbenutzer bestimmen, ob die Tabelle statisch oder dynamisch ist, ob ein Vorgang ausgeführt oder abgeschlossen wurde und ob ein Fehler aus einem abgeschlossenen Vorgang aufgetreten ist. Wenn ein Client beispielsweise einen Sortiervorgang abbrechen muss, weil er zu viel Zeit in Nimmt, kann der Client zunächst **GetStatus** aufrufen, um festzustellen, ob tatsächlich ein Sortiervorgang derzeit verarbeitet wird. Anschließend kann der Client [IMAPITable::Abort](imapitable-abort.md) aufrufen, um es zu beenden. 
    
**So setzen Sie die Aktivität an, bis eine asynchrone Aufgabe abgeschlossen ist**
  
- Rufen Sie [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)auf. Durch aufrufen von **WaitForCompletion** kann die Aufgabe ohne Unterbrechung abgeschlossen werden. 
    
## <a name="see-also"></a>Siehe auch

- [MAPI-Tabellen](mapi-tables.md)

