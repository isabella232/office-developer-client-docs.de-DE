---
title: SUBSTITUTE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60115
localization_priority: Normal
ms.assetid: 4a27663a-9d37-2ac4-5856-edeb0880f16e
description: Ersetzt einen Teil einer Zeichenfolge durch eine andere Textzeichenfolge.
ms.openlocfilehash: 2c33d8aafbd68054ac39d14bb4fb3cf857fb367e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798216"
---
# <a name="substitute-function"></a><span data-ttu-id="41e27-103">SUBSTITUTE Function</span><span class="sxs-lookup"><span data-stu-id="41e27-103">SUBSTITUTE Function</span></span>

<span data-ttu-id="41e27-104">Ersetzt einen Teil einer Zeichenfolge durch eine andere Textzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="41e27-104">Replaces part of a text string with a different text string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="41e27-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="41e27-105">Syntax</span></span>

 <span data-ttu-id="41e27-106">Ersatz (** *Text* **, ** *Alter_Text* **, ** *Neuer_Text* ** [, ** *Erstes_Zeichen* **] [, ** *Ignore_case_opt* **)</span><span class="sxs-lookup"><span data-stu-id="41e27-106">SUBSTITUTE (** *text* **, ** *old_text* **, ** *new_text* ** [, ** *start_num* ** ][, ** *ignore_case_opt* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="41e27-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="41e27-107">Parameters</span></span>

|<span data-ttu-id="41e27-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="41e27-108">**Name**</span></span>|<span data-ttu-id="41e27-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="41e27-109">**Required/Optional**</span></span>|<span data-ttu-id="41e27-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="41e27-110">**Data Type**</span></span>|<span data-ttu-id="41e27-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="41e27-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="41e27-112">_text_</span><span class="sxs-lookup"><span data-stu-id="41e27-112">_text_</span></span> <br/> |<span data-ttu-id="41e27-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="41e27-113">Required</span></span>  <br/> |<span data-ttu-id="41e27-114">**String**</span><span class="sxs-lookup"><span data-stu-id="41e27-114">**String**</span></span> <br/> | <span data-ttu-id="41e27-115">Der Text oder der Bezug auf eine Zelle mit dem Text, in dem Zeichen ersetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="41e27-115">The text or the reference to a cell containing text for which you want to substitute characters.</span></span>  <br/> |
| <span data-ttu-id="41e27-116">_Alter_Text_</span><span class="sxs-lookup"><span data-stu-id="41e27-116">_old_text_</span></span> <br/> |<span data-ttu-id="41e27-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="41e27-117">Required</span></span>  <br/> |<span data-ttu-id="41e27-118">**String**</span><span class="sxs-lookup"><span data-stu-id="41e27-118">**String**</span></span> <br/> | <span data-ttu-id="41e27-119">Der Text, der ersetzt werden soll.
</span><span class="sxs-lookup"><span data-stu-id="41e27-119">The text you want to replace.</span></span>  <br/> |
| <span data-ttu-id="41e27-120">_Neuer_Text_</span><span class="sxs-lookup"><span data-stu-id="41e27-120">_new_text_</span></span> <br/> |<span data-ttu-id="41e27-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="41e27-121">Required</span></span>  <br/> |<span data-ttu-id="41e27-122">**String**</span><span class="sxs-lookup"><span data-stu-id="41e27-122">**String**</span></span> <br/> | <span data-ttu-id="41e27-123">Der Text, den Sie _Alter_Text_ersetzen möchten.</span><span class="sxs-lookup"><span data-stu-id="41e27-123">The text you want to use to replace  _old_text_.</span></span>  <br/> |
| <span data-ttu-id="41e27-124">_start_num_opt_</span><span class="sxs-lookup"><span data-stu-id="41e27-124">_start_num_opt_</span></span> <br/> |<span data-ttu-id="41e27-125">Optional</span><span class="sxs-lookup"><span data-stu-id="41e27-125">Optional</span></span>  <br/> |<span data-ttu-id="41e27-126">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="41e27-126">**Numeric**</span></span> <br/> |<span data-ttu-id="41e27-127">Gibt an, welche Vorkommen von old_text ersetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="41e27-127">Specifies which occurences of old_text to replace.</span></span>  <br/> |
| <span data-ttu-id="41e27-128">_ignore_case_opt_</span><span class="sxs-lookup"><span data-stu-id="41e27-128">_ignore_case_opt_</span></span> <br/> |<span data-ttu-id="41e27-129">Optional</span><span class="sxs-lookup"><span data-stu-id="41e27-129">Optional</span></span>  <br/> |<span data-ttu-id="41e27-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="41e27-130">**Boolean**</span></span> <br/> |<span data-ttu-id="41e27-p101">FALSE, wenn Groß- und Kleinschreibung zu beachten ist; andernfalls TRUE. Die Standardeinstellung ist FALSE.</span><span class="sxs-lookup"><span data-stu-id="41e27-p101">FALSE if case-sensitive; otherwise, TRUE. The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="41e27-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41e27-133">Return value</span></span>

<span data-ttu-id="41e27-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="41e27-134">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="41e27-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41e27-135">Remarks</span></span>

 <span data-ttu-id="41e27-136">Wenn Sie _Start_num_opt_angeben, wird nur dieses Auftreten von _Old_text_ ersetzt.</span><span class="sxs-lookup"><span data-stu-id="41e27-136">If you specify  _start_num_opt_, only that occurrence of  _old_text_ is replaced.</span></span> <span data-ttu-id="41e27-137">Andernfalls wird jedes Vorkommen von _Old_text_ in _Text_ um geändert _Neuer_Text._</span><span class="sxs-lookup"><span data-stu-id="41e27-137">Otherwise, every occurrence of  _old_text_ in  _text_ is changed to  _new_text._</span></span>
  
<span data-ttu-id="41e27-138">Verwenden Sie die Ersatz-Funktion, wenn Sie bestimmten Text in einer Zeichenfolge ersetzen möchten.</span><span class="sxs-lookup"><span data-stu-id="41e27-138">Use the SUBSTITUTE function when you want to replace specific text in a text string.</span></span> <span data-ttu-id="41e27-139">Wenn Text zu ersetzen, das auftritt, an einer bestimmten Stelle in einer Textzeichenfolge zurückgegeben werden soll, verwenden Sie die REPLACE-Funktion.</span><span class="sxs-lookup"><span data-stu-id="41e27-139">If you want to replace text that occurs in a specific location in a text string, use the REPLACE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="41e27-140">Beispiel</span><span class="sxs-lookup"><span data-stu-id="41e27-140">Example</span></span>

<span data-ttu-id="41e27-141">SUBSTITUTE ("1 January 2003", "January", "JAN")</span><span class="sxs-lookup"><span data-stu-id="41e27-141">SUBSTITUTE ("1 January 2003", "January", "JAN")</span></span> 
  
<span data-ttu-id="41e27-142">Gibt "1 JAN 2003" zurück.</span><span class="sxs-lookup"><span data-stu-id="41e27-142">Returns "1 JAN 2003".</span></span> 
  
<span data-ttu-id="41e27-143">SUBSTITUTE ("1 January 2003","january","JAN")</span><span class="sxs-lookup"><span data-stu-id="41e27-143">SUBSTITUTE ("1 January 2003","january","JAN")</span></span> 
  
<span data-ttu-id="41e27-144">Gibt "1. Januar 2003" zurück.</span><span class="sxs-lookup"><span data-stu-id="41e27-144">Returns "1 January 2003".</span></span> <span data-ttu-id="41e27-145">Keine Änderung erfolgt, da die Textsuche Groß-/Kleinschreibung beachtet wird.</span><span class="sxs-lookup"><span data-stu-id="41e27-145">No change is made because the text search is case-sensitive.</span></span> 
  

