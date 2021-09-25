---
title: HrSzFromEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrSzFromEntryID
api_type:
- COM
ms.assetid: 5e3ed6b2-8eaf-44ab-bc6a-d3faabe84a93
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3f6731653fdfde158a0a03b8fa3824b39f882dc1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584507"
---
# <a name="hrszfromentryid"></a>HrSzFromEntryID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Codiert einen Eintragsbezeichner in einer ASCII-Zeichenfolge. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a>Parameter

 _cb_
  
> [in] Größe (in Byte) des Eintragsbezeichners, auf den der  _Pentryparameter_ verweist. 
    
 _Pentry_
  
> [in] Zeiger auf eine [ENTRYID-Struktur,](entryid.md) die den zu codierten Eintragsbezeichner enthält. 
    
 _Psz_
  
> [out] Zeiger auf die zurückgegebene ASCII-Zeichenfolge.
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die [Funktionen HrEntryIDFromSz](hrentryidfromsz.md) und **HrSzFromEntryID** ermöglichen die Konvertierung zwischen dem Zeichenfolgen- und binären Format von Eintragsbezeichnern. Mit MAPI sollten Sie Strukturen mit binären Daten verwenden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **HrSzFromEntryID-Funktion** weist Speicher für die ASCII-Zeichenfolge mithilfe der [MAPIAllocateBuffer-Funktion](mapiallocatebuffer.md) zu. 
  

