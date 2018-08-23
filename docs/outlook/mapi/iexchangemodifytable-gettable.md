---
title: IExchangeModifyTableGetTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.GetTable
api_type:
- COM
ms.assetid: 97df32c4-07c6-41f1-84e7-c6e87d396e34
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d28ce67c6b45f3d0b04d645946ea3f4b3a263c48
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578990"
---
# <a name="iexchangemodifytablegettable"></a>IExchangeModifyTable::GetTable

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt einen Zeiger auf eine Schnittstelle für ein MAPI-Table-Objekt zurück.
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. 0 (null) muss sein.
    
ACLTABLE_FREEBUSY
  
> Neue Rechte festgelegt.
    
frightsFreeBusyDetailed
  
> Wenn ACLTABLE_FREEBUSY übergeben wird, bietet eine detaillierte Ansicht der Rechte für neue Frei/Gebucht-Informationen.
    
frightsFreeBusySimple
  
> Wenn ACLTABLE_FREEBUSY übergeben wird, bietet eine einfache Anzeige von Frei/Gebucht-Informationen Rechte für neue.
    
 _lppTable_
  
> [out] Verweist auf eine [IMAPITable: IUnknown](imapitableiunknown.md) Schnittstelle, die das Table-Objekt enthält. 
    
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::OnRefreshView  <br/> |MFCMAPI (engl.) wird die **IExchangeModifyTable::GetTable** -Methode zum Abrufen einer Tabelle der Regeln verwendet.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

