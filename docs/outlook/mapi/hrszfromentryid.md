---
title: HrSzFromEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSzFromEntryID
api_type:
- COM
ms.assetid: 5e3ed6b2-8eaf-44ab-bc6a-d3faabe84a93
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4020a9161a51994ebe5b7e339d26f7612ad47361
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411554"
---
# <a name="hrszfromentryid"></a>HrSzFromEntryID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Codiert eine Eintrags-ID in eine ASCII-Zeichenfolge. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a>Parameter

 _cb_
  
> in Größe (in Bytes) der Eintrags-ID, auf die durch __ den Penty-Parameter verwiesen wird. 
    
 _Pentry_
  
> in Zeiger auf eine [Eintrags](entryid.md) -ID-Struktur, die den zu codierenden Eintragsbezeichner enthält. 
    
 _PSZ_
  
> Out Zeiger auf die zurückgegebene ASCII-Zeichenfolge.
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Bemerkungen

Die [HrEntryIDFromSz](hrentryidfromsz.md) -und **HrSzFromEntryID** -Funktionen ermöglichen die Konvertierung zwischen den Zeichenfolgen-und Binärformaten der Eintrags-IDs. Mit MAPI sollten Sie Strukturen mit Binärdaten verwenden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **HrSzFromEntryID** -Funktion reserviert Speicher für die ASCII-Zeichenfolge mithilfe der [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion. 
  

