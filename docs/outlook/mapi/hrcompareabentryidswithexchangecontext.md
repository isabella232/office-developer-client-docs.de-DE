---
title: HrCompareABEntryIDsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e537c25f-51b5-4f06-a20a-44ee540b9a1f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4bada5913623e2eb463a9e72347bd31eb22c414b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348076"
---
# <a name="hrcompareabentryidswithexchangecontext"></a>HrCompareABEntryIDsWithExchangeContext

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Vergleicht zwei Adressbuch **entryIDs** sicher in einem Exchange-Profil. Diese Funktion ist eine Ersatzfunktion für [IAddrBook:: CompareEntryIDs](iaddrbook-compareentryids.md).
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
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
  
> in Der angemeldete **IMAPISession**. Er darf nicht NULL sein.
    
 _pEmsmdbUID_
  
> in Ein Zeiger auf ein **emsmdbUID** , das den Exchange-Dienst identifiziert, der den Exchange-Adressbuchanbieter enthält, den diese Funktion verwenden sollte, um Details zur Eintrags-ID anzuzeigen. Wenn die ID des eingehenden Eintrags kein Exchange-Adressbuchanbieter ist, wird dieser Parameter ignoriert, und der Funktionsaufruf verhält sich wie [IAddrBook::D ails](iaddrbook-details.md). Wenn dieser Parameter NULL oder eine NULL-MAPIUID ist, verhält sich diese Funktion wie [IAddrBook::D ails](iaddrbook-details.md).
    
 _pAddrBook_
  
> in Das zum Öffnen des Eintrags Bezeichners verwendete Adressbuch. Er darf nicht NULL sein.
    
 _cbEntryID1_
  
> in Die Bytezahl des ersten Eintrags-Bezeichners, der durch den _lpEntryID1_ -Parameter angegeben wird. 
    
 _lpEntryID1_
  
> in Ein Zeiger auf die erste Eintrags-ID, die den zu vergleichenden Adressbucheintrag darstellt.
    
 _cbEntryID2_
  
> in Die Bytezahl der zweiten Eintrags-ID, die durch den _lpEntryID2_ -Parameter angegeben wird. 
    
 _lpEntryID2_
  
> in Ein Zeiger auf die zweite Eintrags-ID im Vergleich, die den zu vergleichenden Adressbucheintrag darstellt.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpulResult_
  
> Out Ein Zeiger auf den Speicherort, der die Ergebnisse des Vergleichs enthält. 
    

