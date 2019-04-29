---
title: IF-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251442
localization_priority: Normal
ms.assetid: 66771ad3-0fb3-68ff-81da-d1162d37c05a
description: Gibt Wahrheitsprüfung ungleich zurück, wenn logicive auf TRUE festgelegt ist. Andernfalls wird den sonst zurückgegeben.
ms.openlocfilehash: 8780bd3dd5ded1a950a5bf3f79333687f3b6843c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405471"
---
# <a name="if-function"></a><span data-ttu-id="4217e-104">IF Function</span><span class="sxs-lookup"><span data-stu-id="4217e-104">IF Function</span></span>

<span data-ttu-id="4217e-105">Gibt _Wahrheitsprüfung ungleich_ zurück __ , wenn logicive auf true festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4217e-105">Returns  _valueiftrue_ if  _logicalexpression_ is TRUE.</span></span> <span data-ttu-id="4217e-106">Andernfalls wird _den sonst_zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4217e-106">Otherwise, it returns  _valueiffalse_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="4217e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4217e-107">Syntax</span></span>

<span data-ttu-id="4217e-108">IF (\* \* *logischer* \* \*, \* \* *Wahrheitsprüfung ungleich* \* \*, \* \* *den sonst* \* \*)</span><span class="sxs-lookup"><span data-stu-id="4217e-108">IF(\*\* *logicalexpression* \*\*, \*\* *valueiftrue* \*\*, \*\* *valueiffalse* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4217e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4217e-109">Parameters</span></span>

|<span data-ttu-id="4217e-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="4217e-110">**Name**</span></span>|<span data-ttu-id="4217e-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="4217e-111">**Required/Optional**</span></span>|<span data-ttu-id="4217e-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="4217e-112">**Data Type**</span></span>|<span data-ttu-id="4217e-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4217e-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4217e-114">_Logik_</span><span class="sxs-lookup"><span data-stu-id="4217e-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="4217e-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4217e-115">Required</span></span>  <br/> |<span data-ttu-id="4217e-116">**String**</span><span class="sxs-lookup"><span data-stu-id="4217e-116">**String**</span></span> <br/> |<span data-ttu-id="4217e-117">Der auszuwertende Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="4217e-117">Expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="4217e-118">_Wahrheitsprüfung ungleich_</span><span class="sxs-lookup"><span data-stu-id="4217e-118">_valueiftrue_</span></span> <br/> |<span data-ttu-id="4217e-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4217e-119">Required</span></span>  <br/> |<span data-ttu-id="4217e-120">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="4217e-120">**Varies**</span></span> <br/> |<span data-ttu-id="4217e-121">Wert, der zurückgegeben werden soll, wenn die _Logik_ true ist.</span><span class="sxs-lookup"><span data-stu-id="4217e-121">Value to return if  _logicalexpression_ is true.</span></span>  <br/> |
| <span data-ttu-id="4217e-122">_den sonst_</span><span class="sxs-lookup"><span data-stu-id="4217e-122">_valueiffalse_</span></span> <br/> |<span data-ttu-id="4217e-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4217e-123">Required</span></span>  <br/> |<span data-ttu-id="4217e-124">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="4217e-124">**Varies**</span></span> <br/> | <span data-ttu-id="4217e-125">Wert, der zurück __ gegeben werden soll, wenn logisches false ist.</span><span class="sxs-lookup"><span data-stu-id="4217e-125">Value to return if  _logicalexpression_ is false.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4217e-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4217e-126">Return value</span></span>

<span data-ttu-id="4217e-127">Variiert</span><span class="sxs-lookup"><span data-stu-id="4217e-127">Varies</span></span>
  
## <a name="example"></a><span data-ttu-id="4217e-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4217e-128">Example</span></span>

<span data-ttu-id="4217e-129">IF (Höhe \> 1,25 in, 5, 7)</span><span class="sxs-lookup"><span data-stu-id="4217e-129">IF(Height \> 1.25 in,5,7)</span></span>
  
<span data-ttu-id="4217e-130">Gibt 5 zurück, wenn die Höhe des Shapes größer als 3 cm ist.</span><span class="sxs-lookup"><span data-stu-id="4217e-130">Returns 5 if the shape's height is greater than 1.25 inches.</span></span> <span data-ttu-id="4217e-131">Gibt 7 zurück, wenn die Höhe des Shapes kleiner als oder gleich 3 cm ist.</span><span class="sxs-lookup"><span data-stu-id="4217e-131">Returns 7 if the shape's height is less than or equal to 1.25 inches.</span></span>
  

