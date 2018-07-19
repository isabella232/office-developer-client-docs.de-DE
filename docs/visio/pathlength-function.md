---
title: PATHLENGTH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Gibt die Länge des Pfads zurück, der im angegebenen Abschnitt "Geometrie" definiert ist.
ms.openlocfilehash: 37cabbde9fc0782bc1fde46f3065d0c945c9dada
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797604"
---
# <a name="pathlength-function"></a><span data-ttu-id="00e07-103">PATHLENGTH Function</span><span class="sxs-lookup"><span data-stu-id="00e07-103">PATHLENGTH Function</span></span>

<span data-ttu-id="00e07-104">Gibt die Länge des Pfads zurück, der im angegebenen Abschnitt "Geometrie" definiert ist.</span><span class="sxs-lookup"><span data-stu-id="00e07-104">Returns the length of the path that is defined in the specified Geometry section.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="00e07-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="00e07-105">Version Information</span></span>

<span data-ttu-id="00e07-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="00e07-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="00e07-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="00e07-107">Syntax</span></span>

<span data-ttu-id="00e07-108">PATHLENGTH (** *Abschnitt* ** ** *[, Segment]* **)</span><span class="sxs-lookup"><span data-stu-id="00e07-108">PATHLENGTH(** *section* ** ** *[,segment]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="00e07-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="00e07-109">Parameters</span></span>

|<span data-ttu-id="00e07-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="00e07-110">**Name**</span></span>|<span data-ttu-id="00e07-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="00e07-111">**Required/Optional**</span></span>|<span data-ttu-id="00e07-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="00e07-112">**Data Type**</span></span>|<span data-ttu-id="00e07-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="00e07-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="00e07-114">_section_</span><span class="sxs-lookup"><span data-stu-id="00e07-114">_section_</span></span> <br/> |<span data-ttu-id="00e07-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="00e07-115">Required</span></span>  <br/> |<span data-ttu-id="00e07-116">**String**</span><span class="sxs-lookup"><span data-stu-id="00e07-116">**String**</span></span> <br/> |<span data-ttu-id="00e07-117">Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).</span><span class="sxs-lookup"><span data-stu-id="00e07-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="00e07-118">_Segment_</span><span class="sxs-lookup"><span data-stu-id="00e07-118">_segment_</span></span> <br/> |<span data-ttu-id="00e07-119">Optional</span><span class="sxs-lookup"><span data-stu-id="00e07-119">Optional</span></span>  <br/> |<span data-ttu-id="00e07-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="00e07-120">**Integer**</span></span> <br/> |<span data-ttu-id="00e07-121">Das auf 1 basierende Segment des zu messenden Pfads.</span><span class="sxs-lookup"><span data-stu-id="00e07-121">The 1-based segment of the path to measure.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="00e07-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00e07-122">Return value</span></span>

 <span data-ttu-id="00e07-123">**Double**</span><span class="sxs-lookup"><span data-stu-id="00e07-123">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00e07-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00e07-124">Remarks</span></span>

<span data-ttu-id="00e07-125">Wenn _Section_ oder _Segment_ nicht vorhanden ist, gibt Microsoft Visio #REF! zurück.</span><span class="sxs-lookup"><span data-stu-id="00e07-125">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="00e07-126">Wenn Sie einen Wert für _Segment_ eingeschlossen, gibt PATHLENGTH die Länge dieses Abschnitts nur zurück.</span><span class="sxs-lookup"><span data-stu-id="00e07-126">If you include a  _segment_ value, PATHLENGTH returns the length of that segment only.</span></span> 
  

