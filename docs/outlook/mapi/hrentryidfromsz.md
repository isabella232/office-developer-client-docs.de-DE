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
ms.openlocfilehash: ac59aeb3d650c0fbeb5bcdb580e0401cbab58ee6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347810"
---
# <a name="hrentryidfromsz"></a>HrEntryIDFromSz

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine Eintrags-ID aus der ASCII-Codierung. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a>Parameter

 _SZ_
  
> in Zeiger auf die ASCII-Zeichenfolge, aus der ein Eintragsbezeichner erstellt werden soll. 
    
 _PCB_
  
> Out Zeiger auf die Größe der Eintrags-ID, auf die durch den _ppentry_ -Parameter verwiesen wird, in Bytes. 
    
 _ppentry_
  
> Out Zeiger auf einen Zeiger auf die zurück [](entryid.md) geGebene Eintrags-ID-Struktur, die den neuen Eintragsbezeichner enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Die Erholung war erfolgreich.
    
MAPI_E_INVALID_ENTRYID
  
> Die Eintrags-ID war ungültig.
    
## <a name="remarks"></a>Bemerkungen

Die **HrEntryIDFromSz** -und [HrSzFromEntryID](hrszfromentryid.md) -Funktionen ermöglichen die Konvertierung zwischen den Zeichenfolgen-und Binärformaten der Eintrags-IDs. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **HrEntryIDFromSz** -Funktion reserviert Speicher für die ASCII-Zeichenfolge mithilfe der [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion. 
  

