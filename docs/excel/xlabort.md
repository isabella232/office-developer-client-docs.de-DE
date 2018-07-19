---
title: Bereichsgröße
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAbort
keywords:
- Bereichsgröße-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 0fe71454-6b00-464b-8abf-afb209d57754
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e90cbe496404b4cc602dee1ad21c91c8f5f91bfd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790588"
---
# <a name="xlabort"></a><span data-ttu-id="f6a08-104">Bereichsgröße</span><span class="sxs-lookup"><span data-stu-id="f6a08-104">xlAbort</span></span>

 <span data-ttu-id="f6a08-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f6a08-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f6a08-106">Ergibt den Prozessor an anderen Vorgängen im System und überprüft, ob der Benutzer die **ESC-Taste** , um ein Makro abzubrechen gedrückt hat.</span><span class="sxs-lookup"><span data-stu-id="f6a08-106">Yields the processor to other tasks in the system and checks whether the user has pressed **ESC** to cancel a macro.</span></span> <span data-ttu-id="f6a08-107">Wenn der Benutzer während einer neuberechnung Arbeitsmappe die **ESC-Taste** gedrückt wurde, können sie auch aus innerhalb einer Tabellenfunktion erkannt werden durch Aufrufen dieser Funktion.</span><span class="sxs-lookup"><span data-stu-id="f6a08-107">If the user has pressed **ESC** during a workbook recalculation, it can also be detected from within a worksheet function by calling this function.</span></span> 
  
```cs
Excel12(xlAbort, LPXLOPER12 pxRes, 1, LPXLOPER12 pxRetain);
```

## <a name="parameters"></a><span data-ttu-id="f6a08-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6a08-108">Parameters</span></span>

 <span data-ttu-id="f6a08-109">_pxRetain_ (**XltypeBool**)</span><span class="sxs-lookup"><span data-stu-id="f6a08-109">_pxRetain_ (**xltypeBool**)</span></span>
  
<span data-ttu-id="f6a08-110">(Optional).</span><span class="sxs-lookup"><span data-stu-id="f6a08-110">(Optional).</span></span> <span data-ttu-id="f6a08-111">Wenn **FALSE**, diese Funktion für die Unterbrechung überprüft und löscht alle ausstehenden Umbruch.</span><span class="sxs-lookup"><span data-stu-id="f6a08-111">If **FALSE**, this function checks for the break condition and clears any pending break.</span></span> <span data-ttu-id="f6a08-112">Dies ermöglicht dem Benutzer trotz der Unterbrechung fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="f6a08-112">This enables the user to continue despite the break condition.</span></span> <span data-ttu-id="f6a08-113">Wenn dieses Argument ausgelassen wird oder den Wert **TRUE**, überprüft die Funktion für den Abbruch eines Benutzers ohne löschen.</span><span class="sxs-lookup"><span data-stu-id="f6a08-113">If this argument is omitted or is **TRUE**, the function checks for a user abort without clearing it.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="f6a08-114">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6a08-114">Property value/Return value</span></span>

<span data-ttu-id="f6a08-115">Gibt **TRUE** (**XltypeBool**) zurück, wenn der Benutzer die **ESC-Taste**gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="f6a08-115">Returns **TRUE** (**xltypeBool**) if the user has pressed **ESC**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f6a08-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f6a08-116">Remarks</span></span>

### 

#### <a name="frequent-calls-may-be-needed"></a><span data-ttu-id="f6a08-117">Häufig ist eventuell erforderlich</span><span class="sxs-lookup"><span data-stu-id="f6a08-117">Frequent Calls May Be Needed</span></span>

<span data-ttu-id="f6a08-118">Funktionen und Befehle, die eine lange dauern konnte sollte diese Funktion häufig, um den Prozessor an anderen Vorgängen im System zu erzielen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f6a08-118">Functions and commands that could take a long time should call this function frequently to yield the processor to other tasks in the system.</span></span>
  
#### <a name="avoid-sensitive-language"></a><span data-ttu-id="f6a08-119">Vermeiden Sie vertrauliche Sprache</span><span class="sxs-lookup"><span data-stu-id="f6a08-119">Avoid Sensitive Language</span></span>

<span data-ttu-id="f6a08-120">Vermeiden der Verwendung des Begriffs "Abbrechen" auf der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="f6a08-120">Avoid using the term "Abort" in your user interface.</span></span> <span data-ttu-id="f6a08-121">Erwägen, "Abbrechen", "Anhalten", "Unterbrochen" oder "Stop" stattdessen.</span><span class="sxs-lookup"><span data-stu-id="f6a08-121">Consider using "Cancel," "Halt," "Break," or "Stop" instead.</span></span>
  
## <a name="example"></a><span data-ttu-id="f6a08-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f6a08-122">Example</span></span>

<span data-ttu-id="f6a08-123">Mit dem folgende Code wird die aktive Zelle wiederholt auf einem Blatt verschoben, bis eine Minute vergangen ist oder der Benutzer die **ESC-Taste**drückt.</span><span class="sxs-lookup"><span data-stu-id="f6a08-123">The following code repeatedly moves the active cell on a sheet until one minute has elapsed or until the user presses **ESC**.</span></span> <span data-ttu-id="f6a08-124">Sie ruft die Funktion **Bereichsgröße** gelegentlich.</span><span class="sxs-lookup"><span data-stu-id="f6a08-124">It calls the function **xlAbort** occasionally.</span></span> <span data-ttu-id="f6a08-125">Dies ergibt Prozessor, gemeinsame Multitasking Beschleunigung.</span><span class="sxs-lookup"><span data-stu-id="f6a08-125">This yields the processor, easing cooperative multitasking.</span></span> 
  
 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
int WINAPI fDance(void)
{
   DWORD dtickStart;
   XLOPER12 xAbort, xConfirm;
   int boolSheet;
   int col=0;
   XCHAR rgch[32];
//
// Check what kind of sheet is active. If it is a worksheet or macro
// sheet, this function will move the selection in a loop to show
// activity. In any case, it will update the status bar with a countdown.
//
// Call xlSheetId; if that fails the current sheet is not a macro sheet or
// worksheet. Next, get the time at which to start. Then start a while
// loop that will run for one minute. During the while loop, check if the
// user has pressed ESC. If true, confirm the abort. If the abort is
// confirmed, clear the message bar and return; if the abort is not
// confirmed, clear the abort state and continue. After checking for an
// abort, move the active cell if on a worksheet or macro. Then
// update the status bar with the time remaining.
//
// This block uses TempActiveCell12(), which creates a temporary XLOPER12.
// The XLOPER12 contains a reference to a single cell on the active sheet.
// This function is part of the framework library.
//
   boolSheet = (Excel12f(xlSheetId, 0, 0) == xlretSuccess);
   dtickStart = GetTickCount();
   while (GetTickCount() < dtickStart + 60000L)
   {
      Excel12f(xlAbort, &xAbort, 0);
      if (xAbort.val.xbool)
      {
         Excel12f(xlcAlert, &xConfirm, 2,
           TempStr12(L"Are you sure you want to cancel this operation?"),
              TempNum12(1));
         if (xConfirm.val.xbool)
         {
            Excel12f(xlcMessage, 0, 1, TempBool12(0));
            return 1;
         }
         else
         {
            Excel12f(xlAbort, 0, 1, TempBool12(0));
         }
      }
      if (boolSheet)
      {
         Excel12f(xlcSelect, 0, 1,
            TempActiveCell12(0,(BYTE)col));
         col = (col + 1) & 3;
      }
      wsprintfW(rgch,L"0:%lu",
         (60000 + dtickStart - GetTickCount()) / 1000L);
      Excel12f(xlcMessage, 0, 2, TempBool12(1), TempStr12(rgch));
   }
   Excel12f(xlcMessage, 0, 1, TempBool12(0));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="f6a08-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6a08-126">See also</span></span>



[<span data-ttu-id="f6a08-127">C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen</span><span class="sxs-lookup"><span data-stu-id="f6a08-127">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

