---
title: EXP-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09385b75-ec0e-4dde-b9c3-9ade4a7a2b74
description: Gibt den exponentiellen Wert des angegebenen Ausdrucks.
ms.openlocfilehash: 9c4929a25da6a8eec5984f9e9a1a6695a049614d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790181"
---
# <a name="exp-function-access-custom-web-app"></a><span data-ttu-id="ac8ba-103">EXP-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="ac8ba-103">Exp Function (Access custom web app)</span></span>

<span data-ttu-id="ac8ba-104">Gibt den exponentiellen Wert des angegebenen Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="ac8ba-104">Returns the exponential value of the specified expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ac8ba-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="ac8ba-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ac8ba-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac8ba-107">Syntax</span></span>

 <span data-ttu-id="ac8ba-108">**EXP** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="ac8ba-108">**Exp** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="ac8ba-109">Die **Exp** -Funktion enthält das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="ac8ba-109">The **Exp** function contains the following argument.</span></span> 
  
|<span data-ttu-id="ac8ba-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="ac8ba-110">**Argument name**</span></span>|<span data-ttu-id="ac8ba-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="ac8ba-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ac8ba-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="ac8ba-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="ac8ba-113">Ein Ausdruck vom Typ Double-Wert oder einen Typ, der implizit in Double-Wert konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ac8ba-113">An expression of type Double or of a type that can be implicitly converted to Double.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac8ba-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ac8ba-114">Remarks</span></span>

<span data-ttu-id="ac8ba-115">Die Konstante **e** (.. 2.718281) ist die Basis natürlicher Logarithmen.</span><span class="sxs-lookup"><span data-stu-id="ac8ba-115">The constant **e** (2.718281…), is the base of natural logarithms.</span></span> 
  
<span data-ttu-id="ac8ba-116">Der Exponent einer Zahl ist die Konstante **e** potenziert mit der Zahl.</span><span class="sxs-lookup"><span data-stu-id="ac8ba-116">The exponent of a number is the constant **e** raised to the power of the number.</span></span> <span data-ttu-id="ac8ba-117">Beispielsweise **Exp** (1.0) = e ^ 1,0 = 2.71828182845905 und **Exp** (10) = e ^ 10 = 22026.4657948067.</span><span class="sxs-lookup"><span data-stu-id="ac8ba-117">For example **Exp** (1.0) = e^1.0 = 2.71828182845905 and **Exp** (10) = e^10 = 22026.4657948067.</span></span> 
  
<span data-ttu-id="ac8ba-118">Ist die Anzahl der exponentielle den natürlichen Logarithmus einer Zahl selbst: **Exp** (LOG (n)) = n.</span><span class="sxs-lookup"><span data-stu-id="ac8ba-118">The exponential of the natural logarithm of a number is the number itself: **Exp** (LOG (n)) = n.</span></span> <span data-ttu-id="ac8ba-119">Und den natürlichen Logarithmus von den exponentiellen Wert einer Zahl ist die Zahl selbst: LOG (**Exp** (n)) = n.</span><span class="sxs-lookup"><span data-stu-id="ac8ba-119">And the natural logarithm of the exponential of a number is the number itself: LOG (**Exp** (n)) = n.</span></span> 
  

