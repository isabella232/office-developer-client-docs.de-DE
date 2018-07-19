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
description: Gibt WertWennWahr zurück, wenn Logicalexpression wahr ist. Andernfalls ihn Funktion Valueiffalse zurück.
ms.openlocfilehash: 55938e8bd78c02badb98f90665c5c26cdd70f3b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797187"
---
# <a name="if-function"></a><span data-ttu-id="eec86-104">IF Function</span><span class="sxs-lookup"><span data-stu-id="eec86-104">IF Function</span></span>

<span data-ttu-id="eec86-105">Gibt _WertWennWahr_ zurück, wenn _Logicalexpression_ wahr ist.</span><span class="sxs-lookup"><span data-stu-id="eec86-105">Returns  _valueiftrue_ if  _logicalexpression_ is TRUE.</span></span> <span data-ttu-id="eec86-106">Andernfalls ihn _Funktion Valueiffalse zurück_.</span><span class="sxs-lookup"><span data-stu-id="eec86-106">Otherwise, it returns  _valueiffalse_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="eec86-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="eec86-107">Syntax</span></span>

<span data-ttu-id="eec86-108">IF (** *Logicalexpression* **, ** *WertWennWahr* **, ** *Funktion Valueiffalse zurück* **)</span><span class="sxs-lookup"><span data-stu-id="eec86-108">IF(** *logicalexpression* **, ** *valueiftrue* **, ** *valueiffalse* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="eec86-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="eec86-109">Parameters</span></span>

|<span data-ttu-id="eec86-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="eec86-110">**Name**</span></span>|<span data-ttu-id="eec86-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="eec86-111">**Required/Optional**</span></span>|<span data-ttu-id="eec86-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="eec86-112">**Data Type**</span></span>|<span data-ttu-id="eec86-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="eec86-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="eec86-114">_logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="eec86-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="eec86-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="eec86-115">Required</span></span>  <br/> |<span data-ttu-id="eec86-116">**String**</span><span class="sxs-lookup"><span data-stu-id="eec86-116">**String**</span></span> <br/> |<span data-ttu-id="eec86-117">Der auszuwertende Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="eec86-117">Expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="eec86-118">_WertWennWahr_</span><span class="sxs-lookup"><span data-stu-id="eec86-118">_valueiftrue_</span></span> <br/> |<span data-ttu-id="eec86-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="eec86-119">Required</span></span>  <br/> |<span data-ttu-id="eec86-120">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="eec86-120">**Varies**</span></span> <br/> |<span data-ttu-id="eec86-121">Der zurückzugebende Wert, wenn _Logicalexpression_ wahr ist.</span><span class="sxs-lookup"><span data-stu-id="eec86-121">Value to return if  _logicalexpression_ is true.</span></span>  <br/> |
| <span data-ttu-id="eec86-122">_Funktion Valueiffalse zurück_</span><span class="sxs-lookup"><span data-stu-id="eec86-122">_valueiffalse_</span></span> <br/> |<span data-ttu-id="eec86-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="eec86-123">Required</span></span>  <br/> |<span data-ttu-id="eec86-124">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="eec86-124">**Varies**</span></span> <br/> | <span data-ttu-id="eec86-125">Der zurückzugebende Wert, wenn _Logicalexpression_ falsch ist.</span><span class="sxs-lookup"><span data-stu-id="eec86-125">Value to return if  _logicalexpression_ is false.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="eec86-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eec86-126">Return value</span></span>

<span data-ttu-id="eec86-127">Varies</span><span class="sxs-lookup"><span data-stu-id="eec86-127">Varies</span></span>
  
## <a name="example"></a><span data-ttu-id="eec86-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="eec86-128">Example</span></span>

<span data-ttu-id="eec86-129">IF (Höhe \> 1,25 in, 5, 7)</span><span class="sxs-lookup"><span data-stu-id="eec86-129">IF(Height \> 1.25 in,5,7)</span></span>
  
<span data-ttu-id="eec86-p103">Gibt 5 zurück, wenn die Höhe des Shapes größer als 3 cm ist. Gibt 7 zurück, wenn die Höhe des Shapes kleiner als oder gleich 3 cm ist.</span><span class="sxs-lookup"><span data-stu-id="eec86-p103">Returns 5 if the shape's height is greater than 1.25 inches. Returns 7 if the shape's height is less than or equal to 1.25 inches.</span></span>
  

