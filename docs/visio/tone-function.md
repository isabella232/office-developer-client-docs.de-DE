---
title: TONE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Ändert die Farbe, indem die Sättigung um den im Parameter int angegebenen Wert verringert wird.
ms.openlocfilehash: c3352d4c15671244d0fc4701f2c26b4e0c2ea54d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335686"
---
# <a name="tone-function"></a><span data-ttu-id="a5e4f-103">TONE Function</span><span class="sxs-lookup"><span data-stu-id="a5e4f-103">TONE Function</span></span>

<span data-ttu-id="a5e4f-104">Ändert die Farbe, indem die Sättigung um den im Parameter _int_ angegebenen Wert verringert wird.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-104">Modifies the color by decreasing its saturation by the amount specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a5e4f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5e4f-105">Syntax</span></span>

<span data-ttu-id="a5e4f-106">TONE (\* \* *Color* \* \*, \* \* *int* \* \*)</span><span class="sxs-lookup"><span data-stu-id="a5e4f-106">TONE(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a5e4f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5e4f-107">Parameters</span></span>

|<span data-ttu-id="a5e4f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="a5e4f-108">**Name**</span></span>|<span data-ttu-id="a5e4f-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="a5e4f-109">**Required/Optional**</span></span>|<span data-ttu-id="a5e4f-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a5e4f-110">**Data Type**</span></span>|<span data-ttu-id="a5e4f-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a5e4f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a5e4f-112">_color_</span><span class="sxs-lookup"><span data-stu-id="a5e4f-112">_color_</span></span> <br/> |<span data-ttu-id="a5e4f-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a5e4f-113">Required</span></span>  <br/> |<span data-ttu-id="a5e4f-114">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="a5e4f-114">**Numeric**</span></span> <br/> |<span data-ttu-id="a5e4f-115">Der Farbindex von Microsoft Visio oder der RGB-Wert der Farbe.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="a5e4f-116">_int_</span><span class="sxs-lookup"><span data-stu-id="a5e4f-116">_int_</span></span> <br/> |<span data-ttu-id="a5e4f-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a5e4f-117">Required</span></span>  <br/> |<span data-ttu-id="a5e4f-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="a5e4f-118">**Integer**</span></span> <br/> |<span data-ttu-id="a5e4f-119">Der Wert, um den die Farbsättigung verringert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-119">The amount by which to decrease the saturation of the color.</span></span> <span data-ttu-id="a5e4f-120">Kann positiv oder negativ sein.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a5e4f-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5e4f-121">Return value</span></span>

 <span data-ttu-id="a5e4f-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="a5e4f-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a5e4f-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5e4f-123">Remarks</span></span>

<span data-ttu-id="a5e4f-124">Die unteren und oberen Grenzwerte der Sättigung liegen jeweils bei 0 und 240.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-124">The upper and lower limits of saturation are 0 and 240 respectively.</span></span> <span data-ttu-id="a5e4f-125">Es gibt keine Begrenzung für die Größe der Ganzzahl, die Sie für den _int_ -Parameter übergeben können, aber die Sättigung überschreitet diese Grenzwerte nie.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but saturation never exceeds these limits.</span></span> 
  

