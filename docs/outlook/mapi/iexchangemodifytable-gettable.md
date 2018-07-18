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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0cf9373c68d533908b857a4d8f1c0e71aa11846f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792065"
---
# <a name="iexchangemodifytablegettable"></a>IExchangeModifyTable::GetTable

  
  
**Betrifft**: Outlook 
  
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

