---
title: HrGetGALFromEmsmdbUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4b05baf1f819a821da3496cc63c2b2980894efd7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575714"
---
# <a name="hrgetgalfromemsmdbuid"></a>HrGetGALFromEmsmdbUID

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    

