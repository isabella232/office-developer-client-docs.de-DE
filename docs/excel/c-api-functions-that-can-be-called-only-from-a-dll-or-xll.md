---
title: C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Funktionen [Excel 2007], c-API, die von dll oder XLL aufgerufen wird
localization_priority: Normal
ms.assetid: 87c9e75b-c364-4428-a169-010886313b85
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e6d2d3c824c482e3726cdaefa869393002a80f44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301652"
---
# <a name="c-api-functions-that-can-be-called-only-from-a-dll-or-xll"></a><span data-ttu-id="cf753-104">C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="cf753-104">C API Functions That Can Be Called Only from a DLL or XLL</span></span>

<span data-ttu-id="cf753-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cf753-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cf753-106">Die C-API bietet 15 Microsoft Excel-Rückruffunktionen, die nur mithilfe der **Excel4**-, **Excel4v**-, **Excel12**-oder **Excel12v** -Funktionen (oder durch eine dieser Funktionen indirekt mithilfe der Frameworkfunktionen Excel) aufgerufen werden können. \*\* \*\*oder **Excel12f**).</span><span class="sxs-lookup"><span data-stu-id="cf753-106">The C API provides 15 Microsoft Excel callback functions that can only be called by using the **Excel4**, **Excel4v**, **Excel12**, or **Excel12v** functions (or by one of these functions indirectly using the Framework functions **Excel** or **Excel12f**).</span></span> <span data-ttu-id="cf753-107">Das heißt, Sie können nur aus einer DLL oder XLL aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cf753-107">This means they can only be called from a DLL or XLL.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="cf753-108">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="cf753-108">In this section</span></span>

[<span data-ttu-id="cf753-109">xlAbort</span><span class="sxs-lookup"><span data-stu-id="cf753-109">xlAbort</span></span>](xlabort.md)
  
[<span data-ttu-id="cf753-110">xlAsyncReturn</span><span class="sxs-lookup"><span data-stu-id="cf753-110">xlAsyncReturn</span></span>](xlasyncreturn.md)
  
[<span data-ttu-id="cf753-111">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="cf753-111">xlCoerce</span></span>](xlcoerce.md)
  
[<span data-ttu-id="cf753-112">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="cf753-112">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
  
[<span data-ttu-id="cf753-113">xlDisableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="cf753-113">xlDisableXLMsgs</span></span>](xldisablexlmsgs.md)
  
[<span data-ttu-id="cf753-114">xlEnableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="cf753-114">xlEnableXLMsgs</span></span>](xlenablexlmsgs.md)
  
[<span data-ttu-id="cf753-115">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="cf753-115">xlEventRegister</span></span>](xleventregister.md)
  
[<span data-ttu-id="cf753-116">xlFree</span><span class="sxs-lookup"><span data-stu-id="cf753-116">xlFree</span></span>](xlfree.md)
  
[<span data-ttu-id="cf753-117">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="cf753-117">xlGetBinaryName</span></span>](xlgetbinaryname.md)
  
[<span data-ttu-id="cf753-118">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="cf753-118">xlGetHwnd</span></span>](xlgethwnd.md)
  
[<span data-ttu-id="cf753-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="cf753-119">xlGetInst</span></span>](xlgetinst.md)
  
[<span data-ttu-id="cf753-120">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="cf753-120">xlGetInstPtr</span></span>](xlgetinstptr.md)
  
[<span data-ttu-id="cf753-121">xlGetName</span><span class="sxs-lookup"><span data-stu-id="cf753-121">xlGetName</span></span>](xlgetname.md)
  
[<span data-ttu-id="cf753-122">xlRunningOnCluster</span><span class="sxs-lookup"><span data-stu-id="cf753-122">xlRunningOnCluster</span></span>](xlrunningoncluster.md)
  
[<span data-ttu-id="cf753-123">xlSet</span><span class="sxs-lookup"><span data-stu-id="cf753-123">xlSet</span></span>](xlset.md)
  
[<span data-ttu-id="cf753-124">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="cf753-124">xlSheetId</span></span>](xlsheetid.md)
  
[<span data-ttu-id="cf753-125">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="cf753-125">xlSheetNm</span></span>](xlsheetnm.md)
  
[<span data-ttu-id="cf753-126">xlStack</span><span class="sxs-lookup"><span data-stu-id="cf753-126">xlStack</span></span>](xlstack.md)
  
[<span data-ttu-id="cf753-127">xlUDF</span><span class="sxs-lookup"><span data-stu-id="cf753-127">xlUDF</span></span>](xludf.md)
  
## <a name="see-also"></a><span data-ttu-id="cf753-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf753-128">See also</span></span>



[<span data-ttu-id="cf753-129">C-API-R�ckruf funktioniert Excel4 Excel12</span><span class="sxs-lookup"><span data-stu-id="cf753-129">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)

