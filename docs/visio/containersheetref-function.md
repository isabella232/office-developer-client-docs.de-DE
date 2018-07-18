---
title: CONTAINERSHEETREF-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bbdb2dea-4f75-b73e-a98a-0031f34dff2c
description: Gibt eine Blattreferenz auf den angegebenen Container zurück, der das Shape enthält.
ms.openlocfilehash: 6392b4c1a2652f1a831dc585c0be0f430a5ffe0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796734"
---
# <a name="containersheetref-function"></a><span data-ttu-id="686ec-103">CONTAINERSHEETREF Function</span><span class="sxs-lookup"><span data-stu-id="686ec-103">CONTAINERSHEETREF Function</span></span>

<span data-ttu-id="686ec-104">Gibt eine Blattreferenz auf den angegebenen Container zurück, der das Shape enthält.</span><span class="sxs-lookup"><span data-stu-id="686ec-104">Returns a sheet reference to the specified container that contains the shape.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="686ec-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="686ec-105">Version Information</span></span>

<span data-ttu-id="686ec-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="686ec-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="686ec-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="686ec-107">Syntax</span></span>

<span data-ttu-id="686ec-108">CONTAINERSHEETREF (** *Index* ** ** *[, Kategorie]* **)</span><span class="sxs-lookup"><span data-stu-id="686ec-108">CONTAINERSHEETREF(** *index* ** ** *[, category]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="686ec-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="686ec-109">Parameters</span></span>

|<span data-ttu-id="686ec-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="686ec-110">**Name**</span></span>|<span data-ttu-id="686ec-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="686ec-111">**Required/Optional**</span></span>|<span data-ttu-id="686ec-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="686ec-112">**Data Type**</span></span>|<span data-ttu-id="686ec-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="686ec-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="686ec-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="686ec-114">_index_</span></span> <br/> |<span data-ttu-id="686ec-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="686ec-115">Required</span></span>  <br/> |<span data-ttu-id="686ec-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="686ec-116">**Integer**</span></span> <br/> |<span data-ttu-id="686ec-p101">Der auf 1 basierende Index des Containers. Weitere Informationen finden Sie unter "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="686ec-p101">The 1-based index of the container. See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="686ec-119">_category_</span><span class="sxs-lookup"><span data-stu-id="686ec-119">_category_</span></span> <br/> |<span data-ttu-id="686ec-120">Optional</span><span class="sxs-lookup"><span data-stu-id="686ec-120">Optional</span></span>  <br/> |<span data-ttu-id="686ec-121">**String**</span><span class="sxs-lookup"><span data-stu-id="686ec-121">**String**</span></span> <br/> |<span data-ttu-id="686ec-p102">Die Kategorie des Containers. Weitere Informationen finden Sie unter "Anmerkungen".</span><span class="sxs-lookup"><span data-stu-id="686ec-p102">The category of the container. See Remarks for more information.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="686ec-124">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="686ec-124">Return value</span></span>

<span data-ttu-id="686ec-125">ShapeSheet-Referenz</span><span class="sxs-lookup"><span data-stu-id="686ec-125">ShapeSheet reference</span></span>
  
## <a name="remarks"></a><span data-ttu-id="686ec-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="686ec-126">Remarks</span></span>

<span data-ttu-id="686ec-127">Der Index eines Containers wird basierend auf der Z-Reihenfolge der Container von vorne nach hinten berechnet.</span><span class="sxs-lookup"><span data-stu-id="686ec-127">The index of a container is calculated based on the z-order of containers from front to back.</span></span>
  
 <span data-ttu-id="686ec-128">*Kategorien* sind benutzerdefinierte Zeichenfolgen, die Sie verwenden können, die Shapes kategorisieren.</span><span class="sxs-lookup"><span data-stu-id="686ec-128">*Categories*  are user-defined strings that you can use to categorize shapes.</span></span> <span data-ttu-id="686ec-129">Sie können die Kategorien in der Zelle User.msvShapeCategories im ShapeSheet für ein Shape definieren.</span><span class="sxs-lookup"><span data-stu-id="686ec-129">You can define categories in the User.msvShapeCategories cell in the ShapeSheet for a shape.</span></span> <span data-ttu-id="686ec-130">Sie können mehrere Kategorien für ein Shape definieren, indem Sie die Kategorien durch ein Semikolon voneinander getrennt.</span><span class="sxs-lookup"><span data-stu-id="686ec-130">You can define multiple categories for a shape by separating the categories with semi-colons.</span></span> 
  
<span data-ttu-id="686ec-131">Wenn das Shape nicht Element eines Containers ist, oder wenn es keinen Container gibt, der sowohl der angegebenen Indexnummer als auch der Kategorie entspricht, gibt CONTAINERSHEETREF #REF! zurück.</span><span class="sxs-lookup"><span data-stu-id="686ec-131">If the shape is not a member of a container, or if there is no container that matches both the specified index number and the category, CONTAINERSHEETREF returns #REF!.</span></span>
  
## <a name="example"></a><span data-ttu-id="686ec-132">Beispiel</span><span class="sxs-lookup"><span data-stu-id="686ec-132">Example</span></span>

<span data-ttu-id="686ec-133">CONTAINERSHEETREF(1)!Height</span><span class="sxs-lookup"><span data-stu-id="686ec-133">CONTAINERSHEETREF(1)!Height</span></span> 
  
<span data-ttu-id="686ec-134">Gibt den Wert in der Zelle Height des Containers zurück, der sich auf der Seite, auf der sich das Shape befindet, am weitesten vorne befindet.</span><span class="sxs-lookup"><span data-stu-id="686ec-134">Returns the value in the Height cell of the container that is most forward on the page to which the shape belongs.</span></span> 
  

