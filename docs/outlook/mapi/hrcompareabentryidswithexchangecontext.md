---
title: HrCompareABEntryIDsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e537c25f-51b5-4f06-a20a-44ee540b9a1f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 58e90c437e0fb7b0d30a55fad624d85e742c293c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610825"
---
# <a name="hrcompareabentryidswithexchangecontext"></a>HrCompareABEntryIDsWithExchangeContext

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Vergleicht zwei **Adressbucheintrags-ID** sicher in einem Profil mit mehreren Exchange. Diese Funktion ist eine Ersatzfunktion für [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
HRESULT HrCompareABEntryIDsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG * lpulResult
);
```

## <a name="parameters"></a>Parameter

 _pmsess_
  
> [in] Die angemeldete **IMAPISession**. Er darf nicht NULL sein.
    
 _pEmsmdbUID_
  
> [in] Ein Zeiger auf eine **emsmdbUID,** die den Exchange Dienst identifiziert, der den Exchange Adressbuchanbieter enthält, den diese Funktion verwenden soll, um Details zum Eintragsbezeichner anzuzeigen. Wenn der Bezeichner für den eingehenden Eintrag kein Exchange Adressbuchanbieter-Eintragsbezeichner ist, wird dieser Parameter ignoriert, und der Funktionsaufruf verhält sich wie [IAddrBook::D etails](iaddrbook-details.md). Wenn dieser Parameter NULL oder eine Null MAPIUID ist, verhält sich diese Funktion wie [IAddrBook::D etails](iaddrbook-details.md).
    
 _pAddrBook_
  
> [in] Das Zum Öffnen des Eintragsbezeichners verwendete Adressbuch. Er darf nicht NULL sein.
    
 _cbEntryID1_
  
> [in] Die Byteanzahl des ersten Eintragsbezeichners, der durch den  _LpEntryID1-Parameter_ angegeben wird. 
    
 _lpEntryID1_
  
> [in] Ein Zeiger auf den ersten Eintragsbezeichner, der den zu vergleichenden Adressbucheintrag darstellt.
    
 _cbEntryID2_
  
> [in] Die Byteanzahl des zweiten Eintragsbezeichners, der durch den  _LpEntryID2-Parameter_ angegeben wird. 
    
 _lpEntryID2_
  
> [in] Ein Zeiger auf den zweiten Eintragsbezeichner, der im Vergleich verwendet wird und den zu vergleichenden Adressbucheintrag darstellt.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpulResult_
  
> [out] Ein Zeiger auf die Position, die die Ergebnisse des Vergleichs enthält. 
    

