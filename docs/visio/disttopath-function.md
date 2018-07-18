---
title: DISTTOPATH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: Gibt den kürzesten Abstand von dem von den angegebenen Koordinaten festgelegten Punkt zu einem Punkt im Pfad zurück.
ms.openlocfilehash: 227fe860de2e3683b5d7d3e5f9313d1e2e31b2d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796878"
---
# <a name="disttopath-function"></a><span data-ttu-id="546e4-103">DISTTOPATH Function</span><span class="sxs-lookup"><span data-stu-id="546e4-103">DISTTOPATH Function</span></span>

<span data-ttu-id="546e4-104">Gibt den kürzesten Abstand von dem von den angegebenen Koordinaten festgelegten Punkt zu einem Punkt im Pfad zurück.</span><span class="sxs-lookup"><span data-stu-id="546e4-104">Returns the shortest distance from the point represented by the specified coordinates to a point on the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="546e4-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="546e4-105">Version Information</span></span>

<span data-ttu-id="546e4-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="546e4-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="546e4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="546e4-107">Syntax</span></span>

<span data-ttu-id="546e4-108">DISTTOPATH (** *Abschnitt* **, ** *X* **, ** *y* **)</span><span class="sxs-lookup"><span data-stu-id="546e4-108">DISTTOPATH(** *section* **, ** *x* **, ** *y* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="546e4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="546e4-109">Parameters</span></span>

|<span data-ttu-id="546e4-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="546e4-110">**Name**</span></span>|<span data-ttu-id="546e4-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="546e4-111">**Required/Optional**</span></span>|<span data-ttu-id="546e4-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="546e4-112">**Data Type**</span></span>|<span data-ttu-id="546e4-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="546e4-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="546e4-114">_section_</span><span class="sxs-lookup"><span data-stu-id="546e4-114">_section_</span></span> <br/> |<span data-ttu-id="546e4-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="546e4-115">Required</span></span>  <br/> |<span data-ttu-id="546e4-116">**String**</span><span class="sxs-lookup"><span data-stu-id="546e4-116">**String**</span></span> <br/> |<span data-ttu-id="546e4-117">Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).</span><span class="sxs-lookup"><span data-stu-id="546e4-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="546e4-118">_x_</span><span class="sxs-lookup"><span data-stu-id="546e4-118">_x_</span></span> <br/> |<span data-ttu-id="546e4-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="546e4-119">Required</span></span>  <br/> |<span data-ttu-id="546e4-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="546e4-120">**Double**</span></span> <br/> |<span data-ttu-id="546e4-121">Die _X_-Koordinate des Punkts.</span><span class="sxs-lookup"><span data-stu-id="546e4-121">The  _x_-coordinate of the point.</span></span>  <br/> |
| <span data-ttu-id="546e4-122">_y_</span><span class="sxs-lookup"><span data-stu-id="546e4-122">_y_</span></span> <br/> |<span data-ttu-id="546e4-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="546e4-123">Required</span></span>  <br/> |<span data-ttu-id="546e4-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="546e4-124">**Double**</span></span> <br/> |<span data-ttu-id="546e4-125">Die _y_-Koordinate des Punkts.</span><span class="sxs-lookup"><span data-stu-id="546e4-125">The  _y_-coordinate of the point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="546e4-126">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="546e4-126">Return value</span></span>

 <span data-ttu-id="546e4-127">**Double**</span><span class="sxs-lookup"><span data-stu-id="546e4-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="546e4-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="546e4-128">Remarks</span></span>

<span data-ttu-id="546e4-129">Microsoft Visio gibt #REF!</span><span class="sxs-lookup"><span data-stu-id="546e4-129">Microsoft Visio returns #REF!</span></span> <span data-ttu-id="546e4-130">Wenn _Section_ nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="546e4-130">if  _section_ does not exist.</span></span> 
  
<span data-ttu-id="546e4-131">Der Rückgabewert ist positiv, wenn sich der Punkt links der Laufrichtung befindet; er ist positiv, wenn sich der Punkt rechts der Laufrichtung befindet.</span><span class="sxs-lookup"><span data-stu-id="546e4-131">The returned value is positive if the point is to the left of the direction of travel; it is negative if the point is to the right of the direction of travel.</span></span>
  

