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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327286"
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
  
> Bitmaske von Flags, die den Typ der Zeichenfolgen steuert. Das folgende Flag kann verwendet werden:
    
MAPI_UNICODE 
  
> Die Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.
    
 **hDevmode**
  
> Wechseln Sie zum Modus des Druckers.
    
 **hDevnames**
  
> Handle zum Pfad des Druckers.
    
 **ulFirstPageNumber**
  
> Seitennummer der ersten Zu druckten Seite.
    
 **ulFPrintAttachments**
  
> Flag, das angibt, ob Anlagen gedruckt werden sollen. Wenn Anlagen gedruckt werden sollen, wird das **ulFPrintAttachments-Element** auf 1 festgelegt. Wenn keine Anlagen gedruckt werden sollen, wird sie auf 0 festgelegt. 
    
## <a name="remarks"></a>Hinweise

Die **FORMPRINTSETUP-Struktur** wird verwendet, um die Druckeinrichtungsinformationen für ein Formularobjekt zu beschreiben. Implementierungen von [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) füllen die **FORMPRINTSETUP-Struktur** aus und geben sie im Inhalt des _lppFormPrintSetup-Ausgabeparameters_ von **GetPrintSetup zurück.**
  
Wenn das MAPI_UNICODE im  _ulFlags-Parameter_ von **GetPrintSetup** übergeben wird, sollten die Zeichenfolgen, auf die von den **Mitgliedern hDevmode** und **hDevnames** verwiesen wird, im Unicode-Format vorliegen. Andernfalls sollten die Zeichenfolgen im ANSI-Format vorliegen. 
  
Formularbetrachter, die **IMAPIViewContext** implementieren, müssen die **FORMPRINTSETUP-Struktur** mithilfe der MAPI-Zuweisungsfunktion [MAPIAllocateBuffer](mapiallocatebuffer.md)zuordnen, weisen jedoch die einzelnen Member **hDevMode** und **hDevNames** mit der Windows-Funktion [GlobalAlloc zu.](https://go.microsoft.com/fwlink/?LinkId=132110) Die Freigabe des Arbeitsspeichers wird ähnlich behandelt. Die **Elemente hDevMode** und **hDevNames** müssen mithilfe der Windows-Funktion [GlobalFree](https://go.microsoft.com/fwlink/?LinkId=132108) frei, während die **FORMPRINTSETUP-Struktur** mit der [MAPIFreeBuffer-Funktion](mapifreebuffer.md) freigeräumt werden muss. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)


[MAPI-Strukturen](mapi-structures.md)

