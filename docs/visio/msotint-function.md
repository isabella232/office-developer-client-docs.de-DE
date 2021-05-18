---
title: MSOTINT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: Ändert die Farbe, indem deren Helligkeit um den angegebenen Prozentsatz erhöht  wird.
ms.openlocfilehash: d63b90d0cd6fcb35e23a8efa4ca9e13e2838bc21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406423"
---
# <a name="msotint-function"></a><span data-ttu-id="ef41c-103">MSOTINT Function</span><span class="sxs-lookup"><span data-stu-id="ef41c-103">MSOTINT Function</span></span>

<span data-ttu-id="ef41c-104">Ändert die Farbe, indem deren Helligkeit um den angegebenen Prozentsatz erhöht  wird.</span><span class="sxs-lookup"><span data-stu-id="ef41c-104">Modifies the color by increasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="ef41c-105">Versionsinformationen</span><span class="sxs-lookup"><span data-stu-id="ef41c-105">Version Information</span></span>

<span data-ttu-id="ef41c-106">Hinzugefügte Version: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="ef41c-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ef41c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef41c-107">Syntax</span></span>

<span data-ttu-id="ef41c-108">MSOTINT(\*\* *color* \*\*, \*\* *deltaLum* \*\* )</span><span class="sxs-lookup"><span data-stu-id="ef41c-108">MSOTINT(\*\* *color* \*\*, \*\* *deltaLum* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ef41c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef41c-109">Parameters</span></span>

|<span data-ttu-id="ef41c-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="ef41c-110">**Name**</span></span>|<span data-ttu-id="ef41c-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="ef41c-111">**Required/Optional**</span></span>|<span data-ttu-id="ef41c-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="ef41c-112">**Data Type**</span></span>|<span data-ttu-id="ef41c-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ef41c-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ef41c-114">_color_</span><span class="sxs-lookup"><span data-stu-id="ef41c-114">_color_</span></span> <br/> |<span data-ttu-id="ef41c-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ef41c-115">Required</span></span>  <br/> |<span data-ttu-id="ef41c-116">**RGB**</span><span class="sxs-lookup"><span data-stu-id="ef41c-116">**RGB**</span></span> <br/> |<span data-ttu-id="ef41c-117">Der standardmäßige RGB-Farbwert (Rot, Grün, Blau) oder eine Referenz auf eine Farbe.</span><span class="sxs-lookup"><span data-stu-id="ef41c-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="ef41c-118">_deltaLum_</span><span class="sxs-lookup"><span data-stu-id="ef41c-118">_deltaLum_</span></span> <br/> |<span data-ttu-id="ef41c-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ef41c-119">Required</span></span>  <br/> |<span data-ttu-id="ef41c-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="ef41c-120">**Integer**</span></span> <br/> |<span data-ttu-id="ef41c-121">Die prozentuale Änderung in Richtung Weiß (-100 %) oder schwarz (100 %) aus dem _Farbwert._</span><span class="sxs-lookup"><span data-stu-id="ef41c-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef41c-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ef41c-122">Remarks</span></span>

<span data-ttu-id="ef41c-123">Je näher der  _Farbwert_ weiß oder schwarz ist, desto kleiner ist die Änderung des Farbtons, der durch einen bestimmten  _deltaLum-Wert erzeugt_ wird.</span><span class="sxs-lookup"><span data-stu-id="ef41c-123">The closer the  _color_ value is to white or black, the smaller the change to the tint that is produced by a specific  _deltaLum_ value.</span></span> 
  

