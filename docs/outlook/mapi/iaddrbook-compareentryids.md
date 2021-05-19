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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b6abecc298df7a86afff9338752a15615c73b3a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424259"
---
# <a name="iaddrbookcompareentryids"></a>IAddrBook::CompareEntryIDs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Vergleicht zwei Eintragsbezeichner, die zu einem bestimmten Adressbuchanbieter gehören, um zu bestimmen, ob sie auf dasselbe Adressbuchobjekt verweisen. 
  
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
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID1-Parameter_ verweist. 
    
 _lpEntryID1_
  
> [in] Ein Zeiger auf die erste Zutritts-ID, die verglichen werden soll.
    
 _cbEntryID2_
  
> [in] Die Byteanzahl in der Eintrags-ID, auf die der  _lpEntryID2-Parameter_ verweist. 
    
 _lpEntryID2_
  
> [in] Ein Zeiger auf den zweiten Eintragsbezeichner, der verglichen werden soll.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpulResult_
  
> [out] Ein Zeiger auf das Ergebnis des Vergleichs. Der Inhalt von  _lpulResult_ wird auf TRUE festgelegt, wenn sich die beiden Eintragsbezeichner auf dasselbe Objekt beziehen. Andernfalls wird der Inhalt auf FALSE festgelegt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Eine oder beide der mit den  _Parametern lpEntryID1_ oder  _lpEntryID2 übergebenen_ Eintragsbezeichner werden von keinem Adressbuchanbieter erkannt. 
    
## <a name="remarks"></a>Hinweise

Clientanwendungen und Dienstanbieter rufen die **CompareEntryIDs-Methode** auf, um zwei Eintragsbezeichner zu vergleichen, die zu einem einzigen Adressbuchanbieter gehören, um zu bestimmen, ob sie auf dasselbe Objekt verweisen. **CompareEntryIDs** ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner enthalten kann. Diese Situation kann z. B. auftreten, nachdem eine neue Version eines Adressbuchanbieters installiert wurde. 
  
MAPI übergibt diesen Aufruf an den Adressbuchanbieter, der für die Eintragsbezeichner zuständig ist, und ermittelt den entsprechenden Anbieter, indem die [MAPIUID-Struktur](mapiuid.md) in den Eintragsbezeichnern mit der vom Anbieter registrierten **MAPIUID-Struktur** übereinstimmen. 
  
Wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen, legt **CompareEntryIDs** den Inhalt des  _lpulResult-Parameters_ auf TRUE fest. Wenn sie auf verschiedene Objekte verweisen, **legt CompareEntryIDs** den Inhalt auf FALSE fest. In beiden Fällen gibt **CompareEntryIDs** S_OK. Wenn **CompareEntryIDs** einen Fehler zurückgibt, der auftreten kann, wenn kein Adressbuchanbieter eine **MAPIUID-Struktur** registriert hat, die der in den Eintragsbezeichnern entspricht, sollten Clients und Anbieter keine Aktion basierend auf dem Ergebnis des Vergleichs ergreifen. Sie sollten stattdessen den konservativsten Ansatz für die ausgeführte Aktion verwenden. 
  
## <a name="see-also"></a>Siehe auch



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

