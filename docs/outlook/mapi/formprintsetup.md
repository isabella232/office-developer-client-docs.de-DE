---
title: FORMPRINTSETUP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FORMPRINTSETUP
api_type:
- COM
ms.assetid: 6e82fe94-47bd-4a25-b25b-0ab6fe2db274
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 589cb1260c5986b8a93da4bfc4dae4624ac3f018
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556706"
---
# <a name="formprintsetup"></a>FORMPRINTSETUP

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt die Druckeinrichtungsinformationen für das Formularobjekt. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiform.h  <br/> |
   
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
  
> Bitmaske von Flags, die den Typ der Zeichenfolgen steuert. Das folgende Kennzeichen kann verwendet werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format.
    
 **hDevmode**
  
> Behandeln Sie den Modus des Druckers.
    
 **hDevnames**
  
> Handle to the path of the printer.
    
 **ulFirstPageNumber**
  
> Seitenzahl der ersten Seite, die gedruckt werden soll.
    
 **ulFPrintAttachments**
  
> Kennzeichen, das angibt, ob Anlagen gedruckt werden sollen. Wenn Anlagen gedruckt werden müssen, wird der **UlFPrintAttachments-Member** auf 1 festgelegt. Wenn keine Anlagen gedruckt werden müssen, wird der Wert auf 0 festgelegt. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **FORMPRINTSETUP-Struktur** wird verwendet, um die Druckeinrichtungsinformationen für ein Formularobjekt zu beschreiben. Implementierungen von [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) füllen die **FORMPRINTSETUP-Struktur** aus und geben sie im Inhalt des  _lppFormPrintSetup-Ausgabeparameters_ von **GetPrintSetup** zurück.
  
Wenn das MAPI_UNICODE Flag im  _ulFlags-Parameter_ von **GetPrintSetup** übergeben wird, sollten die Zeichenfolgen, auf die von den **Elementen "hDevmode"** und **"hDevnames"** verwiesen wird, im Unicode-Format vorliegen. Andernfalls sollten die Zeichenfolgen im ANSI-Format vorliegen. 
  
Formularviewer, die **IMAPIViewContext** implementieren, müssen die **FORMPRINTSETUP-Struktur** mithilfe der MAPI-Verteilfunktion [MAPIAllocateBuffer](mapiallocatebuffer.md)zuweisen, aber die einzelnen Member **hDevMode** und **hDevNames** mit der Windows-Funktion [GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110)zuweisen. Die Freigabe des Arbeitsspeichers wird auf ähnliche Weise behandelt. Die **Elemente "hDevMode"** und **"hDevNames"** müssen mithilfe der Windows-Funktion ["GlobalFree"](https://go.microsoft.com/fwlink/?LinkId=132108) freigegeben werden, während die **FORMPRINTSETUP-Struktur** mit der [MAPIFreeBuffer-Funktion](mapifreebuffer.md) freigegeben werden muss. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)


[MAPI-Strukturen](mapi-structures.md)

