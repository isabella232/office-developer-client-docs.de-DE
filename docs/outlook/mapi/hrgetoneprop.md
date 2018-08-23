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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 99b63e7b0b31a603bf372b1d52e83af39784b628
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564157"
---
# <a name="hrgetoneprop"></a>HrGetOneProp

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ruft den Wert einer Eigenschaft von einer Eigenschaft Oberfläche, d. h., eine Schnittstelle abgeleitet [IMAPIProp](imapipropiunknown.md)ab. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a>Parameter

 _PMP_
  
> [in] Zeiger auf die [IMAPIProp](imapipropiunknown.md) -Schnittstelle, die von der Wert der Eigenschaft ist abgerufen werden sollen. 
    
 _ulPropTag_
  
> [in] Eigenschaftentag der Eigenschaft abgerufen werden sollen. 
    
 _ppprop_
  
> [out] Zeiger auf einen Zeiger auf die zurückgegebene [SPropValue](spropvalue.md) -Struktur, die den Wert der abgerufenen-Eigenschaft definiert. 
    
## <a name="return-value"></a>R�ckgabewert

MAPI_E_NOT_FOUND 
  
> Die angeforderte-Eigenschaft ist von der angegebenen Schnittstelle nicht verfügbar.
    
## <a name="remarks"></a>HinwBemerkungeneise

Im Gegensatz zu der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode gibt die **HrGetOneProp** -Funktion nie eine Warnung an. Da es nur eine Eigenschaft abruft, es einfach entweder Erfolg oder Fehler. Zum Abrufen von mehreren Eigenschaften, ist **GetProps** schneller. 
  
Sie können festlegen oder ändern eine einzelne Eigenschaft mit der [HrSetOneProp](hrsetoneprop.md) -Funktion. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetMAPIObjectType  <br/> |MFCMAPI (engl.) wird die **HrGetOneProp** -Methode verwendet, um den Typ eines Objekts abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

