---
title: PLAYSOUND-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251479
localization_priority: Normal
ms.assetid: 098d216f-e699-0e74-f702-ccfa7809c19b
description: Gibt eine Sounddatei oder einen Systemsound wieder.
ms.openlocfilehash: 752412aab6584d2b01235fe88644e3ec3fa5daee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435839"
---
# <a name="playsound-function"></a><span data-ttu-id="58314-103">PLAYSOUND Function</span><span class="sxs-lookup"><span data-stu-id="58314-103">PLAYSOUND Function</span></span>

<span data-ttu-id="58314-104">Gibt eine Sounddatei oder einen Systemsound wieder.</span><span class="sxs-lookup"><span data-stu-id="58314-104">Plays a sound file or system sound.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="58314-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="58314-105">Syntax</span></span>

<span data-ttu-id="58314-106">PLAYSOUND(" \*\* *filename* \*\* "|" \*\* *alias* \*\* ", \*\* *isAlias* \*\*, \*\* *beep* \*\*, \*\* *synch* \*\* )</span><span class="sxs-lookup"><span data-stu-id="58314-106">PLAYSOUND(" \*\* *filename* \*\* "|" \*\* *alias* \*\* ", \*\* *isAlias* \*\*, \*\* *beep* \*\*, \*\* *synch* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="58314-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="58314-107">Parameters</span></span>

|<span data-ttu-id="58314-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="58314-108">**Name**</span></span>|<span data-ttu-id="58314-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="58314-109">**Required/Optional**</span></span>|<span data-ttu-id="58314-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="58314-110">**Data Type**</span></span>|<span data-ttu-id="58314-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="58314-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="58314-112">_filename_</span><span class="sxs-lookup"><span data-stu-id="58314-112">_filename_</span></span> <br/> |<span data-ttu-id="58314-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="58314-113">Required</span></span>  <br/> |<span data-ttu-id="58314-114">**String**</span><span class="sxs-lookup"><span data-stu-id="58314-114">**String**</span></span> <br/> |<span data-ttu-id="58314-115">Der Name der Audiodatei, die abgespielt werden soll.</span><span class="sxs-lookup"><span data-stu-id="58314-115">The name of the sound file you want to play.</span></span>  <br/> |
| <span data-ttu-id="58314-116">_alias_</span><span class="sxs-lookup"><span data-stu-id="58314-116">_alias_</span></span> <br/> |<span data-ttu-id="58314-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="58314-117">Required</span></span>  <br/> |<span data-ttu-id="58314-118">**String**</span><span class="sxs-lookup"><span data-stu-id="58314-118">**String**</span></span> <br/> | <span data-ttu-id="58314-119">Ein Systemsignal, das durch einen Alias dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="58314-119">A system sound represented by an alias.</span></span>  <br/> |
| <span data-ttu-id="58314-120">_isAlias_</span><span class="sxs-lookup"><span data-stu-id="58314-120">_isAlias_</span></span> <br/> |<span data-ttu-id="58314-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="58314-121">Required</span></span>  <br/> |<span data-ttu-id="58314-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="58314-122">**Boolean**</span></span> <br/> | <span data-ttu-id="58314-123">Gibt an, ob der vorangegangene Ausdruck ein Alias oder ein Dateiname ist. Verwenden Sie einen Wert ungleich null zur Angabe eines Alias.</span><span class="sxs-lookup"><span data-stu-id="58314-123">Specifies whether the preceding expression is an alias or file name; use a non-zero value to specify an alias.</span></span>  <br/> |
| <span data-ttu-id="58314-124">_Signalton_</span><span class="sxs-lookup"><span data-stu-id="58314-124">_beep_</span></span> <br/> |<span data-ttu-id="58314-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="58314-125">Required</span></span>  <br/> |<span data-ttu-id="58314-126">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="58314-126">**Boolean**</span></span> <br/> |<span data-ttu-id="58314-127">Gibt an, ob Microsoft Visio eine akustische Meldung ausgibt, wenn der Sound nicht abgespielt werden kann. Verwenden Sie einen Wert ungleich null, um ein akustisches Signal zu veranlassen.</span><span class="sxs-lookup"><span data-stu-id="58314-127">Specifies whether Microsoft Visio beeps when sound can't be played; use a non-zero number to beep.</span></span>  <br/> |
| <span data-ttu-id="58314-128">_synch_</span><span class="sxs-lookup"><span data-stu-id="58314-128">_synch_</span></span> <br/> |<span data-ttu-id="58314-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="58314-129">Required</span></span>  <br/> |<span data-ttu-id="58314-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="58314-130">**Boolean**</span></span> <br/> |<span data-ttu-id="58314-131">Bestimmt, ob Klänge asynchron (0) oder synchron (1) abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="58314-131">Determines whether sounds are played asynchronously (0) or synchronously (1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58314-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="58314-132">Remarks</span></span>

<span data-ttu-id="58314-p101">Sounds sollten normalerweise asynchron abgespielt werden, damit Visio fortgesetzt werden kann, während der Sound abgespielt wird. Wenn Sie mehrere Sounds hintereinander abspielen möchten, sollten Sie diese synchron abspielen. Sonst könnte es geschehen, dass einige nicht abgespielt werden.
</span><span class="sxs-lookup"><span data-stu-id="58314-p101">You should usually play sounds asynchronously so that Visio can continue processing while it plays the sound. To string several sounds together, play them synchronously, or some might fail to play.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="58314-135">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="58314-135">Example 1</span></span>

<span data-ttu-id="58314-136">PLAYSOUND("chord.wav", 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="58314-136">PLAYSOUND("chord.wav", 0, 0, 0)</span></span>
  
<span data-ttu-id="58314-137">Spielt die Wave-Datei chord.wav asynchron und ohne akustische Warnung ab.</span><span class="sxs-lookup"><span data-stu-id="58314-137">Plays the wave audio file chord.wav asynchronously with no warning beep.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="58314-138">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="58314-138">Example 2</span></span>

<span data-ttu-id="58314-139">PLAYSOUND("Systemklang", 1, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="58314-139">PLAYSOUND("SystemExclamation", 1, 0, 0)</span></span>
  
<span data-ttu-id="58314-140">Spielt das Systemsignal für Hinweise asynchron und ohne akustische Warnung ab.</span><span class="sxs-lookup"><span data-stu-id="58314-140">Plays the system exclamation sound asynchronously with no warning beep.</span></span>
  

