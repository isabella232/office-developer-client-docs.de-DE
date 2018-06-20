---
title: ITableDataHrInsertRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrInsertRow
api_type:
- COM
ms.assetid: e5ae37ea-81a5-49c7-9ad0-0bfac518426c
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 29fdbf060576ee9309473fddf8740b06229dae9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792834"
---
# <a name="itabledatahrinsertrow"></a>ITableData::HrInsertRow

  
  
**Betrifft**: Outlook 
  
Eine Tabellenzeile eingefügt. 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a>Parameter

 _uliRow_
  
> [in] Eine sequenzielle Zeilennummer, die eine bestimmte Zeile darstellt. Nach der Zeile, der die Anzahl angibt, wird die neue Zeile platziert werden. Der Parameter _UliRow_ können Zeile Zahlen von 0 bis n enthält, wobei n ist die Gesamtzahl der Zeilen in der Tabelle. Übergeben von n in _UliRow_ fügt die Zeile an das Ende der Tabelle. 
    
 _lpSRow_
  
> [in] Ein Zeiger auf eine [SRow](srow.md) -Struktur, die beschreibt die Zeile eingefügt werden soll. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Zeile wurde erfolgreich eingefügt.
    
MAPI_E_INVALID_PARAMETER 
  
> Eine Zeile, die den gleichen Wert für die Indexspalte verfügt, wie die Zeile bereits eingefügt werden in der Tabelle vorhanden sind.
    
## <a name="remarks"></a>Hinweise

Die **ITableData::HrInsertRow** -Methode fügt eine Zeile in einer Tabelle an einer bestimmten Position. Nach der Zeile, die an der Position, die durch den Parameter _UliRow_ angegeben ist, wird die neue Zeile eingefügt. 
  
Wenn _UliRow_ auf die Anzahl der Zeilen in der Tabelle festgelegt ist, wird die neue Zeile am Ende der Tabelle angefügt. 
  
Die Eigenschaft, die fungiert als Index-Spalte für die Tabelle muss in der **LpProps** Mitglied der [SRow](srow.md) -Struktur, die auf das durch den Parameter _LpSRow_ enthalten sein. Dieser Index-Eigenschaft in der Regel **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) wird verwendet, um die Zeile für zukünftige Wartungsaufgaben eindeutig zu identifizieren.
  
Die Spalten in der Struktur **' srow '** müssen nicht in derselben Reihenfolge wie die Spalten in der Tabelle sein. 
  
Nachdem die Zeile eingefügt wurde, werden Benachrichtigungen an alle Clients oder Dienstanbieter, die eine Ansicht der Tabelle und aufgerufen, die die Tabelle [IMAPITable::Advise](imapitable-advise.md) -Methode zum Registrieren für Benachrichtigungen, gesendet. Wenn die eingefügte Zeile in der Ansicht aufgrund einer Einschränkung nicht enthalten ist, wird keine Benachrichtigung gesendet. 
  
## <a name="see-also"></a>Siehe auch



[' Srow '](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData: IUnknown](itabledataiunknown.md)

