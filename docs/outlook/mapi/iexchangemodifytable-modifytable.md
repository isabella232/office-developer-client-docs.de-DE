---
title: IExchangeModifyTableModifyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.ModifyTable
api_type:
- COM
ms.assetid: b9a745cc-260d-4a1c-896e-6a038ab3cfb9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 46bb9b2cc1a4d54807d6929b4e1439b58fb3a531
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350841"
---
# <a name="iexchangemodifytablemodifytable"></a>IExchangeModifyTable::ModifyTable

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Aktualisiert ein MAPI-Tabellenobjekt.
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> in Verwenden Sie einen der folgenden Werte: 
    
0 (Null)
  
> Verwenden Sie den Wert des **ulRowFlags** -Elements der [ROWENTRY](rowentry.md) -Struktur. 
    
ACLTABLE_FREEBUSY
  
> Legt neue Rechte fest.
    
frightsFreeBusyDetailed
  
> Wenn ACLTABLE_FREEBUSY übergeben wird, werden neue frei/gebucht-Rechte ausführlich angezeigt.
    
frightsFreeBusySimple
  
> Wenn ACLTABLE_FREEBUSY übergeben wird, bietet eine einfache Anzeige der neuen frei/gebucht-Rechte.
    
ROWLIST_REPLACE
  
> Ersetzen Sie alle Zeilen in der Tabelle.
    
 _lpMods_
  
> in Verweist auf eine [ROWLIST](rowlist.md) -Struktur, die die Eigenschaften für das Table-Objekt enthält. 
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|RulesDlg. cpp  <br/> |CRulesDlg:: OnModifySelectedItem  <br/> |MFCMAPI verwendet die **IExchangeModifyTable:: Modify** Table-Methode, um eine geänderte Regel zurück in die Tabelle der Regeln zu schreiben.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[ROWENTRY](rowentry.md)
  
[ROWLIST](rowlist.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

