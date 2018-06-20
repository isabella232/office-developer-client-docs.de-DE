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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d0427e36d07d1cdc4f88e471f9ca006e737b73f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795410"
---
# <a name="rowlist"></a>ROWLIST

  
  
**Betrifft**: Outlook 
  
Enthält ein Array von [ROWENTRY](rowentry.md) -Strukturen, darstellen, Zeilen und die Vorgänge, die für die Zeilen in einer Tabelle über die Schnittstelle [IExchangeModifyTable](iexchangemodifytableiunknown.md) ausgeführt werden. 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a>Members

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
  
[IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md)


[MAPI-Strukturen](mapi-structures.md)

