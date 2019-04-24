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
description: Ersetzt einen Teil einer Textzeichenfolge durch eine andere Textzeichenfolge.
ms.openlocfilehash: fc12ab30ec9c509e2f126931bee837f518e96f3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346823"
---
# <a name="substitute-function"></a><span data-ttu-id="b328d-103">SUBSTITUTE Function</span><span class="sxs-lookup"><span data-stu-id="b328d-103">SUBSTITUTE Function</span></span>

<span data-ttu-id="b328d-104">Ersetzt einen Teil einer Textzeichenfolge durch eine andere Textzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b328d-104">Replaces part of a text string with a different text string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b328d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b328d-105">Syntax</span></span>

 <span data-ttu-id="b328d-106">Ersatz (\* \* *Text* \* \*, \* \* *old_text* \* \*, \* \* *new_text* \* \* [, \* \* *start_num* \* \*] [, \* \* *ignore_case_opt* \* \*)</span><span class="sxs-lookup"><span data-stu-id="b328d-106">SUBSTITUTE (\*\* *text* \*\*, \*\* *old_text* \*\*, \*\* *new_text* \*\* [, \*\* *start_num* \*\* ][, \*\* *ignore_case_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b328d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b328d-107">Parameters</span></span>

|<span data-ttu-id="b328d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="b328d-108">**Name**</span></span>|<span data-ttu-id="b328d-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="b328d-109">**Required/Optional**</span></span>|<span data-ttu-id="b328d-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="b328d-110">**Data Type**</span></span>|<span data-ttu-id="b328d-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b328d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b328d-112">_text_</span><span class="sxs-lookup"><span data-stu-id="b328d-112">_text_</span></span> <br/> |<span data-ttu-id="b328d-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b328d-113">Required</span></span>  <br/> |<span data-ttu-id="b328d-114">**String**</span><span class="sxs-lookup"><span data-stu-id="b328d-114">**String**</span></span> <br/> | <span data-ttu-id="b328d-115">Der Text oder der Bezug auf eine Zelle mit dem Text, in dem Zeichen ersetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b328d-115">The text or the reference to a cell containing text for which you want to substitute characters.</span></span>  <br/> |
| <span data-ttu-id="b328d-116">_old_text_</span><span class="sxs-lookup"><span data-stu-id="b328d-116">_old_text_</span></span> <br/> |<span data-ttu-id="b328d-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b328d-117">Required</span></span>  <br/> |<span data-ttu-id="b328d-118">**String**</span><span class="sxs-lookup"><span data-stu-id="b328d-118">**String**</span></span> <br/> | <span data-ttu-id="b328d-119">Der Text, der ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b328d-119">The text you want to replace.</span></span>  <br/> |
| <span data-ttu-id="b328d-120">_new_text_</span><span class="sxs-lookup"><span data-stu-id="b328d-120">_new_text_</span></span> <br/> |<span data-ttu-id="b328d-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b328d-121">Required</span></span>  <br/> |<span data-ttu-id="b328d-122">**String**</span><span class="sxs-lookup"><span data-stu-id="b328d-122">**String**</span></span> <br/> | <span data-ttu-id="b328d-123">Der Text, den Sie zum Ersetzen von _old_text_verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="b328d-123">The text you want to use to replace  _old_text_.</span></span>  <br/> |
| <span data-ttu-id="b328d-124">_start_num_opt_</span><span class="sxs-lookup"><span data-stu-id="b328d-124">_start_num_opt_</span></span> <br/> |<span data-ttu-id="b328d-125">Optional</span><span class="sxs-lookup"><span data-stu-id="b328d-125">Optional</span></span>  <br/> |<span data-ttu-id="b328d-126">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="b328d-126">**Numeric**</span></span> <br/> |<span data-ttu-id="b328d-127">Gibt an, welche Vorkommen von old_text ersetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b328d-127">Specifies which occurrences of old_text to replace.</span></span>  <br/> |
| <span data-ttu-id="b328d-128">_ignore_case_opt_</span><span class="sxs-lookup"><span data-stu-id="b328d-128">_ignore_case_opt_</span></span> <br/> |<span data-ttu-id="b328d-129">Optional</span><span class="sxs-lookup"><span data-stu-id="b328d-129">Optional</span></span>  <br/> |<span data-ttu-id="b328d-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="b328d-130">**Boolean**</span></span> <br/> |<span data-ttu-id="b328d-131">FALSE, wenn Groß- und Kleinschreibung zu beachten ist; andernfalls TRUE.</span><span class="sxs-lookup"><span data-stu-id="b328d-131">FALSE if case-sensitive; otherwise, TRUE.</span></span> <span data-ttu-id="b328d-132">Die Standardeinstellung ist FALSE.</span><span class="sxs-lookup"><span data-stu-id="b328d-132">The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b328d-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b328d-133">Return value</span></span>

<span data-ttu-id="b328d-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b328d-134">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b328d-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b328d-135">Remarks</span></span>

 <span data-ttu-id="b328d-136">Wenn Sie _start_num_opt_angeben, wird nur das Vorkommen von _old_text_ ersetzt.</span><span class="sxs-lookup"><span data-stu-id="b328d-136">If you specify  _start_num_opt_, only that occurrence of  _old_text_ is replaced.</span></span> <span data-ttu-id="b328d-137">Andernfalls wird jedes Vorkommen von _old_text_ in _Text_ in new_text geändert _._</span><span class="sxs-lookup"><span data-stu-id="b328d-137">Otherwise, every occurrence of  _old_text_ in  _text_ is changed to  _new_text._</span></span>
  
<span data-ttu-id="b328d-138">Verwenden Sie die SUBSTITUTE-Funktion, wenn bestimmter Text in einer Zeichenfolge ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b328d-138">Use the SUBSTITUTE function when you want to replace specific text in a text string.</span></span> <span data-ttu-id="b328d-139">Wenn Sie Text ersetzen möchten, der an einer bestimmten Stelle in einer Textzeichenfolge vorkommt, verwenden Sie die REPLACE-Funktion.</span><span class="sxs-lookup"><span data-stu-id="b328d-139">If you want to replace text that occurs in a specific location in a text string, use the REPLACE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="b328d-140">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b328d-140">Example</span></span>

<span data-ttu-id="b328d-141">SUBSTITUTE ("1 January 2003", "January", "JAN")</span><span class="sxs-lookup"><span data-stu-id="b328d-141">SUBSTITUTE ("1 January 2003", "January", "JAN")</span></span> 
  
<span data-ttu-id="b328d-142">Gibt "1 JAN 2003" zurück.</span><span class="sxs-lookup"><span data-stu-id="b328d-142">Returns "1 JAN 2003".</span></span> 
  
<span data-ttu-id="b328d-143">SUBSTITUTE ("1 January 2003","january","JAN")</span><span class="sxs-lookup"><span data-stu-id="b328d-143">SUBSTITUTE ("1 January 2003","january","JAN")</span></span> 
  
<span data-ttu-id="b328d-144">Gibt "1 January 2003" zurück.</span><span class="sxs-lookup"><span data-stu-id="b328d-144">Returns "1 January 2003".</span></span> <span data-ttu-id="b328d-145">Es wurde keine Änderung durchgeführt, da bei der Textsuche zwischen Groß- und Kleinschreibung unterschieden wird.</span><span class="sxs-lookup"><span data-stu-id="b328d-145">No change is made because the text search is case-sensitive.</span></span> 
  

