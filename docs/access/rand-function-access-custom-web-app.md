---
title: Rand-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6390b325-025e-4546-bb19-1cd1c45ceb5a
description: Gibt eine pseudozufällige Zahl zwischen 0 und 1 zurück.
ms.openlocfilehash: ed0f9991b2b1d9553d6d45524d6b1e4e5321ea7e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790341"
---
# <a name="rand-function-access-custom-web-app"></a><span data-ttu-id="d484e-103">Rand-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="d484e-103">Rand Function (Access custom web app)</span></span>

<span data-ttu-id="d484e-104">Gibt eine pseudozufällige Zahl zwischen 0 und 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="d484e-104">Returns a pseudo-random number between 0 and 1.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="d484e-p101"> Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="d484e-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/de-de/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d484e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d484e-107">Syntax</span></span>

 <span data-ttu-id="d484e-108">**Rand** ([ *Seed* ])</span><span class="sxs-lookup"><span data-stu-id="d484e-108">**Rand** ( [  *Seed*  ])</span></span> 
  
<span data-ttu-id="d484e-109">Die **Rand** -Funktion enthält das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="d484e-109">The **Rand** function contains the following argument.</span></span> 
  
|<span data-ttu-id="d484e-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="d484e-110">**Argument name**</span></span>|<span data-ttu-id="d484e-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="d484e-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d484e-112">*Seed*</span><span class="sxs-lookup"><span data-stu-id="d484e-112">*Seed*</span></span>  <br/> |<span data-ttu-id="d484e-113">Ein Integer-Ausdruck, der den Ausgangswert bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="d484e-113">An integer expression that gives the seed value.</span></span> <span data-ttu-id="d484e-114">Wenn der *Ausgangswert* nicht angegeben wird, wird ein Startwert nach dem Zufallsprinzip zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="d484e-114">If  *Seed*  is not specified, a seed value is assigned at random.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d484e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d484e-115">Remarks</span></span>

<span data-ttu-id="d484e-116">Sich wiederholende Aufrufe der **Rand** -Funktion mit demselben Startwert zurückgegeben die gleichen Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="d484e-116">Repetitive calls of the **Rand** function with the same seed return the same results.</span></span> 
  

