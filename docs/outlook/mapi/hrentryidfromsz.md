---
title: HrEntryIDFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrEntryIDFromSz
api_type:
- COM
ms.assetid: 14c171ec-0aec-43ab-8be8-e6bc0ce28a58
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1422a8f6568c210c2d4416a58f625cc701ca3616
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571948"
---
# <a name="hrentryidfromsz"></a>HrEntryIDFromSz

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt einen Eintragsbezeichner aus der ASCII-Codierung neu. 
  
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

 _Sz_
  
> [in] Zeiger auf die ASCII-Zeichenfolge, aus der ein Eintragsbezeichner erstellt werden soll. 
    
 _Pcb_
  
> [out] Zeiger auf die Größe des Eintragsbezeichners in Byte, auf die der  _Ppentry-Parameter_ verweist. 
    
 _Ppentry_
  
> [out] Zeiger auf einen Zeiger auf die zurückgegebene [ENTRYID-Struktur,](entryid.md) die den neuen Eintragsbezeichner enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Die Neugestaltung war erfolgreich.
    
MAPI_E_INVALID_ENTRYID
  
> Die Eintrags-ID war ungültig.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **Funktionen HrEntryIDFromSz** und [HrSzFromEntryID](hrszfromentryid.md) ermöglichen die Konvertierung zwischen dem Zeichenfolgen- und binären Format von Eintragsbezeichnern. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **HrEntryIDFromSz-Funktion** weist Speicher für die ASCII-Zeichenfolge mithilfe der [MAPIAllocateBuffer-Funktion](mapiallocatebuffer.md) zu. 
  

