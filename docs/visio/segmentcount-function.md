---
title: SEGMENTCOUNT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: Gibt die Anzahl der Liniensegmente zurück, aus denen der Pfad besteht.
ms.openlocfilehash: 93a77d9085e6900f502a75401847ad685d25effd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797999"
---
# <a name="segmentcount-function"></a><span data-ttu-id="445f6-103">SEGMENTCOUNT Function</span><span class="sxs-lookup"><span data-stu-id="445f6-103">SEGMENTCOUNT Function</span></span>

<span data-ttu-id="445f6-104">Gibt die Anzahl der Liniensegmente zurück, aus denen der Pfad besteht.</span><span class="sxs-lookup"><span data-stu-id="445f6-104">Returns the number of line segments that make up the path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="445f6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="445f6-105">Syntax</span></span>

<span data-ttu-id="445f6-106">SEGMENTCOUNT (** *PathRef* **)</span><span class="sxs-lookup"><span data-stu-id="445f6-106">SEGMENTCOUNT(** *pathRef* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="445f6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="445f6-107">Parameters</span></span>

|<span data-ttu-id="445f6-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="445f6-108">**Name**</span></span>|<span data-ttu-id="445f6-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="445f6-109">**Required/Optional**</span></span>|<span data-ttu-id="445f6-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="445f6-110">**Data Type**</span></span>|<span data-ttu-id="445f6-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="445f6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="445f6-112">_pathRef_</span><span class="sxs-lookup"><span data-stu-id="445f6-112">_pathRef_</span></span> <br/> |<span data-ttu-id="445f6-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="445f6-113">Required</span></span>  <br/> |<span data-ttu-id="445f6-114">**Integer**</span><span class="sxs-lookup"><span data-stu-id="445f6-114">**Integer**</span></span> <br/> |<span data-ttu-id="445f6-115">Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf die Zelle "Path" (z. B. Geometrie1.Path).</span><span class="sxs-lookup"><span data-stu-id="445f6-115">The Geometry section that represents the path, specified by a reference to Path cell (for example, Geometry1.Path).</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="445f6-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="445f6-116">Return value</span></span>

<span data-ttu-id="445f6-117">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="445f6-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="445f6-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="445f6-118">Remarks</span></span>

<span data-ttu-id="445f6-119">Liniensprünge sind in der Gesamtzahl der zurückgegebenen Segmente nicht eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="445f6-119">Line jumps are not included in the total number of segments returned.</span></span>
  

