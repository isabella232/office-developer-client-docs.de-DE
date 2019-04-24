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
ms.openlocfilehash: c13b741b1e0ddfd964b9325d736a26dac4bff2af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346298"
---
# <a name="rowlist"></a>ROWLIST

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von [ROWENTRY](rowentry.md) -Strukturen, die Zeilen und die Vorgänge darstellen, die für diese Zeilen in einer Tabelle über die [IExchangeModifyTable](iexchangemodifytableiunknown.md) -Schnittstelle ausgeführt werden. 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a>Elemente

 **Zentriert**
  
> Die Anzahl der Einträge im vom **aEntries** -Element angegebenen Array. 
    
 **aEntries [MAPI_DIM]**
  
> Array von **ROWENTRY** -Strukturen, die die Zeilen und Vorgänge enthalten, die für diese Zeilen in der Tabelle ausgeführt werden. 
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|RulesDlg. cpp  <br/> |CRulesDlg:: getSelectedItems  <br/> |Wird zum Erstellen einer Liste ausgewählter Regeln für nachfolg **** Ende modifyable-Aktionen verwendet.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ROWENTRY](rowentry.md)
  
[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[MAPI-Strukturen](mapi-structures.md)

