---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 096f57335572c3788fdf129dd3bcf4a76cf62b01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433011"
---
# <a name="calludf"></a><span data-ttu-id="3586b-103">CallUDF</span><span class="sxs-lookup"><span data-stu-id="3586b-103">CallUDF</span></span>

<span data-ttu-id="3586b-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3586b-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3586b-105">Ruft eine benutzerdefinierte Funktion in einer hochleistungsorientierten Computerumgebung auf.</span><span class="sxs-lookup"><span data-stu-id="3586b-105">Calls a user-defined function in a high-performance computing environment.</span></span>
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a><span data-ttu-id="3586b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3586b-106">Parameters</span></span>

<span data-ttu-id="3586b-107">_SessionId_</span><span class="sxs-lookup"><span data-stu-id="3586b-107">_SessionId_</span></span>
  
> <span data-ttu-id="3586b-108">Die ID der Sitzung, in der der Anruf zu nehmen ist.</span><span class="sxs-lookup"><span data-stu-id="3586b-108">The ID of the session in which to make the call.</span></span>
    
<span data-ttu-id="3586b-109">_XLLName_</span><span class="sxs-lookup"><span data-stu-id="3586b-109">_XLLName_</span></span>
  
> <span data-ttu-id="3586b-110">Der Name der XLL, die die benutzerdefinierte Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="3586b-110">The name of the XLL that contains the user-defined function.</span></span>
    
<span data-ttu-id="3586b-111">_UDFName_</span><span class="sxs-lookup"><span data-stu-id="3586b-111">_UDFName_</span></span>
  
> <span data-ttu-id="3586b-112">Der Name der benutzerdefinierten Funktion.</span><span class="sxs-lookup"><span data-stu-id="3586b-112">The name of the user-defined function.</span></span>
    
<span data-ttu-id="3586b-113">_CallBackAddr_</span><span class="sxs-lookup"><span data-stu-id="3586b-113">_CallBackAddr_</span></span>
  
> <span data-ttu-id="3586b-114">Die Funktion, die der Connector aufrufen soll, wenn die benutzerdefinierte Funktion beendet ist.</span><span class="sxs-lookup"><span data-stu-id="3586b-114">The function that the connector should call when the user-defined function is finished.</span></span>
    
<span data-ttu-id="3586b-115">_pxAsyncHandle_</span><span class="sxs-lookup"><span data-stu-id="3586b-115">_pxAsyncHandle_</span></span>
  
> <span data-ttu-id="3586b-116">Das asynchrone Handle, das von Excel und dem Connector zum Nachverfolgen des ausstehenden benutzerdefinierten Funktionsaufrufs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3586b-116">The asynchronous handle used by Excel and the connector to track the pending user-defined function call.</span></span> <span data-ttu-id="3586b-117">Der Connector verwendet ihn später, wenn der Aufruf beendet ist, wenn er mit Excel aufruft, der im _Argument CallBackAddr übergeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="3586b-117">The connector uses it later when the call is finished, when it calls back into Excel using the function pointer passed in the  _CallBackAddr_ argument.</span></span> 
    
<span data-ttu-id="3586b-118">_ArgCount_</span><span class="sxs-lookup"><span data-stu-id="3586b-118">_ArgCount_</span></span>
  
> <span data-ttu-id="3586b-119">Die Anzahl der Argumente, die an die benutzerdefinierte Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="3586b-119">The number of arguments to pass to the user-defined function.</span></span> <span data-ttu-id="3586b-120">Der maximal zulässige Wert ist 255.</span><span class="sxs-lookup"><span data-stu-id="3586b-120">The maximum value allowed is 255.</span></span>
    
<span data-ttu-id="3586b-121">_Parameter1_</span><span class="sxs-lookup"><span data-stu-id="3586b-121">_Parameter1_</span></span>
  
> <span data-ttu-id="3586b-122">Ein Wert, der an die benutzerdefinierte Funktion übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="3586b-122">A value to pass to the user-defined function.</span></span> <span data-ttu-id="3586b-123">Wiederholen Sie dieses Argument für jeden parameter, der durch _ArgCount angegeben wird._</span><span class="sxs-lookup"><span data-stu-id="3586b-123">Repeat this argument for each parameter indicated by  _ArgCount_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3586b-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3586b-124">Return value</span></span>

<span data-ttu-id="3586b-125">**xlHpcRetSuccess,** wenn der #A0 erfolgreich initiiert wurde. **xlHpcRetInvalidSessionId,** wenn _das Argument SessionId_ ungültig ist; **xlHpcRetCallFailed** bei anderen Fehlern, einschließlich Eines-Zeit-Outs. Wenn der Aufruf Fehlercode zurückgibt (mit Ausnahme von **xlHpcRetSuccess),** wird von Excel der UDF-Aufruf als fehlgeschlagen betrachtet, der _pxAsyncHandle_ ungültig gemacht und kein Rückruf erwartet.</span><span class="sxs-lookup"><span data-stu-id="3586b-125">**xlHpcRetSuccess** if the UDF call is successfully initiated; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures, including time-out. If the call returns any error code (anything except **xlHpcRetSuccess**), then Excel considers the UDF call to have failed, invalidates the  _pxAsyncHandle_, and does not expect a callback to occur.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3586b-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3586b-126">Remarks</span></span>

<span data-ttu-id="3586b-127">Diese Funktion wird asynchron ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3586b-127">This function executes asynchronously.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3586b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3586b-128">See also</span></span>

- [<span data-ttu-id="3586b-129">Excel-Clusterconnector-Funktionen</span><span class="sxs-lookup"><span data-stu-id="3586b-129">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

