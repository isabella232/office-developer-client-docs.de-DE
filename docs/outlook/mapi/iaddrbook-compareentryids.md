---
title: IAddrBookCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBookCompareEntryIDs
api_type:
- COM
ms.assetid: 7dabc1d3-5ea4-482f-91a9-9ef3009eddd2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 773391c12d6100482d27c7bf023e4b75f56c195c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571857"
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
  
> [in] Ein Zeiger auf den ersten Eintragsbezeichner, der verglichen werden soll.
    
 _cbEntryID2_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID2-Parameter_ verweist. 
    
 _lpEntryID2_
  
> [in] Ein Zeiger auf den zweiten Eintragsbezeichner, der verglichen werden soll.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpulResult_
  
> [out] Ein Zeiger auf das Ergebnis des Vergleichs. Der Inhalt von  _lpulResult_ wird auf TRUE festgelegt, wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen. andernfalls wird der Inhalt auf FALSE festgelegt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Einer oder beide der Eintragsbezeichner, die mit den  _Parametern lpEntryID1_ oder  _lpEntryID2_ übergeben werden, werden von keinem Adressbuchanbieter erkannt. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Clientanwendungen und Dienstanbieter rufen die **CompareEntryIDs-Methode** auf, um zwei Eintragsbezeichner zu vergleichen, die zu einem einzelnen Adressbuchanbieter gehören, um zu bestimmen, ob sie auf dasselbe Objekt verweisen. **CompareEntryIDs** ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner aufweisen kann. Diese Situation kann beispielsweise auftreten, nachdem eine neue Version eines Adressbuchanbieters installiert wurde. 
  
Die MAPI übergibt diesen Aufruf an den Adressbuchanbieter, der für die Eintragsbezeichner verantwortlich ist. Dabei wird der entsprechende Anbieter bestimmt, indem die [MAPIUID-Struktur](mapiuid.md) in den Eintragsbezeichnern mit der vom Anbieter registrierten **MAPIUID-Struktur** übereinstimmt. 
  
Wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen, legt **CompareEntryIDs** den Inhalt des  _lpulResult-Parameters_ auf TRUE fest. wenn sie auf verschiedene Objekte verweisen, legt **CompareEntryIDs** den Inhalt auf FALSE fest. In beiden Fällen gibt **CompareEntryIDs** S_OK zurück. If **CompareEntryIDs** returns an error, which can occur if no address book provider has registered a **MAPIUID** structure that matches the one in the entry identifiers, clients and providers should not take any action based on the result of the comparison. Sie sollten stattdessen den vorsichtigsten Ansatz für die ausgeführte Aktion verwenden. 
  
## <a name="see-also"></a>Siehe auch



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

