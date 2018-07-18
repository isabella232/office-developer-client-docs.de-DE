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
ms.openlocfilehash: 9e7f24fb4b444f63b6277d1844a7948f5ab0c590
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792053"
---
# <a name="iexchangemodifytablemodifytable"></a>IExchangeModifyTable::ModifyTable

  
  
**Betrifft**: Outlook 
  
Aktualisiert ein MAPI-Table-Objekt.
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Verwenden Sie eine der folgenden Werte: 
    
0 (Null)
  
> Verwenden Sie den Wert des Elements **UlRowFlags** der [ROWENTRY](rowentry.md) Struktur. 
    
ACLTABLE_FREEBUSY
  
> Neue Rechte festgelegt.
    
frightsFreeBusyDetailed
  
> Wenn ACLTABLE_FREEBUSY übergeben wird, bietet eine detaillierte Ansicht der Rechte für neue Frei/Gebucht-Informationen.
    
frightsFreeBusySimple
  
> Wenn ACLTABLE_FREEBUSY übergeben wird, bietet eine einfache Anzeige von Frei/Gebucht-Informationen Rechte für neue.
    
ROWLIST_REPLACE
  
> Ersetzen Sie alle Zeilen in der Tabelle.
    
 _lpMods_
  
> [in] Verweist auf eine [ROWLIST](rowlist.md) -Struktur mit den Eigenschaften für das Table-Objekt. 
    
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::OnModifySelectedItem  <br/> |MFCMAPI (engl.) wird die **IExchangeModifyTable::ModifyTable** -Methode verwendet, um eine geänderte Regel in der Tabelle der Regeln zurückzuschreiben.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[ROWENTRY](rowentry.md)
  
[ROWLIST](rowlist.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

