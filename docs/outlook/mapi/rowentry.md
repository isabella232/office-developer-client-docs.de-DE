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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f8ac73b1977886208290285fec2d1bd0de1b4f92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795412"
---
# <a name="rowentry"></a>ROWENTRY

**Betrifft**: Outlook 
  
Enthält eine Zeile und den Vorgang, der für diese Zeile in einer Tabelle über die Schnittstelle [IExchangeModifyTable](iexchangemodifytableiunknown.md) ausgeführt wird. 
  
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
  
- [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md)
- [MAPI-Strukturen](mapi-structures.md)

