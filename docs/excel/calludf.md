---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1d55f22de88b274d0403f81717d0fddefbea0219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790384"
---
# <a name="calludf"></a><span data-ttu-id="101a9-103">CallUDF</span><span class="sxs-lookup"><span data-stu-id="101a9-103">CallUDF</span></span>

<span data-ttu-id="101a9-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="101a9-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="101a9-105">Ruft eine benutzerdefinierte Funktion in einer High Performance computing-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="101a9-105">Calls a user-defined function in a high-performance computing environment.</span></span>
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a><span data-ttu-id="101a9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="101a9-106">Parameters</span></span>

<span data-ttu-id="101a9-107">_Sitzungs-ID_</span><span class="sxs-lookup"><span data-stu-id="101a9-107">_SessionId_</span></span>
  
> <span data-ttu-id="101a9-108">Die ID der Sitzung in dem, den Anruf zu tätigen.</span><span class="sxs-lookup"><span data-stu-id="101a9-108">The ID of the session in which to make the call.</span></span>
    
<span data-ttu-id="101a9-109">_XLLName_</span><span class="sxs-lookup"><span data-stu-id="101a9-109">_XLLName_</span></span>
  
> <span data-ttu-id="101a9-110">Der Name der XLL, die die benutzerdefinierte Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="101a9-110">The name of the XLL that contains the user-defined function.</span></span>
    
<span data-ttu-id="101a9-111">_UDFName_</span><span class="sxs-lookup"><span data-stu-id="101a9-111">_UDFName_</span></span>
  
> <span data-ttu-id="101a9-112">Der Name der benutzerdefinierten Funktion.</span><span class="sxs-lookup"><span data-stu-id="101a9-112">The name of the user-defined function.</span></span>
    
<span data-ttu-id="101a9-113">_CallBackAddr_</span><span class="sxs-lookup"><span data-stu-id="101a9-113">_CallBackAddr_</span></span>
  
> <span data-ttu-id="101a9-114">Die Funktion, die der Connector aufrufen soll, wenn die benutzerdefinierte Funktion abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="101a9-114">The function that the connector should call when the user-defined function is finished.</span></span>
    
<span data-ttu-id="101a9-115">_pxAsyncHandle_</span><span class="sxs-lookup"><span data-stu-id="101a9-115">_pxAsyncHandle_</span></span>
  
> <span data-ttu-id="101a9-116">Die asynchrone Handle von Excel und den Connector zur Verfolgung des ausstehenden Funktionsaufrufs verwendet.</span><span class="sxs-lookup"><span data-stu-id="101a9-116">The asynchronous handle used by Excel and the connector to track the pending user-defined function call.</span></span> <span data-ttu-id="101a9-117">Der Connector später verwendet, wenn der Anruf beendet ist, wenn es wieder in Excel mithilfe den Funktionszeiger aufruft im _CallBackAddr_ -Argument übergeben.</span><span class="sxs-lookup"><span data-stu-id="101a9-117">The connector uses it later when the call is finished, when it calls back into Excel using the function pointer passed in the  _CallBackAddr_ argument.</span></span> 
    
<span data-ttu-id="101a9-118">_ArgCount_</span><span class="sxs-lookup"><span data-stu-id="101a9-118">_ArgCount_</span></span>
  
> <span data-ttu-id="101a9-119">Die Anzahl der an die benutzerdefinierte Funktion zu übergebenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="101a9-119">The number of arguments to pass to the user-defined function.</span></span> <span data-ttu-id="101a9-120">Der maximale zulässige Wert beträgt 255.</span><span class="sxs-lookup"><span data-stu-id="101a9-120">The maximum value allowed is 255.</span></span>
    
<span data-ttu-id="101a9-121">_1. Parameter_</span><span class="sxs-lookup"><span data-stu-id="101a9-121">_Parameter1_</span></span>
  
> <span data-ttu-id="101a9-122">Ein Wert, der benutzerdefinierten Funktion zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="101a9-122">A value to pass to the user-defined function.</span></span> <span data-ttu-id="101a9-123">Wiederholen Sie dieses Argument für jeden Parameter durch _ArgCount_angegeben.</span><span class="sxs-lookup"><span data-stu-id="101a9-123">Repeat this argument for each parameter indicated by  _ArgCount_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="101a9-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="101a9-124">Return value</span></span>

<span data-ttu-id="101a9-125">**XlHpcRetSuccess** Wenn der UDF-Anruf erfolgreich initiiert wird; **XlHpcRetInvalidSessionId** Wenn das _SessionId_ -Argument ungültig ist; **XlHpcRetCallFailed** bei anderen Fehlern, einschließlich Timeout. Wenn der Anruf alle Fehlercodes (Alles außer **XlHpcRetSuccess**) zurückgibt, klicken Sie dann Excel hält den UDF-Aufruf fehlgeschlagen, macht die _PxAsyncHandle_und davon ausgehen, dass einen Rückruf ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="101a9-125">**xlHpcRetSuccess** if the UDF call is successfully initiated; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures, including time-out. If the call returns any error code (anything except **xlHpcRetSuccess**), then Excel considers the UDF call to have failed, invalidates the  _pxAsyncHandle_, and does not expect a callback to occur.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="101a9-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="101a9-126">Remarks</span></span>

<span data-ttu-id="101a9-127">Diese Funktion wird asynchron ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="101a9-127">This function executes asynchronously.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="101a9-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="101a9-128">See also</span></span>

- [<span data-ttu-id="101a9-129">Excel-Clusterconnector-Funktionen</span><span class="sxs-lookup"><span data-stu-id="101a9-129">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

