---
title: MSOSHADE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: Ändert die Farbe, indem deren Helligkeit um den angegebenen Prozentsatz verringert wird.
ms.openlocfilehash: 207893552c7378589d4a648bf29ed88fcfd15224
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414494"
---
# <a name="msoshade-function"></a><span data-ttu-id="151f3-103">MSOSHADE Function</span><span class="sxs-lookup"><span data-stu-id="151f3-103">MSOSHADE Function</span></span>

<span data-ttu-id="151f3-104">Ändert die Farbe, indem deren Helligkeit um den angegebenen Prozentsatz verringert wird.</span><span class="sxs-lookup"><span data-stu-id="151f3-104">Modifies the color by decreasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="151f3-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="151f3-105">Version Information</span></span>

<span data-ttu-id="151f3-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="151f3-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="151f3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="151f3-107">Syntax</span></span>

<span data-ttu-id="151f3-108">MSOSHADE (\* \* *Color* \* \*, \* \* *-deltaLum* \* \*)</span><span class="sxs-lookup"><span data-stu-id="151f3-108">MSOSHADE(\*\* *color* \*\*, \*\* *-deltaLum* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="151f3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="151f3-109">Parameters</span></span>

|<span data-ttu-id="151f3-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="151f3-110">**Name**</span></span>|<span data-ttu-id="151f3-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="151f3-111">**Required/Optional**</span></span>|<span data-ttu-id="151f3-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="151f3-112">**Data Type**</span></span>|<span data-ttu-id="151f3-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="151f3-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="151f3-114">_color_</span><span class="sxs-lookup"><span data-stu-id="151f3-114">_color_</span></span> <br/> |<span data-ttu-id="151f3-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="151f3-115">Required</span></span>  <br/> |<span data-ttu-id="151f3-116">**RGB**</span><span class="sxs-lookup"><span data-stu-id="151f3-116">**RGB**</span></span> <br/> |<span data-ttu-id="151f3-117">Der standardmäßige RGB-Farbwert (Rot, Grün, Blau) oder eine Referenz auf eine Farbe.</span><span class="sxs-lookup"><span data-stu-id="151f3-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="151f3-118">_-deltaLum_</span><span class="sxs-lookup"><span data-stu-id="151f3-118">_-deltaLum_</span></span> <br/> |<span data-ttu-id="151f3-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="151f3-119">Required</span></span>  <br/> |<span data-ttu-id="151f3-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="151f3-120">**Integer**</span></span> <br/> |<span data-ttu-id="151f3-121">Die prozentuale Änderung in Richtung weiß (-100%) oder schwarz (100%) aus dem _Farbwert_ .</span><span class="sxs-lookup"><span data-stu-id="151f3-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="151f3-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="151f3-122">Remarks</span></span>

<span data-ttu-id="151f3-123">Je näher der _Farbwert_ zu weiß oder schwarz ist, desto kleiner ist die Änderung der Schattierung, die von einem bestimmten _deltaLum-_ Wert erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="151f3-123">The closer the  _color_ value is to white or black, the smaller the change to the shade that is produced by a specific  _-deltaLum_ value.</span></span> 
  

