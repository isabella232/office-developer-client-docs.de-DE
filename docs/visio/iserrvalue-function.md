---
title: ISERRVALUE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251453
localization_priority: Normal
ms.assetid: c7feec6f-f47a-60ee-b056-7b2dc51ed9a9
description: 'Gibt TRUE zurück, wenn der Wert von cellreference den Fehlertyp #VALUE, wobei ein Argument in der Formel den falschen Typ aufweist. Die ISERRVALUE-Funktion wird in logischen Ausdrücken verwendet, die auf eine andere Zelle verweisen.'
ms.openlocfilehash: 62058522dc8a2387aec9867e4892da740aba9b44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317885"
---
# <a name="iserrvalue-function"></a><span data-ttu-id="ec2a9-104">ISERRVALUE Function</span><span class="sxs-lookup"><span data-stu-id="ec2a9-104">ISERRVALUE Function</span></span>

<span data-ttu-id="ec2a9-105">Gibt TRUE zurück, wenn der Wert von _cellreference_ den fehlertyp #VALUE, wobei ein Argument in der Formel den falschen Typ aufweist.</span><span class="sxs-lookup"><span data-stu-id="ec2a9-105">Returns TRUE if the value of  _cellreference_ is error type #VALUE, where an argument in the formula is the wrong type.</span></span> <span data-ttu-id="ec2a9-106">Die ISERRVALUE-Funktion wird in logischen Ausdrücken verwendet, die auf eine andere Zelle verweisen.</span><span class="sxs-lookup"><span data-stu-id="ec2a9-106">The ISERRVALUE function is used in logical expressions that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ec2a9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec2a9-107">Syntax</span></span>

<span data-ttu-id="ec2a9-108">ISERRVALUE (\* \* *cellreference* \* \*)</span><span class="sxs-lookup"><span data-stu-id="ec2a9-108">ISERRVALUE(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ec2a9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec2a9-109">Parameters</span></span>

|<span data-ttu-id="ec2a9-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="ec2a9-110">**Name**</span></span>|<span data-ttu-id="ec2a9-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="ec2a9-111">**Required/Optional**</span></span>|<span data-ttu-id="ec2a9-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="ec2a9-112">**Data Type**</span></span>|<span data-ttu-id="ec2a9-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ec2a9-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ec2a9-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="ec2a9-114">_cellreference_</span></span> <br/> |<span data-ttu-id="ec2a9-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ec2a9-115">Required</span></span>  <br/> |<span data-ttu-id="ec2a9-116">**String**</span><span class="sxs-lookup"><span data-stu-id="ec2a9-116">**String**</span></span> <br/> |<span data-ttu-id="ec2a9-117">Bezug auf eine Zelle.</span><span class="sxs-lookup"><span data-stu-id="ec2a9-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec2a9-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec2a9-118">Remarks</span></span>

<span data-ttu-id="ec2a9-p103">Die Entwurfzellen A bis D geben keinen Fehler vom Typ #WERT! zurück, da ihre Formeln in der gleichen Zeichenfolge Zahlen und Buchstaben enthalten können. Die Zellen X und Y dürfen nur Zahlen enthalten.</span><span class="sxs-lookup"><span data-stu-id="ec2a9-p103">Scratch cells A through D won't return a #VALUE! error because the formula can contain numbers and letters in the same string. Cells X and Y must contain numbers only.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="ec2a9-122">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ec2a9-122">Example 1</span></span>

|<span data-ttu-id="ec2a9-123">**Cell**</span><span class="sxs-lookup"><span data-stu-id="ec2a9-123">**Cell**</span></span>|<span data-ttu-id="ec2a9-124">**Formula**</span><span class="sxs-lookup"><span data-stu-id="ec2a9-124">**Formula**</span></span>|<span data-ttu-id="ec2a9-125">**Zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="ec2a9-125">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ec2a9-126">Scratch. x1</span><span class="sxs-lookup"><span data-stu-id="ec2a9-126">Scratch.X1</span></span>  <br/> |<span data-ttu-id="ec2a9-127">="Haus"</span><span class="sxs-lookup"><span data-stu-id="ec2a9-127">= "House"</span></span>  <br/> |<span data-ttu-id="ec2a9-128">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="ec2a9-128">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="ec2a9-129">Scratch. a1</span><span class="sxs-lookup"><span data-stu-id="ec2a9-129">Scratch.A1</span></span>  <br/> |<span data-ttu-id="ec2a9-130">= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="ec2a9-130">= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)</span></span>  <br/> |<span data-ttu-id="ec2a9-131">2</span><span class="sxs-lookup"><span data-stu-id="ec2a9-131">2</span></span>  <br/> |
   
<span data-ttu-id="ec2a9-p104">Gibt 2 zurück, da der zurückgegebene Wert den Fehlertyp #WERT! aufweist und der Ausdruck Microsoft Visio anweist, statt des Fehlers eine 2 zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="ec2a9-p104">Returns 2 because the value returned is a #VALUE! error, and the expression instructs Microsoft Visio to return a 2 in place of the error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ec2a9-134">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ec2a9-134">Example 2</span></span>

|<span data-ttu-id="ec2a9-135">**Cell**</span><span class="sxs-lookup"><span data-stu-id="ec2a9-135">**Cell**</span></span>|<span data-ttu-id="ec2a9-136">**Formula**</span><span class="sxs-lookup"><span data-stu-id="ec2a9-136">**Formula**</span></span>|<span data-ttu-id="ec2a9-137">**Zurückgegebener Wert**</span><span class="sxs-lookup"><span data-stu-id="ec2a9-137">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ec2a9-138">Scratch. a1</span><span class="sxs-lookup"><span data-stu-id="ec2a9-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="ec2a9-139">="5 + 7"</span><span class="sxs-lookup"><span data-stu-id="ec2a9-139">="5 + 7"</span></span>  <br/> |<span data-ttu-id="ec2a9-140">5 + 7</span><span class="sxs-lookup"><span data-stu-id="ec2a9-140">5 + 7</span></span>  <br/> |
|<span data-ttu-id="ec2a9-141">Scratch. B1</span><span class="sxs-lookup"><span data-stu-id="ec2a9-141">Scratch.B1</span></span>  <br/> |<span data-ttu-id="ec2a9-142">= If (ISERRVALUE(Scratch.A1),2,Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="ec2a9-142">=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)</span></span>  <br/> |<span data-ttu-id="ec2a9-143">5 + 7</span><span class="sxs-lookup"><span data-stu-id="ec2a9-143">5 + 7</span></span>  <br/> |
   
<span data-ttu-id="ec2a9-p105">Gibt 12 zurück, da der zurückgegebene Wert nicht den Fehlertyp #WERT! aufweist und der Ausdruck Visio anweist, den Wert der ursprünglichen Zelle zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="ec2a9-p105">Returns 12 because the value returned is not a #VALUE! error, and the expression instructs Visio to return the value of the original cell.</span></span>
  

