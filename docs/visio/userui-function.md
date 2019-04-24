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
description: Wertet einen der beiden Ausdrücke in Abhängigkeit vom Wert von State aus.
ms.openlocfilehash: 544bb2b19dc610591afc78c407301098fac9c7c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331325"
---
# <a name="userui-function"></a><span data-ttu-id="aeeaf-103">USERUI Function</span><span class="sxs-lookup"><span data-stu-id="aeeaf-103">USERUI Function</span></span>

<span data-ttu-id="aeeaf-104">Wertet einen der beiden Ausdrücke in Abhängigkeit vom Wert von _State_aus.</span><span class="sxs-lookup"><span data-stu-id="aeeaf-104">Evaluates one of the two expressions depending on the value of  _state_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="aeeaf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aeeaf-105">Syntax</span></span>

<span data-ttu-id="aeeaf-106">USERUI (\* \* *Status* \* \*, \* \* *Standardwert* \* \*, \* \* *Benutzertyp* \* \*)</span><span class="sxs-lookup"><span data-stu-id="aeeaf-106">USERUI(\*\* *state* \*\*, \*\* *defaultexpression* \*\*, \*\* *userexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="aeeaf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="aeeaf-107">Parameters</span></span>

|<span data-ttu-id="aeeaf-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="aeeaf-108">**Name**</span></span>|<span data-ttu-id="aeeaf-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="aeeaf-109">**Required/Optional**</span></span>|<span data-ttu-id="aeeaf-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="aeeaf-110">**Data Type**</span></span>|<span data-ttu-id="aeeaf-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aeeaf-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="aeeaf-112">_state_</span><span class="sxs-lookup"><span data-stu-id="aeeaf-112">_state_</span></span> <br/> |<span data-ttu-id="aeeaf-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="aeeaf-113">Required</span></span>  <br/> |<span data-ttu-id="aeeaf-114">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="aeeaf-114">**Boolean**</span></span> <br/> |<span data-ttu-id="aeeaf-115">Bestimmt, welcher Ausdruck ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="aeeaf-115">Determines which expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="aeeaf-116">_DEFAULTAusdruck_</span><span class="sxs-lookup"><span data-stu-id="aeeaf-116">_defaultexpression_</span></span> <br/> |<span data-ttu-id="aeeaf-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="aeeaf-117">Required</span></span>  <br/> |<span data-ttu-id="aeeaf-118">**String**</span><span class="sxs-lookup"><span data-stu-id="aeeaf-118">**String**</span></span> <br/> |<span data-ttu-id="aeeaf-119">Der Standardausdruck.</span><span class="sxs-lookup"><span data-stu-id="aeeaf-119">The default expression.</span></span>  <br/> |
| <span data-ttu-id="aeeaf-120">_UserForm_</span><span class="sxs-lookup"><span data-stu-id="aeeaf-120">_userexpression_</span></span> <br/> |<span data-ttu-id="aeeaf-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="aeeaf-121">Required</span></span>  <br/> |<span data-ttu-id="aeeaf-122">**String**</span><span class="sxs-lookup"><span data-stu-id="aeeaf-122">**String**</span></span> <br/> |<span data-ttu-id="aeeaf-123">Ein vom Benutzer bereitgestellter Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="aeeaf-123">An expression supplied by the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aeeaf-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aeeaf-124">Remarks</span></span>

<span data-ttu-id="aeeaf-125">Wenn _Status_ 0 ist, wertet die USERUI-Funktion den _Standard_Ausdruck aus.</span><span class="sxs-lookup"><span data-stu-id="aeeaf-125">If  _state_ is 0, the USERUI function evaluates the  _defaultexpression_.</span></span> <span data-ttu-id="aeeaf-126">Wenn _Status_ 1 ist, wird die _Benutzer_Ausdruck ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="aeeaf-126">If  _state_ is 1, it evaluates the  _userexpression_.</span></span>
  
## <a name="example"></a><span data-ttu-id="aeeaf-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="aeeaf-127">Example</span></span>

<span data-ttu-id="aeeaf-128">USERUI (1, if (Breite\>6in, 6in, Breite), Breite\*0,75)</span><span class="sxs-lookup"><span data-stu-id="aeeaf-128">USERUI(1, if(Width\>6in, 6in, Width), Width\*0.75)</span></span> 
  
<span data-ttu-id="aeeaf-129">Wertet den Ausdruck\*Width. 075 und gibt das Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="aeeaf-129">Evaluates the expression Width\*.075 and returns the result.</span></span> 
  

