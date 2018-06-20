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
ms.openlocfilehash: 730c24a179cc6aaf8dc2068199ffc206d30156b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791898"
---
# <a name="hrcompareabentryidswithexchangecontext"></a>HrCompareABEntryIDsWithExchangeContext

  
  
**Betrifft**: Outlook 
  
Vergleicht zwei Address Book **EntryIDs** sicher in einem Profil mehrere Exchange. Diese Funktion ist eine Funktion Ersatz für [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
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
  
> [in] Die angemeldete **IMAPISession**. Es darf nicht NULL sein.
    
 _pEmsmdbUID_
  
> [in] Ein Zeiger auf eine **EmsmdbUID** , die den Exchange-Dienst identifiziert, die die Exchange-Adressbuchanbieter enthält, die diese Funktion zum Anzeigen von Details auf die Eintrags-ID verwendet werden soll. Wenn eingehende Eintrags-ID nicht um ein Exchange-Adressbuchanbieter Eintrags-ID ist, dieser Parameter wird ignoriert, und der Funktionsaufruf verhält sich wie [IAddrBook::Details](iaddrbook-details.md). Wenn dieser Parameter auf NULL oder eine MAPIUID NULL ist, verhält sich diese Funktion wie [IAddrBook::Details](iaddrbook-details.md).
    
 _pAddrBook_
  
> [in] Das Adressbuch verwendet, um die Eintrags-ID zu öffnen. Es darf nicht NULL sein.
    
 _cbEntryID1_
  
> [in] Die Byteanzahl des ersten Eintrags-ID, die durch den Parameter _lpEntryID1_ angegeben. 
    
 _lpEntryID1_
  
> [in] Ein Zeiger auf die erste Eintrags-ID, die den Adresseintrag Adressbuch zum Vergleichen von eigenständigen darstellt.
    
 _cbEntryID2_
  
> [in] Anzahl von Bytes aus der zweite Eintrags-ID, die durch den Parameter _lpEntryID2_ angegeben. 
    
 _lpEntryID2_
  
> [in] Ein Zeiger auf die zweite Eintrags-ID im Vergleich verwendete darstellt, der den Adresseintrag Adressbuch, verglichen werden soll.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpulResult_
  
> [out] Ein Zeiger auf den Speicherort, der die Ergebnisse des Vergleichs enthält. 
    

