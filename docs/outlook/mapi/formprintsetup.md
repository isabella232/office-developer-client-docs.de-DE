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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ff46c58fbb352d56ae3df09d6949cdd5f614673f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791731"
---
# <a name="formprintsetup"></a><span data-ttu-id="53924-103">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="53924-103">FORMPRINTSETUP</span></span>

  
  
<span data-ttu-id="53924-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="53924-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="53924-105">Beschreibt die print Setupinformationen für das Form-Objekt.</span><span class="sxs-lookup"><span data-stu-id="53924-105">Describes the print setup information for the form object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="53924-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="53924-106">Header file:</span></span>  <br/> |<span data-ttu-id="53924-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="53924-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="53924-108">Members</span><span class="sxs-lookup"><span data-stu-id="53924-108">Members</span></span>

 <span data-ttu-id="53924-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="53924-109">**ulFlags**</span></span>
  
> <span data-ttu-id="53924-110">Bitmaske aus Flags, die den Typ der Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="53924-110">Bitmask of flags that controls the type of the strings.</span></span> <span data-ttu-id="53924-111">Das folgende Flag kann verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="53924-111">The following flag can be used:</span></span>
    
<span data-ttu-id="53924-112">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="53924-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="53924-113">Die Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="53924-113">The strings are in Unicode format.</span></span> <span data-ttu-id="53924-114">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="53924-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="53924-115">**hDevMode-Feld**</span><span class="sxs-lookup"><span data-stu-id="53924-115">**hDevmode**</span></span>
  
> <span data-ttu-id="53924-116">In den Modus des Druckers behandeln.</span><span class="sxs-lookup"><span data-stu-id="53924-116">Handle to the mode of the printer.</span></span>
    
 <span data-ttu-id="53924-117">**hDevnames**</span><span class="sxs-lookup"><span data-stu-id="53924-117">**hDevnames**</span></span>
  
> <span data-ttu-id="53924-118">Handle für den Pfad des Druckers an.</span><span class="sxs-lookup"><span data-stu-id="53924-118">Handle to the path of the printer.</span></span>
    
 <span data-ttu-id="53924-119">**ulFirstPageNumber**</span><span class="sxs-lookup"><span data-stu-id="53924-119">**ulFirstPageNumber**</span></span>
  
> <span data-ttu-id="53924-120">Die Seitenzahl der ersten Seite gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="53924-120">Page number of the first page to be printed.</span></span>
    
 <span data-ttu-id="53924-121">**ulFPrintAttachments**</span><span class="sxs-lookup"><span data-stu-id="53924-121">**ulFPrintAttachments**</span></span>
  
> <span data-ttu-id="53924-122">Flag, die angibt, ob Anlagen zu druckende vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="53924-122">Flag that indicates whether there are attachments to be printed.</span></span> <span data-ttu-id="53924-123">Wenn Anlagen drucken vorhanden sind, wird der Member **UlFPrintAttachments** auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="53924-123">If there are attachments to print, the **ulFPrintAttachments** member is set to 1.</span></span> <span data-ttu-id="53924-124">Wenn keine Anhänge zu druckende vorhanden sind, wird es auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="53924-124">If there are no attachments to print, it is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="53924-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="53924-125">Remarks</span></span>

<span data-ttu-id="53924-126">Die Struktur **FORMPRINTSETUP** wird verwendet, um die print Setupinformationen für ein Form-Objekt beschreiben.</span><span class="sxs-lookup"><span data-stu-id="53924-126">The **FORMPRINTSETUP** structure is used to describe the print setup information for a form object.</span></span> <span data-ttu-id="53924-127">Die Implementierung von [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) füllen Sie die **FORMPRINTSETUP** -Struktur und in den Inhalt der _LppFormPrintSetup_ Output-Parameter des **GetPrintSetup**zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="53924-127">Implementations of [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) fill in the **FORMPRINTSETUP** structure and return it in the contents of the  _lppFormPrintSetup_ output parameter of **GetPrintSetup**.</span></span>
  
<span data-ttu-id="53924-128">Wenn die Option MAPI_UNICODE im _UlFlags_ -Parameter der **GetPrintSetup**übergeben wird, sollte die Zeichenfolgen, die durch die **hDevMode-Feld** und **hDevnames** Member im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="53924-128">If the MAPI_UNICODE flag is passed in the  _ulFlags_ parameter of **GetPrintSetup**, the strings referenced by the **hDevmode** and **hDevnames** members should be in Unicode format.</span></span> <span data-ttu-id="53924-129">Andernfalls müssen die Zeichenfolgen in ANSI-Format sein.</span><span class="sxs-lookup"><span data-stu-id="53924-129">Otherwise, the strings should be in ANSI format.</span></span> 
  
<span data-ttu-id="53924-130">Formular Viewer **IMAPIViewContext** implementieren die **FORMPRINTSETUP** -Struktur, die mit der MAPI-Zuweisung Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md)zuordnen, aber die einzelnen Mitgliedern, **hDevMode-Feld** und **hDevNames**zuweisen, mit der Windows-Funktion [GlobalAlloc](http://go.microsoft.com/fwlink/?LinkId=132110).</span><span class="sxs-lookup"><span data-stu-id="53924-130">Form viewers implementing **IMAPIViewContext** must allocate the **FORMPRINTSETUP** structure using the MAPI allocator function [MAPIAllocateBuffer](mapiallocatebuffer.md), but allocate the individual members, **hDevMode** and **hDevNames**, with the Windows function [GlobalAlloc](http://go.microsoft.com/fwlink/?LinkId=132110).</span></span> <span data-ttu-id="53924-131">Die Freigabe des Arbeitsspeichers ist ähnlich behandelt.</span><span class="sxs-lookup"><span data-stu-id="53924-131">The release of memory is handled similarly.</span></span> <span data-ttu-id="53924-132">Die Member **hDevMode-Feld** und **hDevNames** müssen mithilfe der Windows-Funktion [GlobalFree](http://go.microsoft.com/fwlink/?LinkId=132108) , während die **FORMPRINTSETUP** -Struktur mit der Funktion [MAPIFreeBuffer](mapifreebuffer.md) freigegeben werden muss freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="53924-132">The **hDevMode** and **hDevNames** members must be freed using the Windows function [GlobalFree](http://go.microsoft.com/fwlink/?LinkId=132108) whereas the **FORMPRINTSETUP** structure must be freed with the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="53924-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53924-133">See also</span></span>



[<span data-ttu-id="53924-134">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="53924-134">IMAPIViewContext::GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md)
  
[<span data-ttu-id="53924-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="53924-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="53924-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="53924-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)


[<span data-ttu-id="53924-137">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="53924-137">MAPI Structures</span></span>](mapi-structures.md)

