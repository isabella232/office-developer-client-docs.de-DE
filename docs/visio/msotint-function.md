---
title: MSOTINT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: Ändert die Farbe, indem deren Helligkeit um den angegebenen Prozentsatz erhöht  wird.
ms.openlocfilehash: 50e81b5202174c61905d3914c50feddcb05a91cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797563"
---
# <a name="msotint-function"></a><span data-ttu-id="92169-103">MSOTINT Function</span><span class="sxs-lookup"><span data-stu-id="92169-103">MSOTINT Function</span></span>

<span data-ttu-id="92169-104">Ändert die Farbe, indem deren Helligkeit um den angegebenen Prozentsatz erhöht  wird.</span><span class="sxs-lookup"><span data-stu-id="92169-104">Modifies the color by increasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="92169-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="92169-105">Version Information</span></span>

<span data-ttu-id="92169-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="92169-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="92169-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="92169-107">Syntax</span></span>

<span data-ttu-id="92169-108">MSOTINT (** *Farbe* **, ** *DeltaLum* **)</span><span class="sxs-lookup"><span data-stu-id="92169-108">MSOTINT(** *color* **, ** *deltaLum* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="92169-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="92169-109">Parameters</span></span>

|<span data-ttu-id="92169-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="92169-110">**Name**</span></span>|<span data-ttu-id="92169-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="92169-111">**Required/Optional**</span></span>|<span data-ttu-id="92169-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="92169-112">**Data Type**</span></span>|<span data-ttu-id="92169-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="92169-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="92169-114">_Farbe_</span><span class="sxs-lookup"><span data-stu-id="92169-114">_color_</span></span> <br/> |<span data-ttu-id="92169-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="92169-115">Required</span></span>  <br/> |<span data-ttu-id="92169-116">**RGB**</span><span class="sxs-lookup"><span data-stu-id="92169-116">**RGB**</span></span> <br/> |<span data-ttu-id="92169-117">Der standardmäßige RGB-Farbwert (Rot, Grün, Blau) oder eine Referenz auf eine Farbe.</span><span class="sxs-lookup"><span data-stu-id="92169-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="92169-118">_deltaLum_</span><span class="sxs-lookup"><span data-stu-id="92169-118">_deltaLum_</span></span> <br/> |<span data-ttu-id="92169-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="92169-119">Required</span></span>  <br/> |<span data-ttu-id="92169-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="92169-120">**Integer**</span></span> <br/> |<span data-ttu-id="92169-121">Die prozentuale Änderung in Richtung weiß (-100 %) oder Schwarz (100 %) vom Wert _Color_ .</span><span class="sxs-lookup"><span data-stu-id="92169-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92169-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92169-122">Remarks</span></span>

<span data-ttu-id="92169-123">Je näher der _Color_ -Wert ist weiß oder Schwarz ist, desto geringer ist die Änderung am Farbton, die von einem bestimmten _DeltaLum_ -Wert bewirkt wird.</span><span class="sxs-lookup"><span data-stu-id="92169-123">The closer the  _color_ value is to white or black, the smaller the change to the tint that is produced by a specific  _deltaLum_ value.</span></span> 
  

