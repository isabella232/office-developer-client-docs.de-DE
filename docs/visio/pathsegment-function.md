---
title: PATHSEGMENT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Gibt die 1-basierte Segmentnummer an der angegebenen prozentualen Markierung entlang des angegebenen Pfads zurück.
ms.openlocfilehash: c4dfc4d33de1a9c1a03ef14d76103b4de0f28bc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344450"
---
# <a name="pathsegment-function"></a><span data-ttu-id="c6cca-103">PATHSEGMENT Function</span><span class="sxs-lookup"><span data-stu-id="c6cca-103">PATHSEGMENT Function</span></span>

<span data-ttu-id="c6cca-104">Gibt die 1-basierte Segmentnummer an der angegebenen prozentualen Markierung entlang des angegebenen Pfads zurück.</span><span class="sxs-lookup"><span data-stu-id="c6cca-104">Returns the 1-based segment number at the specified percentage mark along the specified path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c6cca-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6cca-105">Syntax</span></span>

<span data-ttu-id="c6cca-106">PATHSEGMENT (\* \* *section* \* \*, \* \* *Reise* \* \*)</span><span class="sxs-lookup"><span data-stu-id="c6cca-106">PATHSEGMENT(\*\* *section* \*\*, \*\* *travel* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c6cca-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6cca-107">Parameters</span></span>

|<span data-ttu-id="c6cca-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c6cca-108">**Name**</span></span>|<span data-ttu-id="c6cca-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="c6cca-109">**Required/Optional**</span></span>|<span data-ttu-id="c6cca-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="c6cca-110">**Data Type**</span></span>|<span data-ttu-id="c6cca-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c6cca-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c6cca-112">_section_</span><span class="sxs-lookup"><span data-stu-id="c6cca-112">_section_</span></span> <br/> |<span data-ttu-id="c6cca-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c6cca-113">Required</span></span>  <br/> |<span data-ttu-id="c6cca-114">**String**</span><span class="sxs-lookup"><span data-stu-id="c6cca-114">**String**</span></span> <br/> |<span data-ttu-id="c6cca-115">Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).</span><span class="sxs-lookup"><span data-stu-id="c6cca-115">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="c6cca-116">_Reise_</span><span class="sxs-lookup"><span data-stu-id="c6cca-116">_travel_</span></span> <br/> |<span data-ttu-id="c6cca-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c6cca-117">Required</span></span>  <br/> |<span data-ttu-id="c6cca-118">**Double**</span><span class="sxs-lookup"><span data-stu-id="c6cca-118">**Double**</span></span> <br/> |<span data-ttu-id="c6cca-119">Der Prozentsatz entlang des durchlaufenen Pfads vom Anfangs- zum Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="c6cca-119">The percentage of the path traversed, from the begin point to the end point.</span></span> <span data-ttu-id="c6cca-120">Muss zwischen 0 und 1 liegen.</span><span class="sxs-lookup"><span data-stu-id="c6cca-120">Must be between 0 and 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c6cca-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6cca-121">Return value</span></span>

<span data-ttu-id="c6cca-122">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="c6cca-122">Integer</span></span>
  

