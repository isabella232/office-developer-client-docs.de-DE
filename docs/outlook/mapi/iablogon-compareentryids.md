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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 03256f2dec62d0228c4d5456dcd1b60f66b13ad2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791974"
---
# <a name="iablogoncompareentryids"></a>IABLogon::CompareEntryIDs

  
  
**Betrifft**: Outlook 
  
Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie sich auf dasselbe Objekt verweisen.
  
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
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _lpEntryID1_ verwiesen. 
    
 _lpEntryID1_
  
> [in] Ein Zeiger auf die erste Eintrags-ID, die verglichen werden.
    
 _cbEntryID2_
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _lpEntryID2_ verwiesen. 
    
 _lpEntryID2_
  
> [in] Ein Zeiger auf die zweite Eintrags-ID, die verglichen werden.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpulRet_
  
> [out] Ein Zeiger auf das Ergebnis des Vergleichs. True, um anzugeben, dass die zwei-Eintragsbezeichner auf dasselbe Objekt verweisen. andernfalls, FALSE.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Eintragsbezeichner wurden erfolgreich verglichen.
    
MAPI_E_INVALID_ENTRYID 
  
> Eine oder beide der Eintragsbezeichner gehören nicht zu den Adressbuchanbieter.
    
## <a name="remarks"></a>Hinweise

Von adressbuchanbietern implementierte implementieren Sie die **CompareEntryIDs** -Methode zum Vergleichen von zwei Eintragsbezeichner, um zu bestimmen, ob sie sich auf dasselbe Objekt verweisen. 
  
 **CompareEntryIDs** eignet sich, da ein Objekt mehr als eine gültige Eingabe Bezeichner haben kann. Diese Situation kann beispielsweise auftreten, wenn Sie eine kurzfristigen Eintrags-ID mit langfristige Eintrags-ID vergleichen. 
  
Weitere Informationen zum Erstellen von Eintragsbezeichner finden Sie unter [MAPI-Eintragsbezeichner](mapi-entry-identifiers.md).
  
## <a name="see-also"></a>Siehe auch



[IABLogon: IUnknown](iablogoniunknown.md)

