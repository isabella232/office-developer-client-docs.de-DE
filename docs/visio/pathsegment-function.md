---
title: PATHSEGMENT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Gibt die 1 basierende Segmentnummer an der angegebenen prozentmarkierung entlang des angegebenen Pfads zurück.
ms.openlocfilehash: b25f43ffa3c719cfc5ffbd1e417f2da9640e483b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797609"
---
# <a name="pathsegment-function"></a><span data-ttu-id="dc497-103">PATHSEGMENT Function</span><span class="sxs-lookup"><span data-stu-id="dc497-103">PATHSEGMENT Function</span></span>

<span data-ttu-id="dc497-104">Gibt die 1 basierende Segmentnummer an der angegebenen prozentmarkierung entlang des angegebenen Pfads zurück.</span><span class="sxs-lookup"><span data-stu-id="dc497-104">Returns the 1-based segment number at the specified percentage mark along the specified path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="dc497-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc497-105">Syntax</span></span>

<span data-ttu-id="dc497-106">PATHSEGMENT (** *Abschnitt* **, ** *Reisen* **)</span><span class="sxs-lookup"><span data-stu-id="dc497-106">PATHSEGMENT(** *section* **, ** *travel* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dc497-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc497-107">Parameters</span></span>

|<span data-ttu-id="dc497-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="dc497-108">**Name**</span></span>|<span data-ttu-id="dc497-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="dc497-109">**Required/Optional**</span></span>|<span data-ttu-id="dc497-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="dc497-110">**Data Type**</span></span>|<span data-ttu-id="dc497-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dc497-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dc497-112">_section_</span><span class="sxs-lookup"><span data-stu-id="dc497-112">_section_</span></span> <br/> |<span data-ttu-id="dc497-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dc497-113">Required</span></span>  <br/> |<span data-ttu-id="dc497-114">**String**</span><span class="sxs-lookup"><span data-stu-id="dc497-114">**String**</span></span> <br/> |<span data-ttu-id="dc497-115">Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).</span><span class="sxs-lookup"><span data-stu-id="dc497-115">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="dc497-116">_Reisen_</span><span class="sxs-lookup"><span data-stu-id="dc497-116">_travel_</span></span> <br/> |<span data-ttu-id="dc497-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dc497-117">Required</span></span>  <br/> |<span data-ttu-id="dc497-118">**Double**</span><span class="sxs-lookup"><span data-stu-id="dc497-118">**Double**</span></span> <br/> |<span data-ttu-id="dc497-p101">Der Prozentsatz entlang des durchlaufenen Pfads vom Anfangs- zum Endpunkt. Muss zwischen 0 und 1 liegen.</span><span class="sxs-lookup"><span data-stu-id="dc497-p101">The percentage of the path traversed, from the begin point to the end point. Must be between 0 and 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="dc497-121">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="dc497-121">Return value</span></span>

<span data-ttu-id="dc497-122">Integer</span><span class="sxs-lookup"><span data-stu-id="dc497-122">Integer</span></span>
  

