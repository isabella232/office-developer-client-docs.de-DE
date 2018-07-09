---
title: ODER (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Kombiniert zwei mögliche Ursachen. Gibt TRUE zurück, wenn eine der beiden folgenden Bedingungen zutrifft.
ms.openlocfilehash: 8ccf4a12644f45e80756f72013d42310fece07fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790330"
---
# <a name="or-access-custom-web-app"></a><span data-ttu-id="1d54d-104">ODER (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="1d54d-104">OR (Access custom web app)</span></span>

<span data-ttu-id="1d54d-105">Kombiniert zwei mögliche Ursachen.</span><span class="sxs-lookup"><span data-stu-id="1d54d-105">Combines two conditions.</span></span> <span data-ttu-id="1d54d-106">Gibt TRUE zurück, wenn eine der beiden folgenden Bedingungen zutrifft.</span><span class="sxs-lookup"><span data-stu-id="1d54d-106">Returns TRUE when either of the two conditions is true.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="1d54d-p103">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="1d54d-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1d54d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d54d-109">Syntax</span></span>

 <span data-ttu-id="1d54d-110">*Boolescher Ausdruck* **Oder** *Boolescher Ausdruck*</span><span class="sxs-lookup"><span data-stu-id="1d54d-110">*BooleanExpression* **Or** *BooleanExpression*</span></span> 
  
<span data-ttu-id="1d54d-111">Der **oder** -Operator verwendet das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="1d54d-111">The **Or** operator uses the following argument.</span></span> 
  
|<span data-ttu-id="1d54d-112">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="1d54d-112">**Argument name**</span></span>|<span data-ttu-id="1d54d-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="1d54d-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="1d54d-114">*Boolescher Ausdruck*</span><span class="sxs-lookup"><span data-stu-id="1d54d-114">*BooleanExpression*</span></span>  <br/> |<span data-ttu-id="1d54d-115">Ein beliebiger gültiger Ausdruck, der TRUE oder FALSE zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1d54d-115">Any valid expression that returns TRUE or FALSE.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d54d-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1d54d-116">Remarks</span></span>

<span data-ttu-id="1d54d-117">Wenn mehr als ein logischer Operator in einer Anweisung verwendet wird, werden nach **und** Operatoren **oder** Operatoren ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="1d54d-117">When more than one logical operator is used in a statement, **Or** operators are evaluated after **And** operators.</span></span> <span data-ttu-id="1d54d-118">Jedoch können Sie die Reihenfolge der Auswertung ändern, indem Sie Klammern verwenden.</span><span class="sxs-lookup"><span data-stu-id="1d54d-118">However, you can change the order of evaluation by using parentheses.</span></span> 
  
<span data-ttu-id="1d54d-119">Die folgende Tabelle zeigt das Ergebnis des Operators **oder** .</span><span class="sxs-lookup"><span data-stu-id="1d54d-119">The following table shows the result of the **Or** operator.</span></span> 
  
||<span data-ttu-id="1d54d-120">**"TRUE"**</span><span class="sxs-lookup"><span data-stu-id="1d54d-120">**TRUE**</span></span>|<span data-ttu-id="1d54d-121">**"FALSE"**</span><span class="sxs-lookup"><span data-stu-id="1d54d-121">**FALSE**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1d54d-122">**"TRUE"**</span><span class="sxs-lookup"><span data-stu-id="1d54d-122">**TRUE**</span></span> <br/> |<span data-ttu-id="1d54d-123">TRUE</span><span class="sxs-lookup"><span data-stu-id="1d54d-123">TRUE</span></span>  <br/> |<span data-ttu-id="1d54d-124">TRUE</span><span class="sxs-lookup"><span data-stu-id="1d54d-124">TRUE</span></span>  <br/> |
|<span data-ttu-id="1d54d-125">**"FALSE"**</span><span class="sxs-lookup"><span data-stu-id="1d54d-125">**FALSE**</span></span> <br/> |<span data-ttu-id="1d54d-126">TRUE</span><span class="sxs-lookup"><span data-stu-id="1d54d-126">TRUE</span></span>  <br/> |<span data-ttu-id="1d54d-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="1d54d-127">FALSE</span></span>  <br/> |
   

