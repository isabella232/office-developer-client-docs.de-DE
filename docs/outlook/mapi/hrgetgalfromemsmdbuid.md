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
  
Gibt die Eintrags-ID des globalen Adressbuchs für den Exchange-Dienst zurück, der von _pEmsmdbUID_identifiziert wurde. Der zurückgegebene Eintragsbezeichner sollte mit [mapifreebufferfreigegeben](mapifreebuffer.md)freigegeben werden.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |abhelp. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
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
  
> in Der angemeldete IMAPISession. Er darf nicht NULL sein.
    
 _pAddrBook_
  
> in Das zum Öffnen des Eintrags Bezeichners verwendete Adressbuch. Er darf nicht NULL sein.
    
 _pEmsmdbUID_
  
> in Ein Zeiger auf ein **emsmdbUID** , das die GAL des Exchange-Diensts identifiziert, der abgerufen werden soll. Wenn _pEmsmdbUID_ oder die UID NULL ist, ruft diese Funktion die Legacy-GAL des Exchange-Diensts ab. 
    
 _lpcbeid_
  
> Out Ein Zeiger auf die Bytezahl des Eintrags Bezeichners der globalen Adressliste.
    
 _lppeid_
  
> Out Ein Zeiger auf die Eintrags-ID der globalen Adressliste. Dies sollte mit [mapifreebufferfreigegeben](mapifreebuffer.md)freigegeben werden.
    

