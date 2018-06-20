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
description: Wertet einen der beiden Ausdrücke abhängig vom Wert des Status aus.
ms.openlocfilehash: 2cfdf23986a06dcc109106bd50a1a38e5af91313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798369"
---
# <a name="userui-function"></a><span data-ttu-id="227ee-103">USERUI-Funktion</span><span class="sxs-lookup"><span data-stu-id="227ee-103">USERUI Function</span></span>

<span data-ttu-id="227ee-104">Wertet einen der beiden Ausdrücke abhängig vom Wert des _Status_aus.</span><span class="sxs-lookup"><span data-stu-id="227ee-104">Evaluates one of the two expressions depending on the value of  _state_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="227ee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="227ee-105">Syntax</span></span>

<span data-ttu-id="227ee-106">USERUI (** *Zustand* **, ** *Standardausdruck aus* **, ** *BenutzerAusdruck ausgewertet* **)</span><span class="sxs-lookup"><span data-stu-id="227ee-106">USERUI(** *state* **, ** *defaultexpression* **, ** *userexpression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="227ee-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="227ee-107">Parameters</span></span>

|<span data-ttu-id="227ee-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="227ee-108">**Name**</span></span>|<span data-ttu-id="227ee-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="227ee-109">**Required/Optional**</span></span>|<span data-ttu-id="227ee-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="227ee-110">**Data Type**</span></span>|<span data-ttu-id="227ee-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="227ee-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="227ee-112">_state_</span><span class="sxs-lookup"><span data-stu-id="227ee-112">_state_</span></span> <br/> |<span data-ttu-id="227ee-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="227ee-113">Required</span></span>  <br/> |<span data-ttu-id="227ee-114">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="227ee-114">**Boolean**</span></span> <br/> |<span data-ttu-id="227ee-115">Bestimmt, welche der auszuwertende Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="227ee-115">Determines which expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="227ee-116">_Standardausdruck aus_</span><span class="sxs-lookup"><span data-stu-id="227ee-116">_defaultexpression_</span></span> <br/> |<span data-ttu-id="227ee-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="227ee-117">Required</span></span>  <br/> |<span data-ttu-id="227ee-118">**String**</span><span class="sxs-lookup"><span data-stu-id="227ee-118">**String**</span></span> <br/> |<span data-ttu-id="227ee-119">Der Standardausdruck.</span><span class="sxs-lookup"><span data-stu-id="227ee-119">The default expression.</span></span>  <br/> |
| <span data-ttu-id="227ee-120">_BenutzerAusdruck ausgewertet_</span><span class="sxs-lookup"><span data-stu-id="227ee-120">_userexpression_</span></span> <br/> |<span data-ttu-id="227ee-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="227ee-121">Required</span></span>  <br/> |<span data-ttu-id="227ee-122">**String**</span><span class="sxs-lookup"><span data-stu-id="227ee-122">**String**</span></span> <br/> |<span data-ttu-id="227ee-123">Ein Ausdruck, der vom Benutzer bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="227ee-123">An expression supplied by the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="227ee-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="227ee-124">Remarks</span></span>

<span data-ttu-id="227ee-125">Wenn _Zustand_ 0 ist, wertet die USERUI-Funktion den _Standardausdruck aus_.</span><span class="sxs-lookup"><span data-stu-id="227ee-125">If  _state_ is 0, the USERUI function evaluates the  _defaultexpression_.</span></span> <span data-ttu-id="227ee-126">Wenn _Zustand_ 1 ist, wird der _BenutzerAusdruck ausgewertet_.</span><span class="sxs-lookup"><span data-stu-id="227ee-126">If  _state_ is 1, it evaluates the  _userexpression_.</span></span>
  
## <a name="example"></a><span data-ttu-id="227ee-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="227ee-127">Example</span></span>

<span data-ttu-id="227ee-128">USERUI (1, wenn (Breite\>6 Zoll, 6 In, Breite), Breite\*0,75)</span><span class="sxs-lookup"><span data-stu-id="227ee-128">USERUI(1, if(Width\>6in, 6in, Width), Width\*0.75)</span></span> 
  
<span data-ttu-id="227ee-129">Wertet den Ausdruck Breite\*.075 und gibt das Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="227ee-129">Evaluates the expression Width\*.075 and returns the result.</span></span> 
  

