---
title: OR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251476
localization_priority: Normal
ms.assetid: 6c2154fa-4190-0699-61f7-f2bdf87173ec
description: Gibt TRUE (1) zurück, wenn einer der logischen Ausdrücke, die als Parameter übergeben werden, TRUE ist.
ms.openlocfilehash: 175a1c72f5109caca786b823966f07836f4737f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433507"
---
# <a name="or-function"></a><span data-ttu-id="2290d-103">OR Function</span><span class="sxs-lookup"><span data-stu-id="2290d-103">OR Function</span></span>

<span data-ttu-id="2290d-104">Gibt TRUE (1) zurück, wenn einer der logischen Ausdrücke, die als Parameter übergeben werden, TRUE ist.</span><span class="sxs-lookup"><span data-stu-id="2290d-104">Returns TRUE (1) if any of the logical expressions passed as parameters are TRUE.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="2290d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2290d-105">Syntax</span></span>

<span data-ttu-id="2290d-106">OR(\*\* *logicalexpression1* \*\*, \*\* *logicalexpression2* \*\*,..., \*\* *logicalexpressionN* \*\* )</span><span class="sxs-lookup"><span data-stu-id="2290d-106">OR(\*\* *logicalexpression1* \*\*, \*\* *logicalexpression2* \*\*,..., \*\* *logicalexpressionN* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2290d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2290d-107">Parameters</span></span>

|<span data-ttu-id="2290d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2290d-108">**Name**</span></span>|<span data-ttu-id="2290d-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="2290d-109">**Required/Optional**</span></span>|<span data-ttu-id="2290d-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="2290d-110">**Data Type**</span></span>|<span data-ttu-id="2290d-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2290d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2290d-112">_logicalexpression1_</span><span class="sxs-lookup"><span data-stu-id="2290d-112">_logicalexpression1_</span></span> <br/> |<span data-ttu-id="2290d-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2290d-113">Required</span></span>  <br/> |<span data-ttu-id="2290d-114">**String**</span><span class="sxs-lookup"><span data-stu-id="2290d-114">**String**</span></span> <br/> |<span data-ttu-id="2290d-115">Der erste Ausdruck, dessen Wahrheit ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2290d-115">The first expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="2290d-116">_logicalexpression2_</span><span class="sxs-lookup"><span data-stu-id="2290d-116">_logicalexpression2_</span></span> <br/> |<span data-ttu-id="2290d-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2290d-117">Required</span></span>  <br/> |<span data-ttu-id="2290d-118">**String**</span><span class="sxs-lookup"><span data-stu-id="2290d-118">**String**</span></span> <br/> |<span data-ttu-id="2290d-119">Der zweite Ausdruck, dessen Wahrheit ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2290d-119">The second expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="2290d-120">_logicalexpressionN_</span><span class="sxs-lookup"><span data-stu-id="2290d-120">_logicalexpressionN_</span></span> <br/> |<span data-ttu-id="2290d-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2290d-121">Required</span></span>  <br/> |<span data-ttu-id="2290d-122">**String**</span><span class="sxs-lookup"><span data-stu-id="2290d-122">**String**</span></span> <br/> |<span data-ttu-id="2290d-123">Der n-te Ausdruck, dessen Wahrheit ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2290d-123">The Nth expression whose truth you want to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2290d-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2290d-124">Return value</span></span>

<span data-ttu-id="2290d-125">Boolesch</span><span class="sxs-lookup"><span data-stu-id="2290d-125">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2290d-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2290d-126">Remarks</span></span>

<span data-ttu-id="2290d-p101">Ein beliebiger Ausdruck, der einen Wert ungleich Null ergibt, wird als TRUE betrachtet. Wenn alle logischen Ausdrücke den Wert FALSE oder 0 aufweisen, gibt die Funktion FALSE zurück.</span><span class="sxs-lookup"><span data-stu-id="2290d-p101">Any expression that evaluates to a non-zero value is considered TRUE. If all of the logical expressions are FALSE or equal 0, this function returns FALSE.</span></span> 
  
## <a name="example"></a><span data-ttu-id="2290d-129">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2290d-129">Example</span></span>

<span data-ttu-id="2290d-130">OR(Height \> 1,PinX \> 1)</span><span class="sxs-lookup"><span data-stu-id="2290d-130">OR(Height \> 1,PinX \> 1)</span></span> 
  
<span data-ttu-id="2290d-p102">Gibt TRUE (1) zurück, wenn mindestens einer der beiden Ausdrücke TRUE ist. Gibt FALSE (0) zurück, wenn beide Ausdrücke FALSE sind.</span><span class="sxs-lookup"><span data-stu-id="2290d-p102">Returns TRUE (1) if either expression is TRUE. Returns FALSE (0) only if both expressions are FALSE.</span></span> 
  

