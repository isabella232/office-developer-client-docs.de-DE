---
title: C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Funktionen [excel 2007], C-api aus Dll oder Xll aufgerufen
localization_priority: Normal
ms.assetid: 87c9e75b-c364-4428-a169-010886313b85
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7935d86d1c0a460bcbec85157429d99242a73620
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790397"
---
# <a name="c-api-functions-that-can-be-called-only-from-a-dll-or-xll"></a><span data-ttu-id="91dd9-104">C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="91dd9-104">C API Functions That Can Be Called Only from a DLL or XLL</span></span>

<span data-ttu-id="91dd9-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="91dd9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="91dd9-106">Der C-API enthält 15 Rückruffunktionen für Microsoft Excel, die nur mithilfe der **Excel4**, **Excel4v**, **Excel12**oder **Excel12v** Funktionen (oder durch eine dieser Funktionen indirekt mithilfe der Funktionen zum Framework **Excel aufgerufen werden können **oder **Excel12f**).</span><span class="sxs-lookup"><span data-stu-id="91dd9-106">The C API provides 15 Microsoft Excel callback functions that can only be called by using the **Excel4**, **Excel4v**, **Excel12**, or **Excel12v** functions (or by one of these functions indirectly using the Framework functions **Excel** or **Excel12f**).</span></span> <span data-ttu-id="91dd9-107">Dies bedeutet, dass sie nur aus einer DLL oder XLL aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="91dd9-107">This means they can only be called from a DLL or XLL.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="91dd9-108">Inhalt dieses Abschnitts</span><span class="sxs-lookup"><span data-stu-id="91dd9-108">In this section</span></span>

[<span data-ttu-id="91dd9-109">Bereichsgröße</span><span class="sxs-lookup"><span data-stu-id="91dd9-109">xlAbort</span></span>](xlabort.md)
  
[<span data-ttu-id="91dd9-110">xlAsyncReturn</span><span class="sxs-lookup"><span data-stu-id="91dd9-110">xlAsyncReturn</span></span>](xlasyncreturn.md)
  
[<span data-ttu-id="91dd9-111">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="91dd9-111">xlCoerce</span></span>](xlcoerce.md)
  
[<span data-ttu-id="91dd9-112">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="91dd9-112">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
  
[<span data-ttu-id="91dd9-113">xlDisableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="91dd9-113">xlDisableXLMsgs</span></span>](xldisablexlmsgs.md)
  
[<span data-ttu-id="91dd9-114">xlEnableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="91dd9-114">xlEnableXLMsgs</span></span>](xlenablexlmsgs.md)
  
[<span data-ttu-id="91dd9-115">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="91dd9-115">xlEventRegister</span></span>](xleventregister.md)
  
[<span data-ttu-id="91dd9-116">xlFree</span><span class="sxs-lookup"><span data-stu-id="91dd9-116">xlFree</span></span>](xlfree.md)
  
[<span data-ttu-id="91dd9-117">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="91dd9-117">xlGetBinaryName</span></span>](xlgetbinaryname.md)
  
[<span data-ttu-id="91dd9-118">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="91dd9-118">xlGetHwnd</span></span>](xlgethwnd.md)
  
[<span data-ttu-id="91dd9-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="91dd9-119">xlGetInst</span></span>](xlgetinst.md)
  
[<span data-ttu-id="91dd9-120">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="91dd9-120">xlGetInstPtr</span></span>](xlgetinstptr.md)
  
[<span data-ttu-id="91dd9-121">xlGetName</span><span class="sxs-lookup"><span data-stu-id="91dd9-121">xlGetName</span></span>](xlgetname.md)
  
[<span data-ttu-id="91dd9-122">xlRunningOnCluster</span><span class="sxs-lookup"><span data-stu-id="91dd9-122">xlRunningOnCluster</span></span>](xlrunningoncluster.md)
  
[<span data-ttu-id="91dd9-123">gleich xlSet</span><span class="sxs-lookup"><span data-stu-id="91dd9-123">xlSet</span></span>](xlset.md)
  
[<span data-ttu-id="91dd9-124">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="91dd9-124">xlSheetId</span></span>](xlsheetid.md)
  
[<span data-ttu-id="91dd9-125">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="91dd9-125">xlSheetNm</span></span>](xlsheetnm.md)
  
[<span data-ttu-id="91dd9-126">xlStack</span><span class="sxs-lookup"><span data-stu-id="91dd9-126">xlStack</span></span>](xlstack.md)
  
[<span data-ttu-id="91dd9-127">xlUDF</span><span class="sxs-lookup"><span data-stu-id="91dd9-127">xlUDF</span></span>](xludf.md)
  
## <a name="see-also"></a><span data-ttu-id="91dd9-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91dd9-128">See also</span></span>



[<span data-ttu-id="91dd9-129">C-API-R�ckruf funktioniert Excel4 Excel12</span><span class="sxs-lookup"><span data-stu-id="91dd9-129">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)

