---
title: ROWENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ROWENTRY
api_type:
- COM
ms.assetid: bd6c0d8e-68cc-4d60-9029-13ed81c816cd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7620f62cc67b99e863a6fa7442056e29f470f1e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591283"
---
# <a name="rowentry"></a>ROWENTRY

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Zeile und den Vorgang, der für diese Zeile in einer Tabelle über die [IExchangeModifyTable-Schnittstelle](iexchangemodifytableiunknown.md) ausgeführt wird. 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a>Members

**ulRowFlags**
  
> Einer der folgenden Vorgänge, der für die Daten ausgeführt werden soll: 
    
  - ROW_ADD: Fügen Sie die Daten der Tabelle als neue Zeile hinzu.
      
  - ROW_MODIFY: Ändern Sie diese Zeile in der Tabelle.
      
  - ROW_REMOVE: Entfernen Sie diese Zeile aus der Tabelle.
      
  - ROW_EMPTY: Fügen Sie der Tabelle keine Zeilendaten hinzu. (Die Zeile ist leer.)
    
**cValues**
  
> Die Anzahl der Eigenschaftswerte in **rgPropvals**.
    
**rgPropVals**
  
> Ein Array von [SPropValue-Strukturen,](spropvalue.md) das die Spaltenwerte darstellt, die in die Tabelle eingefügt werden sollen. 
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |Wird verwendet, um eine Liste der ausgewählten Regeln für nachfolgende **ModifyTable-Aktionen** zu erstellen.  <br/> |
   
## <a name="see-also"></a>Siehe auch
  
- [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
- [MAPI-Strukturen](mapi-structures.md)

