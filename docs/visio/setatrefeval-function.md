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
description: Wird im set_expression der SETATREF-Funktion verwendet, um anzugeben, dass set_expression ausgewertet werden soll, bevor sie dem Referenzparameter in SETATREF zugewiesen werden.
ms.openlocfilehash: a11a7485e04d4deb31e9497476bb198d675bc68f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432982"
---
# <a name="setatrefeval-function"></a><span data-ttu-id="2005f-103">SETATREFEVAL Function</span><span class="sxs-lookup"><span data-stu-id="2005f-103">SETATREFEVAL Function</span></span>

<span data-ttu-id="2005f-104">Wird im _set_expression_ der SETATREF-Funktion verwendet,  um anzugeben, dass set_expression ausgewertet werden  soll, bevor dem Referenzparameter in SETATREF zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="2005f-104">Used in the  _set_expression_ parameter of the SETATREF function to indicate that  _set_expression_ should be evaluated before assigning to the  _reference_ parameter in SETATREF.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2005f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2005f-105">Syntax</span></span>

<span data-ttu-id="2005f-106">SETATREFEVAL(\*\* *expr* \*\* )</span><span class="sxs-lookup"><span data-stu-id="2005f-106">SETATREFEVAL(\*\* *expr* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2005f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2005f-107">Parameters</span></span>

|<span data-ttu-id="2005f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2005f-108">**Name**</span></span>|<span data-ttu-id="2005f-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="2005f-109">**Required/Optional**</span></span>|<span data-ttu-id="2005f-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="2005f-110">**Data Type**</span></span>|<span data-ttu-id="2005f-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2005f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2005f-112">_expr_</span><span class="sxs-lookup"><span data-stu-id="2005f-112">_expr_</span></span> <br/> |<span data-ttu-id="2005f-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2005f-113">Required</span></span>  <br/> |<span data-ttu-id="2005f-114">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="2005f-114">**Varies**</span></span> <br/> | <span data-ttu-id="2005f-115">Ein Ausdruck, der ausgewertet wird, wenn die SETATREF-Funktion  _set_expression_ zu einer anderen Zelle umleite.</span><span class="sxs-lookup"><span data-stu-id="2005f-115">An expression that is evaluated when the SETATREF function redirects  _set_expression_ to another cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2005f-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2005f-116">Remarks</span></span>

<span data-ttu-id="2005f-117">Beim Zuweisen des *set_expression-Parameters* der SETATREF-Funktion zu einer zelle, auf  die verwiesen wird, schreibt Microsoft Visio standardmäßig set_expression in die Zelle als Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="2005f-117">When assigning the  *set_expression*  parameter of the SETATREF function to a referenced cell, Microsoft Visio writes  *set_expression*  to the cell as an expression by default.</span></span> <span data-ttu-id="2005f-118">Wenn jedoch ein Teil des *set_expression-Parameters* von der SETATREFEVAL-Funktion umschlossen wird, wertet Visio den Ausdruck aus und ersetzt die SETATREFEVAL-Funktion durch ihr Ergebnis, bevor der SETATREF-Ausdruck aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="2005f-118">However, if any portion of the  *set_expression*  parameter is wrapped by the SETATREFEVAL function, Visio evaluates the expression and replaces the SETATREFEVAL function with its result prior to resolving the SETATREF expression.</span></span> 
  
## <a name="example"></a><span data-ttu-id="2005f-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2005f-119">Example</span></span>

<span data-ttu-id="2005f-120">Ein Beispiel finden Sie unter [SETATREF](setatref-function.md)-Funktion.</span><span class="sxs-lookup"><span data-stu-id="2005f-120">For an example, see the [SETATREF](setatref-function.md) function.</span></span> 
  

