---
title: ROWENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWENTRY
api_type:
- COM
ms.assetid: bd6c0d8e-68cc-4d60-9029-13ed81c816cd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 243ab1e926171ee66b95cfd8e969cd77e2b31faf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436034"
---
# <a name="rowentry"></a>ROWENTRY

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Zeile und den Vorgang, der für diese Zeile in einer Tabelle über die [IExchangeModifyTable-Schnittstelle ausgeführt](iexchangemodifytableiunknown.md) wird. 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a>Elemente

**ulRowFlags**
  
> Einer der folgenden Vorgänge, die für die Daten ausgeführt werden sollen: 
    
  - ROW_ADD: Fügen Sie der Tabelle die Daten als neue Zeile hinzu.
      
  - ROW_MODIFY: Ändern Sie diese Zeile in der Tabelle.
      
  - ROW_REMOVE: Entfernen Sie diese Zeile aus der Tabelle.
      
  - ROW_EMPTY: Fügen Sie der Tabelle keine Zeilendaten hinzu. (Die Zeile ist leer.)
    
**cValues**
  
> Die Anzahl der Eigenschaftswerte in **rgPropvals**.
    
**rgPropVals**
  
> Ein Array von [SPropValue-Strukturen,](spropvalue.md) die die Spaltenwerte darstellen, die in die Tabelle eingefügt werden sollen. 
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |Wird verwendet, um eine Liste ausgewählter Regeln für nachfolgende **ModifyTable-Aktionen zu** erstellen.  <br/> |
   
## <a name="see-also"></a>Siehe auch
  
- [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
- [MAPI-Strukturen](mapi-structures.md)

