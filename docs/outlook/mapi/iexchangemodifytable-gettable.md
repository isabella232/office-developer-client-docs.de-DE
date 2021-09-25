---
title: IExchangeModifyTableGetTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IExchangeModifyTable.GetTable
api_type:
- COM
ms.assetid: 97df32c4-07c6-41f1-84e7-c6e87d396e34
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 25a58769e464ec70bf859f09c7947b9861f16133
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561523"
---
# <a name="iexchangemodifytablegettable"></a>IExchangeModifyTable::GetTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Zeiger auf eine Schnittstelle für ein MAPI-Tabellenobjekt zurück.
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert; muss 0 (null) sein.
    
ACLTABLE_FREEBUSY
  
> Legt neue Rechte fest.
    
frightsFreeBusyDetailed
  
> Wenn ACLTABLE_FREEBUSY übergeben wird, wird eine detaillierte Anzeige der neuen Frei/Gebucht-Rechte bereitgestellt.
    
frightsFreeBusySimple
  
> Wenn ACLTABLE_FREEBUSY übergeben wird, wird eine einfache Anzeige der neuen Frei/Gebucht-Rechte bereitgestellt.
    
 _lppTable_
  
> [out] Verweist auf eine [IMAPITable: IUnknown-Schnittstelle,](imapitableiunknown.md) die das Tabellenobjekt enthält. 
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::OnRefreshView  <br/> |MFCMAPI verwendet die **IExchangeModifyTable::GetTable-Methode,** um eine Tabelle mit Regeln abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

