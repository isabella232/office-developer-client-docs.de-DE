---
title: FORMPRINTSETUP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FORMPRINTSETUP
api_type:
- COM
ms.assetid: 6e82fe94-47bd-4a25-b25b-0ab6fe2db274
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c2b9176e21341ef28e6f0bc007757b097a05daee
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386572"
---
# <a name="formprintsetup"></a>FORMPRINTSETUP

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt die print Setupinformationen für das Form-Objekt. 
  
|||
|:-----|:-----|
|Headerdatei:  <br/> |Mapiform.h  <br/> |
   
```cpp
typedef struct
{
  ULONG ulFlags;
  HDEVMODE hDevMode;
  HDEVNAMES hDevNames;
  ULONG ulFirstPageNumber;
  ULONG ulFPrintAttachments;
} FORMPRINTSETUP, FAR * LPFORMPRINTSETUP;

```

## <a name="members"></a>Elemente

 **ulFlags**
  
> Bitmaske aus Flags, die den Typ der Zeichenfolgen steuert. Das folgende Flag kann verwendet werden:
    
PARAMETER MAPI_UNICODE 
  
> Die Zeichenfolgen sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.
    
 **hDevMode-Feld**
  
> In den Modus des Druckers behandeln.
    
 **hDevnames**
  
> Handle für den Pfad des Druckers an.
    
 **ulFirstPageNumber**
  
> Die Seitenzahl der ersten Seite gedruckt werden.
    
 **ulFPrintAttachments**
  
> Flag, die angibt, ob Anlagen zu druckende vorhanden sind. Wenn Anlagen drucken vorhanden sind, wird der Member **UlFPrintAttachments** auf 1 festgelegt. Wenn keine Anhänge zu druckende vorhanden sind, wird es auf 0 festgelegt. 
    
## <a name="remarks"></a>Hinweise

Die Struktur **FORMPRINTSETUP** wird verwendet, um die print Setupinformationen für ein Form-Objekt beschreiben. Die Implementierung von [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) füllen Sie die **FORMPRINTSETUP** -Struktur und in den Inhalt der _LppFormPrintSetup_ Output-Parameter des **GetPrintSetup**zurückgeben.
  
Wenn die Option MAPI_UNICODE im _UlFlags_ -Parameter der **GetPrintSetup**übergeben wird, sollte die Zeichenfolgen, die durch die **hDevMode-Feld** und **hDevnames** Member im Unicode-Format. Andernfalls müssen die Zeichenfolgen in ANSI-Format sein. 
  
Formular Viewer **IMAPIViewContext** implementieren die **FORMPRINTSETUP** -Struktur, die mit der MAPI-Zuweisung Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md)zuordnen, aber die einzelnen Mitgliedern, **hDevMode-Feld** und **hDevNames**zuweisen, mit der Windows-Funktion [GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110). Die Freigabe des Arbeitsspeichers ist ähnlich behandelt. Die Member **hDevMode-Feld** und **hDevNames** müssen mithilfe der Windows-Funktion [GlobalFree](https://go.microsoft.com/fwlink/?LinkId=132108) , während die **FORMPRINTSETUP** -Struktur mit der Funktion [MAPIFreeBuffer](mapifreebuffer.md) freigegeben werden muss freigegeben werden. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)


[MAPI-Strukturen](mapi-structures.md)

