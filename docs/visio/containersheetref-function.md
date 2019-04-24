---
title: CONTAINERSHEETREF-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bbdb2dea-4f75-b73e-a98a-0031f34dff2c
description: Gibt eine Blattreferenz auf den angegebenen Container zurück, der das Shape enthält.
ms.openlocfilehash: 473d8c0b81ecc568c1d4f3a3b3a885e1ceb4e00d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318984"
---
# <a name="containersheetref-function"></a><span data-ttu-id="d6ba4-103">CONTAINERSHEETREF Function</span><span class="sxs-lookup"><span data-stu-id="d6ba4-103">CONTAINERSHEETREF Function</span></span>

<span data-ttu-id="d6ba4-104">Gibt eine Blattreferenz auf den angegebenen Container zurück, der das Shape enthält.</span><span class="sxs-lookup"><span data-stu-id="d6ba4-104">Returns a sheet reference to the specified container that contains the shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="d6ba4-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="d6ba4-105">Version Information</span></span>

<span data-ttu-id="d6ba4-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="d6ba4-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d6ba4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6ba4-107">Syntax</span></span>

<span data-ttu-id="d6ba4-108">CONTAINERSHEETREF (\* \* *Index* \* \* \* \* \* *[, Category]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="d6ba4-108">CONTAINERSHEETREF(\*\* *index* \*\* \*\* *[, category]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d6ba4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6ba4-109">Parameters</span></span>

|<span data-ttu-id="d6ba4-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="d6ba4-110">**Name**</span></span>|<span data-ttu-id="d6ba4-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="d6ba4-111">**Required/Optional**</span></span>|<span data-ttu-id="d6ba4-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="d6ba4-112">**Data Type**</span></span>|<span data-ttu-id="d6ba4-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6ba4-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d6ba4-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="d6ba4-114">_index_</span></span> <br/> |<span data-ttu-id="d6ba4-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d6ba4-115">Required</span></span>  <br/> |<span data-ttu-id="d6ba4-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="d6ba4-116">**Integer**</span></span> <br/> |<span data-ttu-id="d6ba4-117">Der auf 1 basierende Index des Containers.</span><span class="sxs-lookup"><span data-stu-id="d6ba4-117">The 1-based index of the container.</span></span> <span data-ttu-id="d6ba4-118">Weitere Informationen finden Sie unter "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="d6ba4-118">See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="d6ba4-119">_Kategorie_</span><span class="sxs-lookup"><span data-stu-id="d6ba4-119">_category_</span></span> <br/> |<span data-ttu-id="d6ba4-120">Optional</span><span class="sxs-lookup"><span data-stu-id="d6ba4-120">Optional</span></span>  <br/> |<span data-ttu-id="d6ba4-121">**String**</span><span class="sxs-lookup"><span data-stu-id="d6ba4-121">**String**</span></span> <br/> |<span data-ttu-id="d6ba4-122">Die Kategorie des Containers.</span><span class="sxs-lookup"><span data-stu-id="d6ba4-122">The category of the container.</span></span> <span data-ttu-id="d6ba4-123">Weitere Informationen finden Sie unter "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="d6ba4-123">See Remarks for more information.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d6ba4-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6ba4-124">Return value</span></span>

<span data-ttu-id="d6ba4-125">ShapeSheet-Referenz</span><span class="sxs-lookup"><span data-stu-id="d6ba4-125">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d6ba4-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6ba4-126">Remarks</span></span>

<span data-ttu-id="d6ba4-127">Der Index eines Containers wird basierend auf der Z-Reihenfolge der Container von vorne nach hinten berechnet.</span><span class="sxs-lookup"><span data-stu-id="d6ba4-127">The index of a container is calculated based on the z-order of containers from front to back.</span></span>
  
 <span data-ttu-id="d6ba4-128">*Kategorien* sind benutzerdefinierte Zeichenfolgen, die Sie verwenden können, um Shapes zu kategorisieren.</span><span class="sxs-lookup"><span data-stu-id="d6ba4-128">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="d6ba4-129">Kategorien können in der Zelle User.msvShapeCategories im ShapeSheet eines Shapes definiert werden.</span><span class="sxs-lookup"><span data-stu-id="d6ba4-129">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="d6ba4-130">Sie können mehrere Kategorien für ein Shape definieren, indem Sie die Kategorien durch Semikolons trennen.</span><span class="sxs-lookup"><span data-stu-id="d6ba4-130">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  
<span data-ttu-id="d6ba4-131">Wenn das Shape nicht Element eines Containers ist, oder wenn es keinen Container gibt, der sowohl der angegebenen Indexnummer als auch der Kategorie entspricht, gibt CONTAINERSHEETREF #REF! zurück.</span><span class="sxs-lookup"><span data-stu-id="d6ba4-131">If the shape is not a member of a container, or if there is no container that matches both the specified index number and the category, CONTAINERSHEETREF returns #REF!.</span></span>
  
## <a name="example"></a><span data-ttu-id="d6ba4-132">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d6ba4-132">Example</span></span>

<span data-ttu-id="d6ba4-133">CONTAINERSHEETREF (1)! Höhe</span><span class="sxs-lookup"><span data-stu-id="d6ba4-133">CONTAINERSHEETREF(1)!Height</span></span> 
  
<span data-ttu-id="d6ba4-134">Gibt den Wert in der Zelle Height des Containers zurück, der sich auf der Seite, auf der sich das Shape befindet, am weitesten vorne befindet.</span><span class="sxs-lookup"><span data-stu-id="d6ba4-134">Returns the value in the Height cell of the container that is most forward on the page to which the shape belongs.</span></span> 
  

