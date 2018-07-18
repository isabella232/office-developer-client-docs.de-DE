---
title: NEARESTPOINTONPATH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Gibt den Prozentsatz des Abstands entlang des Pfads des Punkts zurück, der den angegebenen Koordinaten am nächsten liegt, wie einen Wert zwischen 0 und 1.
ms.openlocfilehash: d9e9b890033526fec99f04cee30ae93578487652
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797535"
---
# <a name="nearestpointonpath-function"></a><span data-ttu-id="e1224-103">NEARESTPOINTONPATH Function</span><span class="sxs-lookup"><span data-stu-id="e1224-103">NEARESTPOINTONPATH Function</span></span>

<span data-ttu-id="e1224-104">Gibt den Prozentsatz des Abstands entlang des Pfads des Punkts zurück, der den angegebenen Koordinaten am nächsten liegt, wie einen Wert zwischen 0 und 1.</span><span class="sxs-lookup"><span data-stu-id="e1224-104">Returns the percentage of the distance along the path of the point that is nearest to the specified coordinates, as a value between 0 and 1.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="e1224-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="e1224-105">Version Information</span></span>

<span data-ttu-id="e1224-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="e1224-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e1224-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1224-107">Syntax</span></span>

<span data-ttu-id="e1224-108">NEARESTPOINTONPATH (** *Abschnitt* **, ** *X* **, ** *y* **)</span><span class="sxs-lookup"><span data-stu-id="e1224-108">NEARESTPOINTONPATH(** *section* **, ** *x* **, ** *y* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e1224-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1224-109">Parameters</span></span>

|<span data-ttu-id="e1224-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="e1224-110">**Name**</span></span>|<span data-ttu-id="e1224-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="e1224-111">**Required/Optional**</span></span>|<span data-ttu-id="e1224-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="e1224-112">**Data Type**</span></span>|<span data-ttu-id="e1224-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e1224-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e1224-114">_section_</span><span class="sxs-lookup"><span data-stu-id="e1224-114">_section_</span></span> <br/> |<span data-ttu-id="e1224-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e1224-115">Required</span></span>  <br/> |<span data-ttu-id="e1224-116">**String**</span><span class="sxs-lookup"><span data-stu-id="e1224-116">**String**</span></span> <br/> |<span data-ttu-id="e1224-117">Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).</span><span class="sxs-lookup"><span data-stu-id="e1224-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="e1224-118">_x_</span><span class="sxs-lookup"><span data-stu-id="e1224-118">_x_</span></span> <br/> |<span data-ttu-id="e1224-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e1224-119">Required</span></span>  <br/> |<span data-ttu-id="e1224-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="e1224-120">**Double**</span></span> <br/> |<span data-ttu-id="e1224-121">Die _X_-Koordinate des angegebenen Punkts.</span><span class="sxs-lookup"><span data-stu-id="e1224-121">The  _x_-coordinate of the specified point.</span></span>  <br/> |
| <span data-ttu-id="e1224-122">_y_</span><span class="sxs-lookup"><span data-stu-id="e1224-122">_y_</span></span> <br/> |<span data-ttu-id="e1224-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e1224-123">Required</span></span>  <br/> |<span data-ttu-id="e1224-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="e1224-124">**Double**</span></span> <br/> |<span data-ttu-id="e1224-125">Die _y_-Koordinate des angegebenen Punkts.</span><span class="sxs-lookup"><span data-stu-id="e1224-125">The  _y_-coordinate of the specified point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e1224-126">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="e1224-126">Return value</span></span>

 <span data-ttu-id="e1224-127">**Double**</span><span class="sxs-lookup"><span data-stu-id="e1224-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e1224-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1224-128">Remarks</span></span>

<span data-ttu-id="e1224-129">Wenn _Section_ nicht vorhanden ist, gibt Microsoft Visio #REF! zurück.</span><span class="sxs-lookup"><span data-stu-id="e1224-129">If  _section_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

