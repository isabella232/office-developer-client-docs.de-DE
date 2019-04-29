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
  
Vergleicht zwei Eintrags-IDs, die zu einem bestimmten Adressbuchanbieter gehören, um zu bestimmen, ob Sie auf dasselbe Adressbuchobjekt verweisen. 
  
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
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID1_ -Parameter verwiesen wird. 
    
 _lpEntryID1_
  
> in Ein Zeiger auf den ersten zu vergleichenden Eintragsbezeichner.
    
 _cbEntryID2_
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID2_ -Parameter verwiesen wird. 
    
 _lpEntryID2_
  
> in Ein Zeiger auf die zweite Eintrags-ID, die verglichen werden soll.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpulResult_
  
> Out Ein Zeiger auf das Ergebnis des Vergleichs. Der Inhalt von _lpulResult_ ist auf true festgelegt, wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen; Andernfalls wird der Inhalt auf FALSE festgelegt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Eine oder beide der Eingabe Bezeichner, die mit den _lpEntryID1_ -oder _lpEntryID2_ -Parametern übergeben wurden, werden von keinem Adressbuchanbieter erkannt. 
    
## <a name="remarks"></a>Bemerkungen

Client Anwendungen und Dienstanbieter rufen die **CompareEntryIDs** -Methode auf, um zwei Eintragsbezeichner zu vergleichen, die zu einem einzelnen Adressbuchanbieter gehören, um zu bestimmen, ob Sie auf dasselbe Objekt verweisen. **CompareEntryIDs** ist nützlich, da ein Objekt mehrere gültige Eintragsbezeichner aufweisen kann. Diese Situation kann beispielsweise auftreten, nachdem eine neue Version eines Adressbuch Anbieters installiert wurde. 
  
MAPI übergibt diesen Aufruf an den Adressbuchanbieter, der für die Eintrags-IDs zuständig ist, indem er den entsprechenden Anbieter ermittelt, indem er die [MAPIUID](mapiuid.md) -Struktur in den Eintrags Bezeichnern mit der **MAPIUID** -Struktur abstimmt, die von der Anbieter. 
  
Wenn die beiden Eintragsbezeichner auf dasselbe Objekt verweisen, legt **CompareEntryIDs** den Inhalt des _lpulResult_ -Parameters auf true fest; Wenn Sie auf verschiedene Objekte verweisen, wird der Inhalt von **CompareEntryIDs** auf false festgelegt. In beiden Fällen gibt **COMPAREENTRYIDS** S_OK zurück. Wenn **CompareEntryIDs** einen Fehler zurückgibt, der auftreten kann, wenn kein Adressbuchanbieter eine **MAPIUID** -Struktur registriert hat, die mit der in den Eintrags-IDs übereinstimmt, sollten Clients und Anbieter keine Aktion basierend auf dem Ergebnis der Vergleich. Stattdessen sollten Sie den konservativsten Ansatz für die auszuführende Aktion verwenden. 
  
## <a name="see-also"></a>Siehe auch



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

