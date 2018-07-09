---
title: Ist gleich (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Vergleicht die Gleichheit zweier Ausdrücke.
ms.openlocfilehash: efdd06a1735190d63c13c4df8230e1d29d71c1dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790216"
---
# <a name="equals-access-custom-web-app"></a><span data-ttu-id="386ac-103">Ist gleich (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="386ac-103">Equals (Access custom web app)</span></span>

<span data-ttu-id="386ac-104">Vergleicht die Gleichheit zweier Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="386ac-104">Compares the equality of two expressions.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="386ac-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="386ac-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="386ac-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="386ac-107">Syntax</span></span>

`= (Equals)`

<span data-ttu-id="386ac-108">*Ausdruck*  =  *Ausdruck*</span><span class="sxs-lookup"><span data-stu-id="386ac-108">*expression*  =  *expression*</span></span> 
  
<span data-ttu-id="386ac-109">*Ausdruck*  Ist ein beliebiger gültiger Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="386ac-109">*expression*  Is any valid expression.</span></span> <span data-ttu-id="386ac-110">Wenn die Ausdrücke nicht den gleichen Datentyp aufweisen, muss der Datentyp für einen Ausdruck implizit in den Datentyp des anderen.</span><span class="sxs-lookup"><span data-stu-id="386ac-110">If the expressions are not of the same data type, the data type for one expression must be implicitly convertible to the data type of the other.</span></span> <span data-ttu-id="386ac-111">Die Konvertierung, abhängig von den Regeln der Rangfolge der Datentypen.</span><span class="sxs-lookup"><span data-stu-id="386ac-111">The conversion depends on the rules of data type precedence.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="386ac-112">Rückgabetyp</span><span class="sxs-lookup"><span data-stu-id="386ac-112">Return Type</span></span>

<span data-ttu-id="386ac-113">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="386ac-113">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="386ac-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="386ac-114">Remarks</span></span>

<span data-ttu-id="386ac-115">Beim Vergleichen von zwei NULL-Ausdrücken ist das Ergebnis TRUE.</span><span class="sxs-lookup"><span data-stu-id="386ac-115">When you compare two NULL expressions, the result is TRUE.</span></span>
  
<span data-ttu-id="386ac-116">FALSE führt NULL immer mit einem NULL Wert zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="386ac-116">Comparing NULL to a non-NULL value always results in FALSE.</span></span>
  

