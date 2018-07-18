---
title: Choose-Funktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: Gibt das Element am angegebenen Index aus einer Liste von Werten zurück.
ms.openlocfilehash: a6db959945bfcfc15993d3979cb9b2b3da0da904
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790197"
---
# <a name="choose-function-access-custom-web-app"></a><span data-ttu-id="0e277-103">Choose-Funktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="0e277-103">Choose function (Access custom web app)</span></span>

<span data-ttu-id="0e277-104">Gibt das Element am angegebenen Index aus einer Liste von Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="0e277-104">Returns the item at the specified index from a list of values.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="0e277-p101">[!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="0e277-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0e277-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e277-107">Syntax</span></span>

<span data-ttu-id="0e277-108">**Wählen Sie aus** (*Indexnummer kann ein*, *Wert*[*Value_n*])</span><span class="sxs-lookup"><span data-stu-id="0e277-108">**Choose** (*IndexNumber*, *Value*, [*Value_n*])</span></span> 
  
<span data-ttu-id="0e277-109">Die **Choose** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="0e277-109">The **Choose** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="0e277-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="0e277-110">**Argument name**</span></span>|<span data-ttu-id="0e277-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="0e277-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="0e277-112">*Indexnummer kann ein*</span><span class="sxs-lookup"><span data-stu-id="0e277-112">*IndexNumber*</span></span>  <br/> |<span data-ttu-id="0e277-113">Ein Integer-Ausdruck, der ein 1-basierter Indexwert in der Liste der folgenden Elemente darstellt.</span><span class="sxs-lookup"><span data-stu-id="0e277-113">An integer expression that represents a 1-based index into the list of the items following it.</span></span>  <br/> |
| <span data-ttu-id="0e277-114">*Wert*</span><span class="sxs-lookup"><span data-stu-id="0e277-114">*Value*</span></span>  <br/> |<span data-ttu-id="0e277-115">Liste der Werte von einem beliebigen Datentyp.</span><span class="sxs-lookup"><span data-stu-id="0e277-115">List of values of any data type.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e277-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e277-116">Remarks</span></span>

<span data-ttu-id="0e277-117">Wenn der angegebenen *Indexnummer kann ein* nicht um eine ganze Zahl ist, wird der Wert auf eine Ganzzahl implizit konvertiert.</span><span class="sxs-lookup"><span data-stu-id="0e277-117">If the provided  *IndexNumber*  is not an integer, then the value is implicitly converted to an integer.</span></span> 
  
<span data-ttu-id="0e277-118">Wenn der Indexwert die Grenzen des Arrays von Werte überschreitet, gibt **Choose** NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="0e277-118">If the index value exceeds the bounds of the array of values, **Choose** returns NULL.</span></span> 
  

