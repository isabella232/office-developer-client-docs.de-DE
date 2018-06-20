---
title: HrGetGALFromEmsmdbUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5db1b45f42365837d7b0e7af91f859f221ff687b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791919"
---
# <a name="hrgetgalfromemsmdbuid"></a>HrGetGALFromEmsmdbUID

  
  
**Betrifft**: Outlook 
  
Gibt die Eintrags-ID der im globalen Adressbuch für den Exchange-Dienst _pEmsmdbUID_identifizierten zurück. Die zurückgegebene Eintrags-ID sollte mithilfe der [MAPIFreeBuffer](mapifreebuffer.md)freigegeben werden.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a>Parameter

 _pSess_
  
> [in] Die angemeldete IMAPISession. Es darf nicht NULL sein.
    
 _pAddrBook_
  
> [in] Das Adressbuch verwendet, um die Eintrags-ID zu öffnen. Es darf nicht NULL sein.
    
 _pEmsmdbUID_
  
> [in] Ein Zeiger auf eine **EmsmdbUID** , die identifiziert die globale Adressliste des Exchange-Diensts abgerufen werden sollen. Wenn _pEmsmdbUID_ NULL oder die UID 0 (null) ist, gibt diese Funktion die Vorgängerversion GAL von der Exchange-Dienst. 
    
 _lpcbeid_
  
> [out] Ein Zeiger auf die Byteanzahl des Eintrags-ID der globalen Adressliste.
    
 _lppeid_
  
> [out] Ein Zeiger auf die Eintrags-ID der globalen Adressliste. Dies sollte mithilfe der [MAPIFreeBuffer](mapifreebuffer.md)freigegeben werden.
    

