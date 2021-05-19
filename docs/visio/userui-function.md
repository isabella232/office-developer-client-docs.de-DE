---
title: USERUI-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251511
localization_priority: Normal
ms.assetid: c01dd938-677c-b2ba-8f56-4638e7e988fd
description: Wertet einen der beiden Ausdrücke abhängig vom Wert des Zustands aus.
ms.openlocfilehash: 544bb2b19dc610591afc78c407301098fac9c7c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420346"
---
# <a name="userui-function"></a><span data-ttu-id="b04b9-103">USERUI Function</span><span class="sxs-lookup"><span data-stu-id="b04b9-103">USERUI Function</span></span>

<span data-ttu-id="b04b9-104">Wertet einen der beiden Ausdrücke abhängig vom Wert des Status _aus._</span><span class="sxs-lookup"><span data-stu-id="b04b9-104">Evaluates one of the two expressions depending on the value of  _state_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b04b9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b04b9-105">Syntax</span></span>

<span data-ttu-id="b04b9-106">USERUI(\*\* *state* \*\*, \*\* *defaultexpression* \*\*, \*\* *userexpression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="b04b9-106">USERUI(\*\* *state* \*\*, \*\* *defaultexpression* \*\*, \*\* *userexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b04b9-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b04b9-107">Parameters</span></span>

|<span data-ttu-id="b04b9-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="b04b9-108">**Name**</span></span>|<span data-ttu-id="b04b9-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="b04b9-109">**Required/Optional**</span></span>|<span data-ttu-id="b04b9-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="b04b9-110">**Data Type**</span></span>|<span data-ttu-id="b04b9-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b04b9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b04b9-112">_state_</span><span class="sxs-lookup"><span data-stu-id="b04b9-112">_state_</span></span> <br/> |<span data-ttu-id="b04b9-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b04b9-113">Required</span></span>  <br/> |<span data-ttu-id="b04b9-114">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="b04b9-114">**Boolean**</span></span> <br/> |<span data-ttu-id="b04b9-115">Bestimmt, welcher Ausdruck ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b04b9-115">Determines which expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="b04b9-116">_defaultexpression_</span><span class="sxs-lookup"><span data-stu-id="b04b9-116">_defaultexpression_</span></span> <br/> |<span data-ttu-id="b04b9-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b04b9-117">Required</span></span>  <br/> |<span data-ttu-id="b04b9-118">**String**</span><span class="sxs-lookup"><span data-stu-id="b04b9-118">**String**</span></span> <br/> |<span data-ttu-id="b04b9-119">Der Standardausdruck.</span><span class="sxs-lookup"><span data-stu-id="b04b9-119">The default expression.</span></span>  <br/> |
| <span data-ttu-id="b04b9-120">_userexpression_</span><span class="sxs-lookup"><span data-stu-id="b04b9-120">_userexpression_</span></span> <br/> |<span data-ttu-id="b04b9-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b04b9-121">Required</span></span>  <br/> |<span data-ttu-id="b04b9-122">**String**</span><span class="sxs-lookup"><span data-stu-id="b04b9-122">**String**</span></span> <br/> |<span data-ttu-id="b04b9-123">Ein vom Benutzer bereitgestellter Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="b04b9-123">An expression supplied by the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b04b9-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b04b9-124">Remarks</span></span>

<span data-ttu-id="b04b9-125">Wenn _der Status_ 0 ist, wertet die USERUI-Funktion den _defaultexpression aus._</span><span class="sxs-lookup"><span data-stu-id="b04b9-125">If  _state_ is 0, the USERUI function evaluates the  _defaultexpression_.</span></span> <span data-ttu-id="b04b9-126">Wenn _der Status_ 1 ist, wird der _userexpression ausgewertet._</span><span class="sxs-lookup"><span data-stu-id="b04b9-126">If  _state_ is 1, it evaluates the  _userexpression_.</span></span>
  
## <a name="example"></a><span data-ttu-id="b04b9-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b04b9-127">Example</span></span>

<span data-ttu-id="b04b9-128">USERUI(1, if(Width \> 6in, 6in, Width), Width \* 0.75)</span><span class="sxs-lookup"><span data-stu-id="b04b9-128">USERUI(1, if(Width\>6in, 6in, Width), Width\*0.75)</span></span> 
  
<span data-ttu-id="b04b9-129">Ausgewertet den Ausdruck Width \* .075 und gibt das Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="b04b9-129">Evaluates the expression Width\*.075 and returns the result.</span></span> 
  

