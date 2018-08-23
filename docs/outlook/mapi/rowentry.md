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
ms.openlocfilehash: fb0bfaba1ca0a0d7d34096b3b0b1db9863207097
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576267"
---
# <a name="rowentry"></a>ROWENTRY

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält eine Zeile und den Vorgang, der für diese Zeile in einer Tabelle über die Schnittstelle [IExchangeModifyTable](iexchangemodifytableiunknown.md) ausgeführt wird. 
  
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
  
> Einer der folgenden Vorgänge in die Daten ausgeführt werden: 
    
  - ROW_ADD: Fügen Sie die Daten als eine neue Zeile der Tabelle.
      
  - ROW_MODIFY: Ändern Sie diese Zeile in der Tabelle.
      
  - ROW_REMOVE: Entfernen Sie diese Zeile aus der Tabelle.
      
  - ROW_EMPTY: Fügen Sie die Zeilendaten nicht auf die Tabelle an. (Die Zeile ist leer).
    
**cValues**
  
> Die Anzahl der Eigenschaftswerte in **RgPropvals**.
    
**rgPropVals**
  
> Ein Array von [SPropValue](spropvalue.md) -Strukturen, die Darstellung der Werte der Spalten in der Tabelle eingefügt werden soll. 
    
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |Verwendet, um eine Liste der ausgewählten Regeln für nachfolgende **ModifyTable** Aktionen zu erstellen.  <br/> |
   
## <a name="see-also"></a>Siehe auch
  
- [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
- [MAPI-Strukturen](mapi-structures.md)

