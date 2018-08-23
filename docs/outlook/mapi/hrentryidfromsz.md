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
ms.openlocfilehash: a524a7eb40c33d6de2f64cd5373c9a39a8a1e3df
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565298"
---
# <a name="hrentryidfromsz"></a>HrEntryIDFromSz

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Funktionen **HrEntryIDFromSz** und [HrSzFromEntryID](hrszfromentryid.md) bieten eine Konvertierung zwischen der Zeichenfolge und der binären Formate der Eintragsbezeichner. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **HrEntryIDFromSz** -Funktion weist Speicher für die Verwendung der Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) ASCII-Zeichenfolge. 
  

