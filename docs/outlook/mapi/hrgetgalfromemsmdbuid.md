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
ms.openlocfilehash: b9a31fec93ec7fafc4d1565d63e4bc427ba4050e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439107"
---
# <a name="hrgetgalfromemsmdbuid"></a>HrGetGALFromEmsmdbUID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Eintragsbezeichner des globalen Adressbuchs für den Exchange, der von _pEmsmdbUID identifiziert wurde._ Der zurückgegebene Eintragsbezeichner sollte mithilfe von [MAPIFreeBuffer freigebe.](mapifreebuffer.md)
  
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
  
> [in] Die angemeldete IMAPISession. Es kann nicht NULL sein.
    
 _pAddrBook_
  
> [in] Das Adressbuch, das zum Öffnen der Eintrags-ID verwendet wird. Es kann nicht NULL sein.
    
 _pEmsmdbUID_
  
> [in] Ein Zeiger auf eine **emsmdbUID,** die die GAL des abzurufenden Exchange identifiziert. Wenn _pEmsmdbUID_ NULL oder null UID ist, ruft diese Funktion die legacy-GAL des Exchange ab. 
    
 _lpcbeid_
  
> [out] Ein Zeiger auf die Byteanzahl des Eintragsbezeichners der globalen Adressliste.
    
 _lppeid_
  
> [out] Ein Zeiger auf die Eintrags-ID der globalen Adressliste. Dies sollte mithilfe von [MAPIFreeBuffer frei werden.](mapifreebuffer.md)
    

