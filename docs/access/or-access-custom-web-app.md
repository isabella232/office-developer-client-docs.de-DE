---
title: OR (Benutzerdefinierte Web-App access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Kombiniert zwei Bedingungen. Gibt TRUE zurück, wenn eine der beiden Bedingungen true ist.
ms.openlocfilehash: ffa605d2403c5aa8396d89f78d0bb7dd11343540
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414760"
---
# <a name="or-access-custom-web-app"></a><span data-ttu-id="5224e-104">OR (Benutzerdefinierte Web-App access)</span><span class="sxs-lookup"><span data-stu-id="5224e-104">OR (Access custom web app)</span></span>

<span data-ttu-id="5224e-105">Kombiniert zwei Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="5224e-105">Combines two conditions.</span></span> <span data-ttu-id="5224e-106">Gibt TRUE zurück, wenn eine der beiden Bedingungen true ist.</span><span class="sxs-lookup"><span data-stu-id="5224e-106">Returns TRUE when either of the two conditions is true.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="5224e-p103">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="5224e-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5224e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5224e-109">Syntax</span></span>

 <span data-ttu-id="5224e-110">*BooleanExpression* **oder** *BooleanExpression*</span><span class="sxs-lookup"><span data-stu-id="5224e-110">*BooleanExpression* **Or** *BooleanExpression*</span></span> 
  
<span data-ttu-id="5224e-111">Der **Operator Or** verwendet das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="5224e-111">The **Or** operator uses the following argument.</span></span> 
  
|<span data-ttu-id="5224e-112">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="5224e-112">**Argument name**</span></span>|<span data-ttu-id="5224e-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5224e-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5224e-114">*BooleanExpression*</span><span class="sxs-lookup"><span data-stu-id="5224e-114">*BooleanExpression*</span></span>  <br/> |<span data-ttu-id="5224e-115">Jeder gültige Ausdruck, der TRUE oder FALSE zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="5224e-115">Any valid expression that returns TRUE or FALSE.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5224e-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5224e-116">Remarks</span></span>

<span data-ttu-id="5224e-117">Wenn mehrere logische Operatoren in einer  Anweisung verwendet werden, werden Or-Operatoren nach **And-Operatoren** ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="5224e-117">When more than one logical operator is used in a statement, **Or** operators are evaluated after **And** operators.</span></span> <span data-ttu-id="5224e-118">Sie können die Reihenfolge der Auswertung jedoch mithilfe von Klammern ändern.</span><span class="sxs-lookup"><span data-stu-id="5224e-118">However, you can change the order of evaluation by using parentheses.</span></span> 
  
<span data-ttu-id="5224e-119">In der folgenden Tabelle ist das Ergebnis des Operators **Or** aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5224e-119">The following table shows the result of the **Or** operator.</span></span> 
  
||<span data-ttu-id="5224e-120">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="5224e-120">**TRUE**</span></span>|<span data-ttu-id="5224e-121">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="5224e-121">**FALSE**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5224e-122">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="5224e-122">**TRUE**</span></span> <br/> |<span data-ttu-id="5224e-123">TRUE</span><span class="sxs-lookup"><span data-stu-id="5224e-123">TRUE</span></span>  <br/> |<span data-ttu-id="5224e-124">TRUE</span><span class="sxs-lookup"><span data-stu-id="5224e-124">TRUE</span></span>  <br/> |
|<span data-ttu-id="5224e-125">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="5224e-125">**FALSE**</span></span> <br/> |<span data-ttu-id="5224e-126">TRUE</span><span class="sxs-lookup"><span data-stu-id="5224e-126">TRUE</span></span>  <br/> |<span data-ttu-id="5224e-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="5224e-127">FALSE</span></span>  <br/> |
   

