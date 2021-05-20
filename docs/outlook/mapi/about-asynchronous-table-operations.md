---
title: Informationen zu asynchronen Tabellenvorgängen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 57219d96-bd9e-4e9a-b34a-dd3aad97bfd9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: eebc04e2263b4a2037e167bd464a31d298b84664
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439569"
---
# <a name="about-asynchronous-table-operations"></a>Informationen zu asynchronen Tabellenvorgängen
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die **IMAPITable-Schnittstelle** umfasst drei asynchrone Methoden und drei Methoden zum Steuern eines asynchronen Vorgangs. In der folgenden Tabelle sind diese Methoden aufgeführt: 
  
|**Asynchroner Vorgang**|**Asynchrone Steuerelementmethode**|
|:-----|:-----|
|[IMAPITable::SetColumns](imapitable-setcolumns.md) <br/> |[IMAPITable::GetStatus](imapitable-getstatus.md) <br/> |
|[IMAPITable::Restrict](imapitable-restrict.md) <br/> |[IMAPITable::Abort](imapitable-abort.md) <br/> |
|[IMAPITable::SortTable](imapitable-sorttable.md) <br/> |[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) <br/> |
   
**So rufen Sie Statusinformationen zum Typ und aktuellen Vorgang einer Tabelle ab**
  
- Rufen [Sie IMAPITable::GetStatus auf.](imapitable-getstatus.md) Mit **GetStatus** kann ein Tabellenbenutzer bestimmen, ob die Tabelle statisch oder dynamisch ist, ob ein Vorgang ausgeführt oder abgeschlossen wurde und ob ein Fehler aus einem abgeschlossenen Vorgang aufgetreten ist. Wenn ein Client beispielsweise einen Sortiervorgang abbrechen muss, weil er zu viel Zeit in Sich nimmt, kann der Client **zunächst GetStatus** aufrufen, um zu ermitteln, ob derzeit ein Sortiervorgang verarbeitet wird. Anschließend kann der Client [IMAPITable::Abort aufrufen, um](imapitable-abort.md) ihn zu beenden. 
    
**So anhalten Sie die Aktivität, bis eine asynchrone Aufgabe abgeschlossen ist**
  
- Rufen [Sie IMAPITable::WaitForCompletion auf.](imapitable-waitforcompletion.md) Durch **das Aufrufen von WaitForCompletion** kann die Aufgabe ohne Unterbrechung abgeschlossen werden. 
    
## <a name="see-also"></a>Siehe auch

- [MAPI-Tabellen](mapi-tables.md)

