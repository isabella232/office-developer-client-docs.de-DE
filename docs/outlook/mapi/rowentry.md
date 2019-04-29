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
  
Enthält eine Zeile und die Operation, die für diese Zeile in einer Tabelle über die [IExchangeModifyTable](iexchangemodifytableiunknown.md) -Schnittstelle ausgeführt wird. 
  
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
  
> Einer der folgenden Vorgänge, die für die Daten ausgeführt werden sollen: 
    
  - ROW_ADD: Fügen Sie die Daten der Tabelle als neue Zeile hinzu.
      
  - ROW_MODIFY: diese Zeile in der Tabelle ändern.
      
  - ROW_REMOVE: diese Zeile aus der Tabelle entfernen.
      
  - ROW_EMPTY: Fügen Sie die Zeilendaten nicht zur Tabelle hinzu. (Die Zeile ist leer.)
    
**cValues**
  
> Die Anzahl der Eigenschaftswerte in **rgPropvals**.
    
**rgPropVals**
  
> Ein Array von [SPropValue](spropvalue.md) -Strukturen, das die Spaltenwerte darstellt, die in die Tabelle eingefügt werden sollen. 
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|RulesDlg. cpp  <br/> |CRulesDlg:: getSelectedItems  <br/> |Wird zum Erstellen einer Liste ausgewählter Regeln für nachfolg **** Ende modifyable-Aktionen verwendet.  <br/> |
   
## <a name="see-also"></a>Siehe auch
  
- [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
- [MAPI-Strukturen](mapi-structures.md)

