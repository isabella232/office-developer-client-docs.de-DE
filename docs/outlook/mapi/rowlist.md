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
ms.openlocfilehash: c13b741b1e0ddfd964b9325d736a26dac4bff2af
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419184"
---
# <a name="rowlist"></a>ROWLIST

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von [ROWENTRY-Strukturen,](rowentry.md) die Zeilen und die Vorgänge darstellen, die für diese Zeilen in einer Tabelle über die [IExchangeModifyTable-Schnittstelle ausgeführt](iexchangemodifytableiunknown.md) werden. 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a>Elemente

 **cEntries**
  
> Anzahl der Einträge im vom **aEntries-Element angegebenen** Array. 
    
 **aEntries[MAPI_DIM]**
  
> Array von **ROWENTRY-Strukturen,** die die Zeilen und Vorgänge enthält, die für diese Zeilen in der Tabelle ausgeführt werden. 
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |Wird verwendet, um eine Liste ausgewählter Regeln für nachfolgende **ModifyTable-Aktionen zu** erstellen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ROWENTRY](rowentry.md)
  
[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[MAPI-Strukturen](mapi-structures.md)

