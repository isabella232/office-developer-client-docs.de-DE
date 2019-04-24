---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 096f57335572c3788fdf129dd3bcf4a76cf62b01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304165"
---
# <a name="calludf"></a><span data-ttu-id="52be5-103">CallUDF</span><span class="sxs-lookup"><span data-stu-id="52be5-103">CallUDF</span></span>

<span data-ttu-id="52be5-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="52be5-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="52be5-105">Ruft eine benutzerdefinierte Funktion in einer Hochleistungs-Computing-Umgebung auf.</span><span class="sxs-lookup"><span data-stu-id="52be5-105">Calls a user-defined function in a high-performance computing environment.</span></span>
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a><span data-ttu-id="52be5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="52be5-106">Parameters</span></span>

<span data-ttu-id="52be5-107">_SessionId_</span><span class="sxs-lookup"><span data-stu-id="52be5-107">_SessionId_</span></span>
  
> <span data-ttu-id="52be5-108">Die ID der Sitzung, in der der Anruf vorgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="52be5-108">The ID of the session in which to make the call.</span></span>
    
<span data-ttu-id="52be5-109">_XLLName_</span><span class="sxs-lookup"><span data-stu-id="52be5-109">_XLLName_</span></span>
  
> <span data-ttu-id="52be5-110">Der Name der XLL, die die benutzerdefinierte Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="52be5-110">The name of the XLL that contains the user-defined function.</span></span>
    
<span data-ttu-id="52be5-111">_UDFName_</span><span class="sxs-lookup"><span data-stu-id="52be5-111">_UDFName_</span></span>
  
> <span data-ttu-id="52be5-112">Der Name der benutzerdefinierten Funktion.</span><span class="sxs-lookup"><span data-stu-id="52be5-112">The name of the user-defined function.</span></span>
    
<span data-ttu-id="52be5-113">_CallBackAddr_</span><span class="sxs-lookup"><span data-stu-id="52be5-113">_CallBackAddr_</span></span>
  
> <span data-ttu-id="52be5-114">Die Funktion, die der Connector aufrufen sollte, wenn die benutzerdefinierte Funktion abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="52be5-114">The function that the connector should call when the user-defined function is finished.</span></span>
    
<span data-ttu-id="52be5-115">_pxAsyncHandle_</span><span class="sxs-lookup"><span data-stu-id="52be5-115">_pxAsyncHandle_</span></span>
  
> <span data-ttu-id="52be5-116">Das von Excel verwendete asynchrone Handle und der Konnektor zum Nachverfolgen des ausstehenden benutzerdefinierten Funktionsaufrufs.</span><span class="sxs-lookup"><span data-stu-id="52be5-116">The asynchronous handle used by Excel and the connector to track the pending user-defined function call.</span></span> <span data-ttu-id="52be5-117">Der Connector verwendet ihn später, wenn der Anruf beendet wird, wenn er mit dem Funktionszeiger, der im _CallBackAddr_ -Argument übergeben wird, zurück in Excel aufruft.</span><span class="sxs-lookup"><span data-stu-id="52be5-117">The connector uses it later when the call is finished, when it calls back into Excel using the function pointer passed in the  _CallBackAddr_ argument.</span></span> 
    
<span data-ttu-id="52be5-118">_ArgCount_</span><span class="sxs-lookup"><span data-stu-id="52be5-118">_ArgCount_</span></span>
  
> <span data-ttu-id="52be5-119">Die Anzahl der Argumente, die an die benutzerdefinierte Funktion übergeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="52be5-119">The number of arguments to pass to the user-defined function.</span></span> <span data-ttu-id="52be5-120">Der maximal zulässige Wert ist 255.</span><span class="sxs-lookup"><span data-stu-id="52be5-120">The maximum value allowed is 255.</span></span>
    
<span data-ttu-id="52be5-121">_Parameter1_</span><span class="sxs-lookup"><span data-stu-id="52be5-121">_Parameter1_</span></span>
  
> <span data-ttu-id="52be5-122">Ein Wert, der an die benutzerdefinierte Funktion weitergegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="52be5-122">A value to pass to the user-defined function.</span></span> <span data-ttu-id="52be5-123">Wiederholen Sie dieses Argument für jeden von _ArgCount_angegebenen Parameter.</span><span class="sxs-lookup"><span data-stu-id="52be5-123">Repeat this argument for each parameter indicated by  _ArgCount_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="52be5-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52be5-124">Return value</span></span>

<span data-ttu-id="52be5-125">**xlHpcRetSuccess** , wenn der UDF-Aufruf erfolgreich initiiert wurde; **xlHpcRetInvalidSessionId** , wenn das _SessionID_ -Argument ungültig ist; **xlHpcRetCallFailed** bei anderen Fehlern, einschließlich Timeout. Wenn der Aufruf einen Fehlercode (alles außer **xlHpcRetSuccess**) zurückgibt, sieht Excel, dass der UDF-Aufruf fehlgeschlagen ist, die _pxAsyncHandle_ungültig macht und nicht erwartet, dass ein Rückruf stattfindet.</span><span class="sxs-lookup"><span data-stu-id="52be5-125">**xlHpcRetSuccess** if the UDF call is successfully initiated; **xlHpcRetInvalidSessionId** if the  _SessionId_ argument is invalid; **xlHpcRetCallFailed** on other failures, including time-out. If the call returns any error code (anything except **xlHpcRetSuccess**), then Excel considers the UDF call to have failed, invalidates the  _pxAsyncHandle_, and does not expect a callback to occur.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="52be5-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52be5-126">Remarks</span></span>

<span data-ttu-id="52be5-127">Diese Funktion wird asynchron ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="52be5-127">This function executes asynchronously.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="52be5-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52be5-128">See also</span></span>

- [<span data-ttu-id="52be5-129">Excel-Clusterconnector-Funktionen</span><span class="sxs-lookup"><span data-stu-id="52be5-129">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)

