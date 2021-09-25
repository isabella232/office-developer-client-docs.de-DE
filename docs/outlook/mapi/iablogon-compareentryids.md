---
title: IABLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: cb4a38ff-2fdd-40ac-a613-12c3f11a1df9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ca5474e56a1a72124e6d49bc67329994e6eec04f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571920"
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
  
> [in] Ein Zeiger auf den ersten Eintragsbezeichner, der verglichen werden soll.
    
 _cbEntryID2_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID2-Parameter_ verweist. 
    
 _lpEntryID2_
  
> [in] Ein Zeiger auf den zweiten Eintragsbezeichner, der verglichen werden soll.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpulRet_
  
> [out] Ein Zeiger auf das Ergebnis des Vergleichs. TRUE, um anzugeben, dass die beiden Eintragsbezeichner auf dasselbe Objekt verweisen; andernfalls FALSE.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Eintragsbezeichner wurden erfolgreich verglichen.
    
MAPI_E_INVALID_ENTRYID 
  
> Einer oder beide Eintragsbezeichner gehören nicht zum Adressbuchanbieter.
    
## <a name="remarks"></a>HinwBemerkungeneise

Adressbuchanbieter implementieren die **CompareEntryIDs-Methode,** um zwei Eintragsbezeichner zu vergleichen, um zu bestimmen, ob sie auf dasselbe Objekt verweisen. 
  
 **CompareEntryIDs** ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner haben kann. eine solche Situation kann beispielsweise auftreten, wenn Sie einen kurzfristigen Eintragsbezeichner mit einem langfristigen Eintragsbezeichner vergleichen. 
  
Weitere Informationen zum Erstellen von Eintragsbezeichnern finden Sie unter [MAPI-Eintragsbezeichner.](mapi-entry-identifiers.md)
  
## <a name="see-also"></a>Siehe auch



[IABLogon : IUnknown](iablogoniunknown.md)

