---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 869122954ffe3928dfea72b8fc9fb432b9979e42
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438764"
---
# <a name="xleventregister"></a><span data-ttu-id="9e5bd-103">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="9e5bd-103">xlEventRegister</span></span>

 <span data-ttu-id="9e5bd-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9e5bd-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9e5bd-105">Wird zum Registrieren eines Ereignishandlers verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e5bd-105">Used to register an event handler.</span></span> <span data-ttu-id="9e5bd-106">Eingeführt in Excel 2010.</span><span class="sxs-lookup"><span data-stu-id="9e5bd-106">Introduced in Excel 2010.</span></span>
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a><span data-ttu-id="9e5bd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e5bd-107">Parameters</span></span>

 <span data-ttu-id="9e5bd-108">_pxProcedure_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="9e5bd-108">_pxProcedure_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="9e5bd-109">Der Name der Ereignishandlerfunktion, wie er im DLL-Code angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9e5bd-109">The name of the event handler function as it appears in the DLL code.</span></span>
  
 <span data-ttu-id="9e5bd-110">_pxEvent_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="9e5bd-110">_pxEvent_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="9e5bd-111">Das Ereignis, das von der im _pxProcedure_ -Parameter angegebenen Funktion behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="9e5bd-111">The event handled by the function designated in the  _pxProcedure_ parameter.</span></span> 
  
<span data-ttu-id="9e5bd-112">Ab Excel 2010 unterstützt Excel die folgenden Ereignisse:</span><span class="sxs-lookup"><span data-stu-id="9e5bd-112">Starting in Excel 2010, Excel supports the following events:</span></span>
  
|<span data-ttu-id="9e5bd-113">**Event**</span><span class="sxs-lookup"><span data-stu-id="9e5bd-113">**Event**</span></span>|<span data-ttu-id="9e5bd-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9e5bd-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9e5bd-115">**xleventCalculationEnded**</span><span class="sxs-lookup"><span data-stu-id="9e5bd-115">**xleventCalculationEnded**</span></span> <br/> |<span data-ttu-id="9e5bd-116">Wird ausgelöst, wenn Excel eine Berechnung abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="9e5bd-116">Raised when Excel completes a calculation.</span></span> <span data-ttu-id="9e5bd-117">Sie können alle Ressourcen freigeben, die während der Berechnung nach diesem Ereignis zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9e5bd-117">You can free any resources allocated during the calculation after this event.</span></span>  <br/> |
|<span data-ttu-id="9e5bd-118">**xleventCalculationCanceled**</span><span class="sxs-lookup"><span data-stu-id="9e5bd-118">**xleventCalculationCanceled**</span></span> <br/> |<span data-ttu-id="9e5bd-119">Wird ausgelöst, wenn der Benutzer die Berechnung unterbricht.</span><span class="sxs-lookup"><span data-stu-id="9e5bd-119">Raised when the user interrupts the calculation.</span></span> <span data-ttu-id="9e5bd-120">Die XLL sollte alle asynchronen Aktivitäten beenden.</span><span class="sxs-lookup"><span data-stu-id="9e5bd-120">The XLL should stop any asynchronous activities.</span></span> <span data-ttu-id="9e5bd-121">Das CalculationEnded-Ereignis wird unmittelbar nach diesem Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="9e5bd-121">The CalculationEnded event is raised immediately following this event.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="9e5bd-122">Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e5bd-122">Property value/Return value</span></span>

<span data-ttu-id="9e5bd-123">Wenn der Wert erfolgreich ist, wird **true** (**xltypeBool**) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9e5bd-123">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="9e5bd-124">Wenn nicht erfolgreich, gibt **false**zurück.</span><span class="sxs-lookup"><span data-stu-id="9e5bd-124">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9e5bd-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e5bd-125">See also</span></span>



[<span data-ttu-id="9e5bd-126">Asynchrone benutzerdefinierte Funktionen</span><span class="sxs-lookup"><span data-stu-id="9e5bd-126">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)

