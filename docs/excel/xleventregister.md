---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 00c222efce6925c3f691eb2b799adf687c22082c
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160279"
---
# <a name="xleventregister"></a><span data-ttu-id="f26c0-103">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="f26c0-103">xlEventRegister</span></span>

 <span data-ttu-id="f26c0-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f26c0-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f26c0-105">Wird zum Registrieren eines Ereignishandlers verwendet.</span><span class="sxs-lookup"><span data-stu-id="f26c0-105">Used to register an event handler.</span></span> <span data-ttu-id="f26c0-106">In Excel 2010 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f26c0-106">Introduced in Excel 2010.</span></span>
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a><span data-ttu-id="f26c0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f26c0-107">Parameters</span></span>

 <span data-ttu-id="f26c0-108">_pxProcedure_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="f26c0-108">_pxProcedure_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="f26c0-109">Der Name der Ereignis Handlerfunktion, wie er im DLL-Code angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f26c0-109">The name of the event handler function as it appears in the DLL code.</span></span>
  
 <span data-ttu-id="f26c0-110">_pxEvent_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="f26c0-110">_pxEvent_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="f26c0-111">Das Ereignis, das von der im _pxProcedure_ -Parameter festgelegten Funktion behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="f26c0-111">The event handled by the function designated in the  _pxProcedure_ parameter.</span></span> 
  
<span data-ttu-id="f26c0-112">Beginnend mit Excel 2010 unterstützt Excel die folgenden Ereignisse:</span><span class="sxs-lookup"><span data-stu-id="f26c0-112">Starting in Excel 2010, Excel supports the following events:</span></span>
  
|<span data-ttu-id="f26c0-113">**Event**</span><span class="sxs-lookup"><span data-stu-id="f26c0-113">**Event**</span></span>|<span data-ttu-id="f26c0-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f26c0-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f26c0-115">**xleventCalculationEnded**</span><span class="sxs-lookup"><span data-stu-id="f26c0-115">**xleventCalculationEnded**</span></span> <br/> |<span data-ttu-id="f26c0-116">Wird ausgelöst, wenn Excel eine Berechnung abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="f26c0-116">Raised when Excel completes a calculation.</span></span> <span data-ttu-id="f26c0-117">Sie können alle während der Berechnung zugeordneten Ressourcen nach diesem Ereignis freigeben.</span><span class="sxs-lookup"><span data-stu-id="f26c0-117">You can free any resources allocated during the calculation after this event.</span></span>  <br/> |
|<span data-ttu-id="f26c0-118">**xleventCalculationCanceled**</span><span class="sxs-lookup"><span data-stu-id="f26c0-118">**xleventCalculationCanceled**</span></span> <br/> |<span data-ttu-id="f26c0-119">Wird ausgelöst, wenn der Benutzer die Berechnung unterbricht.</span><span class="sxs-lookup"><span data-stu-id="f26c0-119">Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="f26c0-120">Die XLL sollte alle asynchronen Aktivitäten beenden.</span><span class="sxs-lookup"><span data-stu-id="f26c0-120">The XLL should stop any asynchronous activities.</span></span> <span data-ttu-id="f26c0-121">Das CalculationEnded-Ereignis wird unmittelbar nach diesem Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="f26c0-121">The CalculationEnded event is raised immediately following this event.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="f26c0-122">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f26c0-122">Property value/Return value</span></span>

<span data-ttu-id="f26c0-123">Wenn die Methode erfolgreich verläuft, hat pxRes (**xltypeInt**) einen Wert > 0.</span><span class="sxs-lookup"><span data-stu-id="f26c0-123">If successful, pxRes (**xltypeInt**) has a value > 0.</span></span> <span data-ttu-id="f26c0-124">Wenn nicht erfolgreich, pxRes = = 0.</span><span class="sxs-lookup"><span data-stu-id="f26c0-124">If unsuccessful, pxRes ==0.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f26c0-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f26c0-125">See also</span></span>



[<span data-ttu-id="f26c0-126">Asynchrone benutzerdefinierte Funktionen</span><span class="sxs-lookup"><span data-stu-id="f26c0-126">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

