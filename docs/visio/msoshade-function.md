---
title: MSOSHADE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: Ändert die Farbe, indem deren Helligkeit um den angegebenen Prozentsatz verringert wird.
ms.openlocfilehash: f5f6eb0b6009473dcec017e951cca2f90b6c4d55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797534"
---
# <a name="msoshade-function"></a><span data-ttu-id="a3fc4-103">MSOSHADE Function</span><span class="sxs-lookup"><span data-stu-id="a3fc4-103">MSOSHADE Function</span></span>

<span data-ttu-id="a3fc4-104">Ändert die Farbe, indem deren Helligkeit um den angegebenen Prozentsatz verringert wird.</span><span class="sxs-lookup"><span data-stu-id="a3fc4-104">Modifies the color by decreasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="a3fc4-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="a3fc4-105">Version Information</span></span>

<span data-ttu-id="a3fc4-106">Hinzugefügte Version: Visio 2010</span><span class="sxs-lookup"><span data-stu-id="a3fc4-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a3fc4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3fc4-107">Syntax</span></span>

<span data-ttu-id="a3fc4-108">MSOSHADE (** *Farbe* **, ** *DeltaLum* **)</span><span class="sxs-lookup"><span data-stu-id="a3fc4-108">MSOSHADE(** *color* **, ** *-deltaLum* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a3fc4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3fc4-109">Parameters</span></span>

|<span data-ttu-id="a3fc4-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="a3fc4-110">**Name**</span></span>|<span data-ttu-id="a3fc4-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="a3fc4-111">**Required/Optional**</span></span>|<span data-ttu-id="a3fc4-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a3fc4-112">**Data Type**</span></span>|<span data-ttu-id="a3fc4-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a3fc4-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a3fc4-114">_Farbe_</span><span class="sxs-lookup"><span data-stu-id="a3fc4-114">_color_</span></span> <br/> |<span data-ttu-id="a3fc4-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a3fc4-115">Required</span></span>  <br/> |<span data-ttu-id="a3fc4-116">**RGB**</span><span class="sxs-lookup"><span data-stu-id="a3fc4-116">**RGB**</span></span> <br/> |<span data-ttu-id="a3fc4-117">Der standardmäßige RGB-Farbwert (Rot, Grün, Blau) oder eine Referenz auf eine Farbe.</span><span class="sxs-lookup"><span data-stu-id="a3fc4-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="a3fc4-118">_-deltaLum_</span><span class="sxs-lookup"><span data-stu-id="a3fc4-118">_-deltaLum_</span></span> <br/> |<span data-ttu-id="a3fc4-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a3fc4-119">Required</span></span>  <br/> |<span data-ttu-id="a3fc4-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="a3fc4-120">**Integer**</span></span> <br/> |<span data-ttu-id="a3fc4-121">Die prozentuale Änderung in Richtung weiß (-100 %) oder Schwarz (100 %) vom Wert _Color_ .</span><span class="sxs-lookup"><span data-stu-id="a3fc4-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3fc4-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a3fc4-122">Remarks</span></span>

<span data-ttu-id="a3fc4-123">Je näher der _Color_ -Wert ist weiß oder Schwarz ist, desto geringer ist die Änderung am Farbton, die von einem bestimmten _DeltaLum_ -Wert bewirkt wird.</span><span class="sxs-lookup"><span data-stu-id="a3fc4-123">The closer the  _color_ value is to white or black, the smaller the change to the shade that is produced by a specific  _-deltaLum_ value.</span></span> 
  

