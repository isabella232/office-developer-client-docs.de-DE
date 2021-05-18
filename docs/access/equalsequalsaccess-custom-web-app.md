---
title: Equals(Benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Vergleicht die Gleichheit von zwei Ausdrücken.
ms.openlocfilehash: 8c551e3dbc057433b49bc2558e08feba5ee3d04f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408929"
---
# <a name="equals-access-custom-web-app"></a><span data-ttu-id="40ae5-103">Gleich (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="40ae5-103">Equals (Access custom web app)</span></span>

<span data-ttu-id="40ae5-104">Vergleicht die Gleichheit von zwei Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="40ae5-104">Compares the equality of two expressions.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="40ae5-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="40ae5-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="40ae5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="40ae5-107">Syntax</span></span>

`= (Equals)`

<span data-ttu-id="40ae5-108">*Ausdruck*   =   *Ausdruck*</span><span class="sxs-lookup"><span data-stu-id="40ae5-108">*expression*  =  *expression*</span></span> 
  
<span data-ttu-id="40ae5-109">*expression*  Ein beliebiger gültiger Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="40ae5-109">*expression*  Is any valid expression.</span></span> <span data-ttu-id="40ae5-110">Wenn die Ausdrücke nicht denselben Datentyp haben, muss der Datentyp für einen Ausdruck implizit in den Datentyp des anderen konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="40ae5-110">If the expressions are not of the same data type, the data type for one expression must be implicitly convertible to the data type of the other.</span></span> <span data-ttu-id="40ae5-111">Die Konvertierung ist von den Regeln der Rangfolge der Datentypen abhängig.</span><span class="sxs-lookup"><span data-stu-id="40ae5-111">The conversion depends on the rules of data type precedence.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="40ae5-112">Rückgabetyp</span><span class="sxs-lookup"><span data-stu-id="40ae5-112">Return Type</span></span>

<span data-ttu-id="40ae5-113">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="40ae5-113">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="40ae5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40ae5-114">Remarks</span></span>

<span data-ttu-id="40ae5-115">Wenn Sie zwei NULL-Ausdrücke vergleichen, ist das Ergebnis TRUE.</span><span class="sxs-lookup"><span data-stu-id="40ae5-115">When you compare two NULL expressions, the result is TRUE.</span></span>
  
<span data-ttu-id="40ae5-116">Der Vergleich von NULL mit einem Nicht-NULL-Wert führt immer zu FALSE.</span><span class="sxs-lookup"><span data-stu-id="40ae5-116">Comparing NULL to a non-NULL value always results in FALSE.</span></span>
  

