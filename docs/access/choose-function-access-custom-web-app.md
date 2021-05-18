---
title: Choose-Funktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: Gibt das Element am angegebenen Index aus einer Liste von Werten zurück.
ms.openlocfilehash: e44655b9c2f4055f1f3dc57befa8adc6884c43b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414116"
---
# <a name="choose-function-access-custom-web-app"></a><span data-ttu-id="296d9-103">Choose-Funktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="296d9-103">Choose function (Access custom web app)</span></span>

<span data-ttu-id="296d9-104">Gibt das Element am angegebenen Index aus einer Liste von Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="296d9-104">Returns the item at the specified index from a list of values.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="296d9-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="296d9-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="296d9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="296d9-107">Syntax</span></span>

<span data-ttu-id="296d9-108">**Choose** (*IndexNumber*, *Value*, [*Value_n*])</span><span class="sxs-lookup"><span data-stu-id="296d9-108">**Choose** (*IndexNumber*, *Value*, [*Value_n*])</span></span> 
  
<span data-ttu-id="296d9-109">Die **Choose-Funktion** enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="296d9-109">The **Choose** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="296d9-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="296d9-110">**Argument name**</span></span>|<span data-ttu-id="296d9-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="296d9-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="296d9-112">*IndexNumber*</span><span class="sxs-lookup"><span data-stu-id="296d9-112">*IndexNumber*</span></span>  <br/> |<span data-ttu-id="296d9-113">Ein ganzzahliger Ausdruck, der einen 1-basierten Index in der Liste der folgenden Elemente darstellt.</span><span class="sxs-lookup"><span data-stu-id="296d9-113">An integer expression that represents a 1-based index into the list of the items following it.</span></span>  <br/> |
| <span data-ttu-id="296d9-114">*Wert*</span><span class="sxs-lookup"><span data-stu-id="296d9-114">*Value*</span></span>  <br/> |<span data-ttu-id="296d9-115">Liste der Werte eines beliebigen Datentyps.</span><span class="sxs-lookup"><span data-stu-id="296d9-115">List of values of any data type.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="296d9-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="296d9-116">Remarks</span></span>

<span data-ttu-id="296d9-117">Wenn die  *bereitgestellte IndexNumber*  keine ganze Zahl ist, wird der Wert implizit in eine ganze Zahl konvertiert.</span><span class="sxs-lookup"><span data-stu-id="296d9-117">If the provided  *IndexNumber*  is not an integer, then the value is implicitly converted to an integer.</span></span> 
  
<span data-ttu-id="296d9-118">Wenn der Indexwert die Grenzen des Wertearrays überschreitet, gibt **Choose NULL** zurück.</span><span class="sxs-lookup"><span data-stu-id="296d9-118">If the index value exceeds the bounds of the array of values, **Choose** returns NULL.</span></span> 
  

