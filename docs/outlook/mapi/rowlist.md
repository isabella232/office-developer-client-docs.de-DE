---
title: ROWLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWLIST
api_type:
- COM
ms.assetid: ce0be0d5-4962-4d53-828f-c93d1c5aae32
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4cbaf08c58a98be45ad33aebb8f230fb53c234f3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577660"
---
# <a name="rowlist"></a>ROWLIST

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von [ROWENTRY](rowentry.md) -Strukturen, darstellen, Zeilen und die Vorgänge, die für die Zeilen in einer Tabelle über die Schnittstelle [IExchangeModifyTable](iexchangemodifytableiunknown.md) ausgeführt werden. 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a>Elemente

 **cEntries**
  
> Anzahl der Einträge im Array vom **aEntries** Member angegeben. 
    
 **aEntries [MAPI_DIM]**
  
> Array von **ROWENTRY** -Strukturen, enthält die Zeilen und die Vorgänge, die für die Zeilen in der Tabelle ausgeführt werden. 
    
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |Verwendet, um eine Liste der ausgewählten Regeln für nachfolgende **ModifyTable** Aktionen zu erstellen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ROWENTRY](rowentry.md)
  
[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[MAPI-Strukturen](mapi-structures.md)

