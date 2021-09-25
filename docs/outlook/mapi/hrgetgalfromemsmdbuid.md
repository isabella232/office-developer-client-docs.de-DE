---
title: HrGetGALFromEmsmdbUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5af9689bd79745ab6505ce9977229fc61567376b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561649"
---
# <a name="hrgetgalfromemsmdbuid"></a>HrGetGALFromEmsmdbUID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Eintragsbezeichner des globalen Adressbuchs für den von _pEmsmdbUID identifizierten_ Exchange Dienst zurück. Der zurückgegebene Eintragsbezeichner sollte mit [MAPIFreeBuffer](mapifreebuffer.md)freigegeben werden.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
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
  
> [in] Die angemeldete IMAPISession. Er darf nicht NULL sein.
    
 _pAddrBook_
  
> [in] Das Zum Öffnen des Eintragsbezeichners verwendete Adressbuch. Er darf nicht NULL sein.
    
 _pEmsmdbUID_
  
> [in] Ein Zeiger auf eine **emsmdbUID,** die die GAL des abzurufenden Exchange Diensts identifiziert. Wenn _pEmsmdbUID_ NULL oder die Null-UID ist, ruft diese Funktion die legacy-GAL des Exchange-Diensts ab. 
    
 _lpcbeid_
  
> [out] Ein Zeiger auf die Byteanzahl des Eintragsbezeichners der globalen Adressliste.
    
 _lppeid_
  
> [out] Ein Zeiger auf den Eintragsbezeichner der globalen Adressliste. Dies sollte mit [MAPIFreeBuffer](mapifreebuffer.md)freigegeben werden.
    

