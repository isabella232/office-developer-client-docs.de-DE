---
title: ROWLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ROWLIST
api_type:
- COM
ms.assetid: ce0be0d5-4962-4d53-828f-c93d1c5aae32
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2b2e5255ef48fa90ce57e8b80d9e0a9214fca3f7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624272"
---
# <a name="rowlist"></a>ROWLIST

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von [ROWENTRY-Strukturen,](rowentry.md) die Zeilen und die Vorgänge darstellen, die für diese Zeilen in einer Tabelle über die [IExchangeModifyTable-Schnittstelle](iexchangemodifytableiunknown.md) ausgeführt werden. 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a>Members

 **cEntries**
  
> Anzahl der Einträge im Array, das durch das **Element aEntries** angegeben wird. 
    
 **aEntries[MAPI_DIM]**
  
> Array von **ROWENTRY-Strukturen,** die die Zeilen und die Vorgänge enthalten, die für diese Zeilen in der Tabelle ausgeführt werden. 
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |Wird verwendet, um eine Liste der ausgewählten Regeln für nachfolgende **ModifyTable-Aktionen** zu erstellen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ROWENTRY](rowentry.md)
  
[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[MAPI-Strukturen](mapi-structures.md)

