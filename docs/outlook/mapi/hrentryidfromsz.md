---
title: HrEntryIDFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrEntryIDFromSz
api_type:
- COM
ms.assetid: 14c171ec-0aec-43ab-8be8-e6bc0ce28a58
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ac59aeb3d650c0fbeb5bcdb580e0401cbab58ee6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437728"
---
# <a name="hrentryidfromsz"></a>HrEntryIDFromSz

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt einen Eintragsbezeichner aus seiner ASCII-Codierung neu. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a>Parameter

 _sz_
  
> [in] Zeiger auf die ASCII-Zeichenfolge, aus der ein Eintragsbezeichner erstellt werden soll. 
    
 _leiterplatte_
  
> [out] Zeiger auf die Größe des Eintragsbezeichners in Bytes, auf den der  _ppentry-Parameter_ verweist. 
    
 _ppentry_
  
> [out] Zeiger auf einen Zeiger auf die zurückgegebene [ENTRYID-Struktur,](entryid.md) die den neuen Eintragsbezeichner enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Die Neugestaltung war erfolgreich.
    
MAPI_E_INVALID_ENTRYID
  
> Die Eintrags-ID war ungültig.
    
## <a name="remarks"></a>Hinweise

Die **Funktionen HrEntryIDFromSz** und [HrSzFromEntryID](hrszfromentryid.md) stellen eine Konvertierung zwischen den Zeichenfolgen- und Binärformaten von Eintragsbezeichnern zur Verfügung. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **HrEntryIDFromSz-Funktion** weist der ASCII-Zeichenfolge mithilfe der [MAPIAllocateBuffer-Funktion Arbeitsspeicher](mapiallocatebuffer.md) zu. 
  

