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
description: Eine Audiodatei oder Systemsound wiedergegeben.
ms.openlocfilehash: ca54b749b764e9ea2c7db71d41268303542417f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797653"
---
# <a name="playsound-function"></a><span data-ttu-id="da03f-103">PLAYSOUND Function</span><span class="sxs-lookup"><span data-stu-id="da03f-103">PLAYSOUND Function</span></span>

<span data-ttu-id="da03f-104">Eine Audiodatei oder Systemsound wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="da03f-104">Plays a sound file or system sound.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="da03f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="da03f-105">Syntax</span></span>

<span data-ttu-id="da03f-106">PLAYSOUND ("** *Filename* **" | "** *Alias* **", ** *istAlias* **, ** *Beep* **, ** *Synch* **)</span><span class="sxs-lookup"><span data-stu-id="da03f-106">PLAYSOUND(" ** *filename* ** "|" ** *alias* ** ", ** *isAlias* **, ** *beep* **, ** *synch* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="da03f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="da03f-107">Parameters</span></span>

|<span data-ttu-id="da03f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="da03f-108">**Name**</span></span>|<span data-ttu-id="da03f-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="da03f-109">**Required/Optional**</span></span>|<span data-ttu-id="da03f-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="da03f-110">**Data Type**</span></span>|<span data-ttu-id="da03f-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="da03f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="da03f-112">_Dateiname_</span><span class="sxs-lookup"><span data-stu-id="da03f-112">_filename_</span></span> <br/> |<span data-ttu-id="da03f-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="da03f-113">Required</span></span>  <br/> |<span data-ttu-id="da03f-114">**String**</span><span class="sxs-lookup"><span data-stu-id="da03f-114">**String**</span></span> <br/> |<span data-ttu-id="da03f-115">Der Name der Audiodatei, die abgespielt werden soll.</span><span class="sxs-lookup"><span data-stu-id="da03f-115">The name of the sound file you want to play.</span></span>  <br/> |
| <span data-ttu-id="da03f-116">_alias_</span><span class="sxs-lookup"><span data-stu-id="da03f-116">_alias_</span></span> <br/> |<span data-ttu-id="da03f-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="da03f-117">Required</span></span>  <br/> |<span data-ttu-id="da03f-118">**String**</span><span class="sxs-lookup"><span data-stu-id="da03f-118">**String**</span></span> <br/> | <span data-ttu-id="da03f-119">Ein Systemsignal, das durch einen Alias dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="da03f-119">A system sound represented by an alias.</span></span>  <br/> |
| <span data-ttu-id="da03f-120">_istAlias_</span><span class="sxs-lookup"><span data-stu-id="da03f-120">_isAlias_</span></span> <br/> |<span data-ttu-id="da03f-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="da03f-121">Required</span></span>  <br/> |<span data-ttu-id="da03f-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="da03f-122">**Boolean**</span></span> <br/> | <span data-ttu-id="da03f-123">Gibt an, ob der vorangegangene Ausdruck ein Alias oder ein Dateiname ist. Verwenden Sie einen Wert ungleich null zur Angabe eines Alias.</span><span class="sxs-lookup"><span data-stu-id="da03f-123">Specifies whether the preceding expression is an alias or file name; use a non-zero value to specify an alias.</span></span>  <br/> |
| <span data-ttu-id="da03f-124">_Signalton_</span><span class="sxs-lookup"><span data-stu-id="da03f-124">_beep_</span></span> <br/> |<span data-ttu-id="da03f-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="da03f-125">Required</span></span>  <br/> |<span data-ttu-id="da03f-126">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="da03f-126">**Boolean**</span></span> <br/> |<span data-ttu-id="da03f-127">Gibt an, ob Microsoft Visio eine akustische Meldung ausgibt, wenn der Sound nicht abgespielt werden kann. Verwenden Sie einen Wert ungleich null, um ein akustisches Signal zu veranlassen.</span><span class="sxs-lookup"><span data-stu-id="da03f-127">Specifies whether Microsoft Visio beeps when sound can't be played; use a non-zero number to beep.</span></span>  <br/> |
| <span data-ttu-id="da03f-128">_Synch_</span><span class="sxs-lookup"><span data-stu-id="da03f-128">_synch_</span></span> <br/> |<span data-ttu-id="da03f-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="da03f-129">Required</span></span>  <br/> |<span data-ttu-id="da03f-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="da03f-130">**Boolean**</span></span> <br/> |<span data-ttu-id="da03f-131">Bestimmt, ob Klänge asynchron (0) oder synchron (1) abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="da03f-131">Determines whether sounds are played asynchronously (0) or synchronously (1).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da03f-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da03f-132">Remarks</span></span>

<span data-ttu-id="da03f-133">Sie sollten in der Regel Sounds asynchron wiedergegeben werden sollen, damit Visio fortgeführt werden kann, während es der Sound wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="da03f-133">You should usually play sounds asynchronously so that Visio can continue processing while it plays the sound.</span></span> <span data-ttu-id="da03f-134">Mehrere Sounds hintereinander abspielen möchten, deren synchron oder einige möglicherweise nicht wiedergegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="da03f-134">To string several sounds together, play them synchronously, or some might fail to play.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="da03f-135">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="da03f-135">Example 1</span></span>

<span data-ttu-id="da03f-136">PLAYSOUND("chord.wav", 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="da03f-136">PLAYSOUND("chord.wav", 0, 0, 0)</span></span>
  
<span data-ttu-id="da03f-137">Spielt die Wave-Datei chord.wav asynchron und ohne akustische Warnung ab.</span><span class="sxs-lookup"><span data-stu-id="da03f-137">Plays the wave audio file chord.wav asynchronously with no warning beep.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="da03f-138">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="da03f-138">Example 2</span></span>

<span data-ttu-id="da03f-139">PLAYSOUND("Systemklang", 1, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="da03f-139">PLAYSOUND("SystemExclamation", 1, 0, 0)</span></span>
  
<span data-ttu-id="da03f-140">Spielt das Systemsignal für Hinweise asynchron und ohne akustische Warnung ab.</span><span class="sxs-lookup"><span data-stu-id="da03f-140">Plays the system exclamation sound asynchronously with no warning beep.</span></span>
  

