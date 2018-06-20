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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2b7ef789c80f85f3539ec3bbd0caf4a8adc50f3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791920"
---
# <a name="hrentryidfromsz"></a>HrEntryIDFromSz

  
  
**Betrifft**: Outlook 
  
Erstellt eine Eintrags-ID aus der ASCII-Codierung neu. 
  
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

 _su_
  
> [in] Zeiger auf die ASCII-Zeichenfolge aus dem Eintrags-ID erstellt. 
    
 _PCB_
  
> [out] Zeiger auf die Größe des Eintrags-ID, die auf das durch den Parameter _Ppentry_ in Bytes. 
    
 _ppentry_
  
> [out] Zeiger auf einen Zeiger auf das zurückgegebene [ENTRYID](entryid.md) -Struktur, die neuen Eintrags-ID enthält. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK
  
> Erneutes Erstellen war erfolgreich.
    
MAPI_E_INVALID_ENTRYID
  
> Die Eintrags-ID ist ungültig.
    
## <a name="remarks"></a>Hinweise

Die Funktionen **HrEntryIDFromSz** und [HrSzFromEntryID](hrszfromentryid.md) bieten eine Konvertierung zwischen der Zeichenfolge und der binären Formate der Eintragsbezeichner. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **HrEntryIDFromSz** -Funktion weist Speicher für die Verwendung der Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) ASCII-Zeichenfolge. 
  

