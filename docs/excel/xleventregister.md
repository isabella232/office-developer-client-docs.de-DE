---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: d837d87c479f70f0184a7cf1612dea5ab8c99e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790598"
---
# <a name="xleventregister"></a><span data-ttu-id="8116b-103">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="8116b-103">xlEventRegister</span></span>

 <span data-ttu-id="8116b-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8116b-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8116b-105">Verwendet, um einen Ereignishandler registrieren.</span><span class="sxs-lookup"><span data-stu-id="8116b-105">Used to register an event handler.</span></span> <span data-ttu-id="8116b-106">In Excel 2010 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8116b-106">Introduced in Excel 2010.</span></span>
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a><span data-ttu-id="8116b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8116b-107">Parameters</span></span>

 <span data-ttu-id="8116b-108">_pxProcedure_ (**XltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="8116b-108">_pxProcedure_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="8116b-109">Der Name des der Ereignishandlerfunktion, wie er in der DLL-Code wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8116b-109">The name of the event handler function as it appears in the DLL code.</span></span>
  
 <span data-ttu-id="8116b-110">_pxEvent_ (**vom Typ XltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="8116b-110">_pxEvent_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="8116b-111">Das Ereignis behandelt, indem die Funktion, die im Parameter _PxProcedure_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="8116b-111">The event handled by the function designated in the  _pxProcedure_ parameter.</span></span> 
  
<span data-ttu-id="8116b-112">Starten in Excel 2010, unterstützt Excel die folgenden Ereignisse:</span><span class="sxs-lookup"><span data-stu-id="8116b-112">Starting in Excel 2010, Excel supports the following events:</span></span>
  
|<span data-ttu-id="8116b-113">Document.SelectionChanged **-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="8116b-113">**Event**</span></span>|<span data-ttu-id="8116b-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8116b-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8116b-115">**xleventCalculationEnded**</span><span class="sxs-lookup"><span data-stu-id="8116b-115">**xleventCalculationEnded**</span></span> <br/> |<span data-ttu-id="8116b-116">Wird ausgelöst, wenn Excel eine Berechnung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="8116b-116">Raised when Excel completes a calculation.</span></span> <span data-ttu-id="8116b-117">Sie können während der Berechnung nach diesem Ereignis reservierten Ressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="8116b-117">You can free any resources allocated during the calculation after this event.</span></span>  <br/> |
|<span data-ttu-id="8116b-118">**xleventCalculationCanceled**</span><span class="sxs-lookup"><span data-stu-id="8116b-118">**xleventCalculationCanceled**</span></span> <br/> |<span data-ttu-id="8116b-119">Wird ausgelöst, wenn der Benutzer die Berechnung unterbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="8116b-119">Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="8116b-120">Die XLL sollten alle asynchronen Aktivitäten beenden.</span><span class="sxs-lookup"><span data-stu-id="8116b-120">The XLL should stop any asynchronous activities.</span></span> <span data-ttu-id="8116b-121">Das CalculationEnded-Ereignis wird unmittelbar nach diesem Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="8116b-121">The CalculationEnded event is raised immediately following this event.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="8116b-122">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8116b-122">Property value/Return value</span></span>

<span data-ttu-id="8116b-123">Wenn erfolgreich ist, gibt **"true"** (**XltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="8116b-123">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="8116b-124">Wenn nicht erfolgreich ist, gibt **FALSE**zurück.</span><span class="sxs-lookup"><span data-stu-id="8116b-124">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8116b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8116b-125">See also</span></span>



[<span data-ttu-id="8116b-126">Asynchrone benutzerdefinierte Funktionen</span><span class="sxs-lookup"><span data-stu-id="8116b-126">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

