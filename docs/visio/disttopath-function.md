---
title: DISTTOPATH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: Gibt den kürzesten Abstand von dem von den angegebenen Koordinaten festgelegten Punkt zu einem Punkt im Pfad zurück.
ms.openlocfilehash: 5727b24739705d3e562150c48fe77f7ad6eedb57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332690"
---
# <a name="disttopath-function"></a><span data-ttu-id="323c5-103">DISTTOPATH Function</span><span class="sxs-lookup"><span data-stu-id="323c5-103">DISTTOPATH Function</span></span>

<span data-ttu-id="323c5-104">Gibt den kürzesten Abstand von dem von den angegebenen Koordinaten festgelegten Punkt zu einem Punkt im Pfad zurück.</span><span class="sxs-lookup"><span data-stu-id="323c5-104">Returns the shortest distance from the point represented by the specified coordinates to a point on the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="323c5-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="323c5-105">Version Information</span></span>

<span data-ttu-id="323c5-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="323c5-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="323c5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="323c5-107">Syntax</span></span>

<span data-ttu-id="323c5-108">DISTTOPATH (\* \* *section* \* \*, \* \* *x* \* \*, \* \* *y* \* \*)</span><span class="sxs-lookup"><span data-stu-id="323c5-108">DISTTOPATH(\*\* *section* \*\*, \*\* *x* \*\*, \*\* *y* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="323c5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="323c5-109">Parameters</span></span>

|<span data-ttu-id="323c5-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="323c5-110">**Name**</span></span>|<span data-ttu-id="323c5-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="323c5-111">**Required/Optional**</span></span>|<span data-ttu-id="323c5-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="323c5-112">**Data Type**</span></span>|<span data-ttu-id="323c5-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="323c5-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="323c5-114">_section_</span><span class="sxs-lookup"><span data-stu-id="323c5-114">_section_</span></span> <br/> |<span data-ttu-id="323c5-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="323c5-115">Required</span></span>  <br/> |<span data-ttu-id="323c5-116">**String**</span><span class="sxs-lookup"><span data-stu-id="323c5-116">**String**</span></span> <br/> |<span data-ttu-id="323c5-117">Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).</span><span class="sxs-lookup"><span data-stu-id="323c5-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="323c5-118">_x_</span><span class="sxs-lookup"><span data-stu-id="323c5-118">_x_</span></span> <br/> |<span data-ttu-id="323c5-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="323c5-119">Required</span></span>  <br/> |<span data-ttu-id="323c5-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="323c5-120">**Double**</span></span> <br/> |<span data-ttu-id="323c5-121">Die _x_-Koordinate des Punkts.</span><span class="sxs-lookup"><span data-stu-id="323c5-121">The  _x_-coordinate of the point.</span></span>  <br/> |
| <span data-ttu-id="323c5-122">_y_</span><span class="sxs-lookup"><span data-stu-id="323c5-122">_y_</span></span> <br/> |<span data-ttu-id="323c5-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="323c5-123">Required</span></span>  <br/> |<span data-ttu-id="323c5-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="323c5-124">**Double**</span></span> <br/> |<span data-ttu-id="323c5-125">Die _y_-Koordinate des Punkts.</span><span class="sxs-lookup"><span data-stu-id="323c5-125">The  _y_-coordinate of the point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="323c5-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="323c5-126">Return value</span></span>

 <span data-ttu-id="323c5-127">**Double**</span><span class="sxs-lookup"><span data-stu-id="323c5-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="323c5-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="323c5-128">Remarks</span></span>

<span data-ttu-id="323c5-129">Microsoft Visio gibt #REF!</span><span class="sxs-lookup"><span data-stu-id="323c5-129">Microsoft Visio returns #REF!</span></span> <span data-ttu-id="323c5-130">Wenn _section_ nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="323c5-130">if  _section_ does not exist.</span></span> 
  
<span data-ttu-id="323c5-131">Der Rückgabewert ist positiv, wenn sich der Punkt links der Laufrichtung befindet; er ist positiv, wenn sich der Punkt rechts der Laufrichtung befindet.</span><span class="sxs-lookup"><span data-stu-id="323c5-131">The returned value is positive if the point is to the left of the direction of travel; it is negative if the point is to the right of the direction of travel.</span></span>
  

