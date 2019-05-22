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
# <a name="formprintsetup"></a><span data-ttu-id="d4f62-103">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="d4f62-103">FORMPRINTSETUP</span></span>

  
  
<span data-ttu-id="d4f62-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4f62-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4f62-105">Beschreibt die Druck Einrichtungsinformationen für das Form-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d4f62-105">Describes the print setup information for the form object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d4f62-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="d4f62-106">Header file:</span></span>  <br/> |<span data-ttu-id="d4f62-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="d4f62-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="d4f62-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="d4f62-108">Members</span></span>

 <span data-ttu-id="d4f62-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="d4f62-109">**ulFlags**</span></span>
  
> <span data-ttu-id="d4f62-110">Bitmaske von Flags, die den Typ der Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="d4f62-110">Bitmask of flags that controls the type of the strings.</span></span> <span data-ttu-id="d4f62-111">Das folgende Flag kann verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="d4f62-111">The following flag can be used:</span></span>
    
<span data-ttu-id="d4f62-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d4f62-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d4f62-113">Die Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="d4f62-113">The strings are in Unicode format.</span></span> <span data-ttu-id="d4f62-114">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, sind die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="d4f62-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="d4f62-115">**hDevmode**</span><span class="sxs-lookup"><span data-stu-id="d4f62-115">**hDevmode**</span></span>
  
> <span data-ttu-id="d4f62-116">Behandeln Sie den Modus des Druckers.</span><span class="sxs-lookup"><span data-stu-id="d4f62-116">Handle to the mode of the printer.</span></span>
    
 <span data-ttu-id="d4f62-117">**hDevnames**</span><span class="sxs-lookup"><span data-stu-id="d4f62-117">**hDevnames**</span></span>
  
> <span data-ttu-id="d4f62-118">Handle für den Druckerpfad.</span><span class="sxs-lookup"><span data-stu-id="d4f62-118">Handle to the path of the printer.</span></span>
    
 <span data-ttu-id="d4f62-119">**ulFirstPageNumber**</span><span class="sxs-lookup"><span data-stu-id="d4f62-119">**ulFirstPageNumber**</span></span>
  
> <span data-ttu-id="d4f62-120">Die Seitenzahl der ersten Seite, die gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4f62-120">Page number of the first page to be printed.</span></span>
    
 <span data-ttu-id="d4f62-121">**ulFPrintAttachments**</span><span class="sxs-lookup"><span data-stu-id="d4f62-121">**ulFPrintAttachments**</span></span>
  
> <span data-ttu-id="d4f62-122">Flag, das angibt, ob Anlagen gedruckt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d4f62-122">Flag that indicates whether there are attachments to be printed.</span></span> <span data-ttu-id="d4f62-123">Wenn Anlagen zum Drucken vorhanden sind, wird das **ulFPrintAttachments** -Element auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d4f62-123">If there are attachments to print, the **ulFPrintAttachments** member is set to 1.</span></span> <span data-ttu-id="d4f62-124">Wenn keine Anlagen zum Drucken vorhanden sind, wird Sie auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d4f62-124">If there are no attachments to print, it is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d4f62-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4f62-125">Remarks</span></span>

<span data-ttu-id="d4f62-126">Die **FORMPRINTSETUP** -Struktur wird verwendet, um die Druck Einrichtungsinformationen für ein Form-Objekt zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d4f62-126">The **FORMPRINTSETUP** structure is used to describe the print setup information for a form object.</span></span> <span data-ttu-id="d4f62-127">Implementierungen von [IMAPIViewContext:: GetPrintSetup](imapiviewcontext-getprintsetup.md) füllen die **FORMPRINTSETUP** -Struktur und geben Sie im Inhalt des _lppFormPrintSetup_ -Ausgabeparameters von **GetPrintSetup**zurück.</span><span class="sxs-lookup"><span data-stu-id="d4f62-127">Implementations of [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) fill in the **FORMPRINTSETUP** structure and return it in the contents of the  _lppFormPrintSetup_ output parameter of **GetPrintSetup**.</span></span>
  
<span data-ttu-id="d4f62-128">Wenn das MAPI_UNICODE-Flag im _ulFlags_ -Parameter von **GetPrintSetup**übergeben wird, sollten die Zeichenfolgen, auf die von den Elementen **hDevmode** und **hDevnames** verwiesen wird, im Unicode-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="d4f62-128">If the MAPI_UNICODE flag is passed in the  _ulFlags_ parameter of **GetPrintSetup**, the strings referenced by the **hDevmode** and **hDevnames** members should be in Unicode format.</span></span> <span data-ttu-id="d4f62-129">Andernfalls sollten die Zeichenfolgen im ANSI-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="d4f62-129">Otherwise, the strings should be in ANSI format.</span></span> 
  
<span data-ttu-id="d4f62-130">Formular Betrachter, die **IMAPIViewContext** implementieren, müssen die **FORMPRINTSETUP** -Struktur mithilfe der MAPI-Zuordnungsfunktion [MAPIAllocateBuffer](mapiallocatebuffer.md)zuordnen, die einzelnen Elemente **hDevMode** und **hDevNames**jedoch zuweisen. mit der Windows-Funktion [GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110).</span><span class="sxs-lookup"><span data-stu-id="d4f62-130">Form viewers implementing **IMAPIViewContext** must allocate the **FORMPRINTSETUP** structure using the MAPI allocator function [MAPIAllocateBuffer](mapiallocatebuffer.md), but allocate the individual members, **hDevMode** and **hDevNames**, with the Windows function [GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110).</span></span> <span data-ttu-id="d4f62-131">Die Veröffentlichung des Speichers wird ähnlich gehandhabt.</span><span class="sxs-lookup"><span data-stu-id="d4f62-131">The release of memory is handled similarly.</span></span> <span data-ttu-id="d4f62-132">Die **hDevMode** -und **hDevNames** -Member müssen mit der Windows-Funktion [GlobalFree](https://go.microsoft.com/fwlink/?LinkId=132108) freigegeben werden, während die **FORMPRINTSETUP** -Struktur mit der [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion freigegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="d4f62-132">The **hDevMode** and **hDevNames** members must be freed using the Windows function [GlobalFree](https://go.microsoft.com/fwlink/?LinkId=132108) whereas the **FORMPRINTSETUP** structure must be freed with the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d4f62-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4f62-133">See also</span></span>



[<span data-ttu-id="d4f62-134">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="d4f62-134">IMAPIViewContext::GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md)
  
[<span data-ttu-id="d4f62-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d4f62-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d4f62-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="d4f62-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)


[<span data-ttu-id="d4f62-137">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="d4f62-137">MAPI Structures</span></span>](mapi-structures.md)

