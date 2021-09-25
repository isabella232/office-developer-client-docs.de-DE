---
title: HrGetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- HrGetOneProp
api_type:
- HeaderDef
ms.assetid: 8d0a381a-e714-4663-9a57-b0e1cdbd6ba7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 84685b6d1cc48861da6202f38628330b5ebd0156
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576170"
---
# <a name="hrgetoneprop"></a>HrGetOneProp

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft den Wert einer einzelnen Eigenschaft von einer Eigenschaftenschnittstelle ab, d. h. einer schnittstelle, die von [IMAPIProp](imapipropiunknown.md)abgeleitet wurde. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
HRESULT HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a>Parameter

 _Pmp_
  
> [in] Zeiger auf die [IMAPIProp-Schnittstelle,](imapipropiunknown.md) von der der Eigenschaftswert abgerufen werden soll. 
    
 _ulPropTag_
  
> [in] Eigenschaftstag der abzurufenden Eigenschaft. 
    
 _ppprop_
  
> [out] Zeiger auf einen Zeiger auf die [zurückgegebene SPropValue-Struktur,](spropvalue.md) die den abgerufenen Eigenschaftswert definiert. 
    
## <a name="return-value"></a>Rückgabewert

MAPI_E_NOT_FOUND 
  
> Die angeforderte Eigenschaft ist in der angegebenen Schnittstelle nicht verfügbar.
    
## <a name="remarks"></a>HinwBemerkungeneise

Im Gegensatz zur [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) gibt die **HrGetOneProp-Funktion** nie eine Warnung zurück. Da nur eine Eigenschaft abgerufen wird, ist sie entweder erfolgreich oder schlägt fehl. Zum Abrufen mehrerer Eigenschaften ist **GetProps** schneller. 
  
Sie können eine einzelne Eigenschaft mit der [HrSetOneProp-Funktion](hrsetoneprop.md) festlegen oder ändern. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetMAPIObjectType  <br/> |MFCMAPI verwendet die **HrGetOneProp-Methode,** um den Typ eines Objekts abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

