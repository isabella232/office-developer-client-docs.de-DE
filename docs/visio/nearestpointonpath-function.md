---
title: NEARESTPOINTONPATH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Gibt den Prozentsatz des Abstands entlang des Pfads des Punkts zurück, der den angegebenen Koordinaten am nächsten liegt, wie einen Wert zwischen 0 und 1.
ms.openlocfilehash: ced20cdf1f3531eafaa03c2666b09334029fd3da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319719"
---
# <a name="nearestpointonpath-function"></a><span data-ttu-id="af12b-103">NEARESTPOINTONPATH Function</span><span class="sxs-lookup"><span data-stu-id="af12b-103">NEARESTPOINTONPATH Function</span></span>

<span data-ttu-id="af12b-104">Gibt den Prozentsatz des Abstands entlang des Pfads des Punkts zurück, der den angegebenen Koordinaten am nächsten liegt, wie einen Wert zwischen 0 und 1.</span><span class="sxs-lookup"><span data-stu-id="af12b-104">Returns the percentage of the distance along the path of the point that is nearest to the specified coordinates, as a value between 0 and 1.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="af12b-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="af12b-105">Version Information</span></span>

<span data-ttu-id="af12b-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="af12b-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="af12b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="af12b-107">Syntax</span></span>

<span data-ttu-id="af12b-108">NEARESTPOINTONPATH (\* \* *section* \* \*, \* \* *x* \* \*, \* \* *y* \* \*)</span><span class="sxs-lookup"><span data-stu-id="af12b-108">NEARESTPOINTONPATH(\*\* *section* \*\*, \*\* *x* \*\*, \*\* *y* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="af12b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="af12b-109">Parameters</span></span>

|<span data-ttu-id="af12b-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="af12b-110">**Name**</span></span>|<span data-ttu-id="af12b-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="af12b-111">**Required/Optional**</span></span>|<span data-ttu-id="af12b-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="af12b-112">**Data Type**</span></span>|<span data-ttu-id="af12b-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="af12b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="af12b-114">_section_</span><span class="sxs-lookup"><span data-stu-id="af12b-114">_section_</span></span> <br/> |<span data-ttu-id="af12b-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="af12b-115">Required</span></span>  <br/> |<span data-ttu-id="af12b-116">**String**</span><span class="sxs-lookup"><span data-stu-id="af12b-116">**String**</span></span> <br/> |<span data-ttu-id="af12b-117">Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).</span><span class="sxs-lookup"><span data-stu-id="af12b-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="af12b-118">_x_</span><span class="sxs-lookup"><span data-stu-id="af12b-118">_x_</span></span> <br/> |<span data-ttu-id="af12b-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="af12b-119">Required</span></span>  <br/> |<span data-ttu-id="af12b-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="af12b-120">**Double**</span></span> <br/> |<span data-ttu-id="af12b-121">Die _x_-Koordinate des angegebenen Punkts.</span><span class="sxs-lookup"><span data-stu-id="af12b-121">The  _x_-coordinate of the specified point.</span></span>  <br/> |
| <span data-ttu-id="af12b-122">_y_</span><span class="sxs-lookup"><span data-stu-id="af12b-122">_y_</span></span> <br/> |<span data-ttu-id="af12b-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="af12b-123">Required</span></span>  <br/> |<span data-ttu-id="af12b-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="af12b-124">**Double**</span></span> <br/> |<span data-ttu-id="af12b-125">Die _y_-Koordinate des angegebenen Punkts.</span><span class="sxs-lookup"><span data-stu-id="af12b-125">The  _y_-coordinate of the specified point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="af12b-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af12b-126">Return value</span></span>

 <span data-ttu-id="af12b-127">**Double**</span><span class="sxs-lookup"><span data-stu-id="af12b-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="af12b-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af12b-128">Remarks</span></span>

<span data-ttu-id="af12b-129">Wenn _section_ nicht vorhanden ist, gibt Microsoft Visio #REF! zurück.</span><span class="sxs-lookup"><span data-stu-id="af12b-129">If  _section_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

