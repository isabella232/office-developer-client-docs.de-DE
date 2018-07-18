---
title: IAddrBookCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBookCompareEntryIDs
api_type:
- COM
ms.assetid: 7dabc1d3-5ea4-482f-91a9-9ef3009eddd2
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 807e592cf535ac060fd275075035ae8beb7d6e78
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791984"
---
# <a name="iaddrbookcompareentryids"></a>IAddrBook::CompareEntryIDs

  
  
**Betrifft**: Outlook 
  
Vergleicht zwei Eintragsbezeichner, die gehören zu einer bestimmten Adressbuchanbieter um festzustellen, ob diese auf das gleiche Address Book-Objekt verweisen. 
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
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
    
 _lpulResult_
  
> [out] Ein Zeiger auf das Ergebnis des Vergleichs. Der Inhalt der _LpulResult_ sind auf TRUE festlegen, wenn die zwei-Eintragsbezeichner auf dasselbe Objekt verweisen. Andernfalls werden die Inhalte auf FALSE festgelegt. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Eine oder beide der mit dem Parameter _lpEntryID1_ oder _lpEntryID2_ übergebene Eintrags-IDs werden durch eine beliebige Adressbuchanbieter nicht erkannt. 
    
## <a name="remarks"></a>Bemerkungen

Clientanwendungen und Anbieter aufzurufen **CompareEntryIDs** -Methode zum Vergleichen von zwei Eintragsbezeichner, die gehört zu einer einzelnen Adressbuchanbieter um zu bestimmen, ob sie sich auf dasselbe Objekt verweisen. **CompareEntryIDs** ist hilfreich, da ein Objekt mehr als eine gültige Eingabe Bezeichner haben kann. Dies kann beispielsweise auftreten, wenn eine neue Version des Adressbuch-Dienstanbieter installiert ist. 
  
MAPI übergibt dieser Aufruf der Adressbuchanbieter, die für die Eintragsbezeichner verantwortlich ist bestimmen den entsprechenden Anbieter durch entsprechende [MAPIUID](mapiuid.md) Strukturänderung in der Eintragsbezeichner mit der **MAPIUID** -Struktur registriert, indem die Anbieter. 
  
Wenn die zwei-Eintragsbezeichner auf dasselbe Objekt verweisen möchten, legt **CompareEntryIDs** den Inhalt des Parameters _LpulResult_ auf "true" fest. Wenn sie verschiedene Objekte verweisen möchten, werden die Inhalte von **CompareEntryIDs** auf FALSE festgelegt. In beiden Fällen gibt **CompareEntryIDs** S_OK zurück. **CompareEntryIDs** einen Fehler zurück, die auftreten, wenn kein Adressbuch eine Struktur **MAPIUID** registriert hat, die in der Eintragsbezeichner übereinstimmt, Clients und Anbieter sollte keine Aktion basierend auf das Ergebnis der Vergleich. Sie sollten stattdessen die Aktion den am häufigsten konservativen Ansatz dauern. 
  
## <a name="see-also"></a>Siehe auch



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

