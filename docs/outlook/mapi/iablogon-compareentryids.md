---
title: IABLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: cb4a38ff-2fdd-40ac-a613-12c3f11a1df9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 48ddb5a7c4e013c03138b08d9dadcdc0991faeec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438372"
---
# <a name="iablogoncompareentryids"></a>IABLogon::CompareEntryIDs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie auf dasselbe Objekt verweisen.
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulRet
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID1_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID1-Parameter_ verweist. 
    
 _lpEntryID1_
  
> [in] Ein Zeiger auf die erste Zutritts-ID, die verglichen werden soll.
    
 _cbEntryID2_
  
> [in] Die Byteanzahl in der Eintrags-ID, auf die der  _lpEntryID2-Parameter_ verweist. 
    
 _lpEntryID2_
  
> [in] Ein Zeiger auf den zweiten Eintragsbezeichner, der verglichen werden soll.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpulRet_
  
> [out] Ein Zeiger auf das Ergebnis des Vergleichs. TRUE, um anzugeben, dass sich die beiden Eintragsbezeichner auf dasselbe Objekt beziehen. Andernfalls FALSE.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Eintragsbezeichner wurden erfolgreich verglichen.
    
MAPI_E_INVALID_ENTRYID 
  
> Eine oder beide eintragsbezeichner gehören nicht zum Adressbuchanbieter.
    
## <a name="remarks"></a>Hinweise

Adressbuchanbieter implementieren die **CompareEntryIDs-Methode,** um zwei Eintragsbezeichner zu vergleichen, um festzustellen, ob sie auf dasselbe Objekt verweisen. 
  
 **CompareEntryIDs** ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner enthalten kann. Eine solche Situation kann beispielsweise auftreten, wenn Sie eine kurzfristige Eintrags-ID mit einer langfristigen Eintrags-ID vergleichen. 
  
Weitere Informationen zum Erstellen von Eintragsbezeichnern finden Sie unter [MAPI Entry Identifiers](mapi-entry-identifiers.md).
  
## <a name="see-also"></a>Siehe auch



[IABLogon : IUnknown](iablogoniunknown.md)

