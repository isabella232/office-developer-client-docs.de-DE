---
title: HrGetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetOneProp
api_type:
- HeaderDef
ms.assetid: 8d0a381a-e714-4663-9a57-b0e1cdbd6ba7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e5adc7d0c317d8b803645d78227777998d7d241f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347838"
---
# <a name="hrgetoneprop"></a>HrGetOneProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft den Wert einer einzelnen Eigenschaft von einer Eigenschaften Schnittstelle ab, also einer von [IMAPIProp](imapipropiunknown.md)abgeleiteten Schnittstelle. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a>Parameter

 _PMP_
  
> in Zeiger auf die [IMAPIProp](imapipropiunknown.md) -Schnittstelle, von der der Eigenschaftswert abgerufen werden soll. 
    
 _ulPropTag_
  
> in Property-Tag der Eigenschaft, die abgerufen werden soll. 
    
 _ppprop_
  
> Out Zeiger auf einen Zeiger auf die zurückgegebene [SPropValue](spropvalue.md) -Struktur, die den abgerufenen Eigenschaftswert definiert. 
    
## <a name="return-value"></a>Rückgabewert

MAPI_E_NOT_FOUND 
  
> Die angeforderte Eigenschaft ist nicht über die angegebene Schnittstelle verfügbar.
    
## <a name="remarks"></a>Bemerkungen

Im Gegensatz zur [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode gibt die **HrGetOneProp** -Funktion nie eine Warnung zurück. Da nur eine Eigenschaft abgerufen wird, ist Sie entweder erfolgreich oder schlägt fehl. Zum Abrufen mehrerer Eigenschaften ist getProps schneller. **** 
  
Sie können eine einzelne Eigenschaft mit der [HrSetOneProp](hrsetoneprop.md) -Funktion festlegen oder ändern. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |GetMAPIObjectType  <br/> |MFCMAPI verwendet die **HrGetOneProp** -Methode, um den Typ eines Objekts abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

