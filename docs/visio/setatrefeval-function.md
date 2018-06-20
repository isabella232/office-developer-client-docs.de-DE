---
title: SETATREFEVAL-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1042150
localization_priority: Normal
ms.assetid: b3f3a0a0-7b14-0b71-d247-ada81b93b66b
description: In der Set_expression-Parameter der SETATREF-Funktion verwendet, um anzugeben, dass diese Set_expression berechnet werden soll, bevor Sie Reference-Parameter in SETATREF zuweisen.
ms.openlocfilehash: 0826ef9ca91e180576c0b2611452758b238736a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797989"
---
# <a name="setatrefeval-function"></a><span data-ttu-id="98f85-103">SETATREFEVAL-Funktion</span><span class="sxs-lookup"><span data-stu-id="98f85-103">SETATREFEVAL Function</span></span>

<span data-ttu-id="98f85-104">In der _Set_expression_ -Parameter der SETATREF-Funktion verwendet, um anzugeben, dass _Set_expression_ vor dem Zuweisen zum _Reference_ -Parameter in SETATREF ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="98f85-104">Used in the  _set_expression_ parameter of the SETATREF function to indicate that  _set_expression_ should be evaluated before assigning to the  _reference_ parameter in SETATREF.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="98f85-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="98f85-105">Syntax</span></span>

<span data-ttu-id="98f85-106">SETATREFEVAL (** *Ausdr* **)</span><span class="sxs-lookup"><span data-stu-id="98f85-106">SETATREFEVAL(** *expr* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="98f85-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="98f85-107">Parameters</span></span>

|<span data-ttu-id="98f85-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="98f85-108">**Name**</span></span>|<span data-ttu-id="98f85-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="98f85-109">**Required/Optional**</span></span>|<span data-ttu-id="98f85-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="98f85-110">**Data Type**</span></span>|<span data-ttu-id="98f85-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="98f85-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="98f85-112">_expr_</span><span class="sxs-lookup"><span data-stu-id="98f85-112">_expr_</span></span> <br/> |<span data-ttu-id="98f85-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="98f85-113">Required</span></span>  <br/> |<span data-ttu-id="98f85-114">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="98f85-114">**Varies**</span></span> <br/> | <span data-ttu-id="98f85-115">Ein Ausdruck, der ausgewertet wird, wenn die SETATREF-Funktion _Set_expression_ in eine andere Zelle umleitet.</span><span class="sxs-lookup"><span data-stu-id="98f85-115">An expression that is evaluated when the SETATREF function redirects  _set_expression_ to another cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98f85-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="98f85-116">Remarks</span></span>

<span data-ttu-id="98f85-117">Beim Zuweisen des *Set_expression* -Parameters der SETATREF-Funktion zu einer referenzierten Zelle wird *Set_expression* von Microsoft Visio eine Standard auf die Zelle geschrieben.</span><span class="sxs-lookup"><span data-stu-id="98f85-117">When assigning the  *set_expression*  parameter of the SETATREF function to a referenced cell, Microsoft Visio writes  *set_expression*  to the cell as an expression by default.</span></span> <span data-ttu-id="98f85-118">Wenn ein Teil von *Set_expression* -Parameters durch die SETATREFEVAL-Funktion umbrochen wird, Visio wertet den Ausdruck und ersetzt die SETATREFEVAL-Funktion durch das Ergebnis vor dem Auflösen des SETATREF-Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="98f85-118">However, if any portion of the  *set_expression*  parameter is wrapped by the SETATREFEVAL function, Visio evaluates the expression and replaces the SETATREFEVAL function with its result prior to resolving the SETATREF expression.</span></span> 
  
## <a name="example"></a><span data-ttu-id="98f85-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="98f85-119">Example</span></span>

<span data-ttu-id="98f85-120">Ein Beispiel finden Sie unter der [SETATREF](setatref-function.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="98f85-120">For an example, see the [SETATREF](setatref-function.md) function.</span></span> 
  

