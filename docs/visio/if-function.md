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
description: Gibt valueiftrue zurück, wenn logicalexpression true ist. Andernfalls wird valueiffalse zurückgegeben.
ms.openlocfilehash: 8780bd3dd5ded1a950a5bf3f79333687f3b6843c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405471"
---
# <a name="if-function"></a><span data-ttu-id="c79cc-104">IF Function</span><span class="sxs-lookup"><span data-stu-id="c79cc-104">IF Function</span></span>

<span data-ttu-id="c79cc-105">Gibt  _valueiftrue_ zurück,  _wenn logicalexpression_ true ist.</span><span class="sxs-lookup"><span data-stu-id="c79cc-105">Returns  _valueiftrue_ if  _logicalexpression_ is TRUE.</span></span> <span data-ttu-id="c79cc-106">Andernfalls wird _valueiffalse zurückgegeben._</span><span class="sxs-lookup"><span data-stu-id="c79cc-106">Otherwise, it returns  _valueiffalse_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c79cc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c79cc-107">Syntax</span></span>

<span data-ttu-id="c79cc-108">IF(\*\* *logicalexpression* \*\*, \*\* *valueiftrue* \*\*, \*\* *valueiffalse* \*\* )</span><span class="sxs-lookup"><span data-stu-id="c79cc-108">IF(\*\* *logicalexpression* \*\*, \*\* *valueiftrue* \*\*, \*\* *valueiffalse* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c79cc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c79cc-109">Parameters</span></span>

|<span data-ttu-id="c79cc-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="c79cc-110">**Name**</span></span>|<span data-ttu-id="c79cc-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="c79cc-111">**Required/Optional**</span></span>|<span data-ttu-id="c79cc-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="c79cc-112">**Data Type**</span></span>|<span data-ttu-id="c79cc-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c79cc-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c79cc-114">_logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="c79cc-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="c79cc-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c79cc-115">Required</span></span>  <br/> |<span data-ttu-id="c79cc-116">**String**</span><span class="sxs-lookup"><span data-stu-id="c79cc-116">**String**</span></span> <br/> |<span data-ttu-id="c79cc-117">Der auszuwertende Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="c79cc-117">Expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="c79cc-118">_valueiftrue_</span><span class="sxs-lookup"><span data-stu-id="c79cc-118">_valueiftrue_</span></span> <br/> |<span data-ttu-id="c79cc-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c79cc-119">Required</span></span>  <br/> |<span data-ttu-id="c79cc-120">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="c79cc-120">**Varies**</span></span> <br/> |<span data-ttu-id="c79cc-121">Der Wert, der zurückzukehren  _ist, wenn logicalexpression_ true ist.</span><span class="sxs-lookup"><span data-stu-id="c79cc-121">Value to return if  _logicalexpression_ is true.</span></span>  <br/> |
| <span data-ttu-id="c79cc-122">_valueiffalse_</span><span class="sxs-lookup"><span data-stu-id="c79cc-122">_valueiffalse_</span></span> <br/> |<span data-ttu-id="c79cc-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c79cc-123">Required</span></span>  <br/> |<span data-ttu-id="c79cc-124">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="c79cc-124">**Varies**</span></span> <br/> | <span data-ttu-id="c79cc-125">Der Wert, der zurückzukehren  _ist, wenn logicalexpression_ false ist.</span><span class="sxs-lookup"><span data-stu-id="c79cc-125">Value to return if  _logicalexpression_ is false.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c79cc-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c79cc-126">Return value</span></span>

<span data-ttu-id="c79cc-127">Variiert</span><span class="sxs-lookup"><span data-stu-id="c79cc-127">Varies</span></span>
  
## <a name="example"></a><span data-ttu-id="c79cc-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c79cc-128">Example</span></span>

<span data-ttu-id="c79cc-129">IF(Height \> 1.25 in,5,7)</span><span class="sxs-lookup"><span data-stu-id="c79cc-129">IF(Height \> 1.25 in,5,7)</span></span>
  
<span data-ttu-id="c79cc-p103">Gibt 5 zurück, wenn die Höhe des Shapes größer als 3 cm ist. Gibt 7 zurück, wenn die Höhe des Shapes kleiner als oder gleich 3 cm ist.</span><span class="sxs-lookup"><span data-stu-id="c79cc-p103">Returns 5 if the shape's height is greater than 1.25 inches. Returns 7 if the shape's height is less than or equal to 1.25 inches.</span></span>
  

