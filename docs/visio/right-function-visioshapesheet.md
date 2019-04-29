---
title: RIGHT-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027314
localization_priority: Normal
ms.assetid: 910f0297-d588-2048-f308-03f3c2389bba
description: Gibt das letzte Zeichen in einer Textzeichenfolge basierend auf der Anzahl der Zeichen zurück, die Sie angeben.
ms.openlocfilehash: faf14ef55b34e51bac11129d6857e381d07357c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411456"
---
# <a name="right-function-visioshapesheet"></a><span data-ttu-id="255d4-103">RIGHT-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="255d4-103">RIGHT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="255d4-104">Gibt das letzte Zeichen in einer Textzeichenfolge basierend auf der Anzahl der Zeichen zurück, die Sie angeben.</span><span class="sxs-lookup"><span data-stu-id="255d4-104">Returns the last character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="255d4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="255d4-105">Syntax</span></span>

<span data-ttu-id="255d4-106">Rechts (\* \* *Text* \* \* [, \* \* *num_chars_opt* \* \*])</span><span class="sxs-lookup"><span data-stu-id="255d4-106">RIGHT(\*\* *text* \*\* [, \*\* *num_chars_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="255d4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="255d4-107">Parameters</span></span>

|<span data-ttu-id="255d4-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="255d4-108">**Name**</span></span>|<span data-ttu-id="255d4-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="255d4-109">**Required/Optional**</span></span>|<span data-ttu-id="255d4-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="255d4-110">**Data Type**</span></span>|<span data-ttu-id="255d4-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="255d4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="255d4-112">_text_</span><span class="sxs-lookup"><span data-stu-id="255d4-112">_text_</span></span> <br/> |<span data-ttu-id="255d4-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="255d4-113">Required</span></span>  <br/> |<span data-ttu-id="255d4-114">**String**</span><span class="sxs-lookup"><span data-stu-id="255d4-114">**String**</span></span> <br/> | <span data-ttu-id="255d4-115">Die Textzeichenfolge mit den zu extrahierenden Zeichen.</span><span class="sxs-lookup"><span data-stu-id="255d4-115">The text string containing the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="255d4-116">_num_chars_opt_</span><span class="sxs-lookup"><span data-stu-id="255d4-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="255d4-117">Optional</span><span class="sxs-lookup"><span data-stu-id="255d4-117">Optional</span></span>  <br/> |<span data-ttu-id="255d4-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="255d4-118">**Number**</span></span> <br/> |<span data-ttu-id="255d4-119">Die Anzahl der Zeichen, die extrahiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="255d4-119">The number of characters you want to extract.</span></span> <span data-ttu-id="255d4-120">Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="255d4-120">The default is 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="255d4-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="255d4-121">Return value</span></span>

<span data-ttu-id="255d4-122">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="255d4-122">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="255d4-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="255d4-123">Remarks</span></span>

<span data-ttu-id="255d4-124">Der Wert von _num_chars_opt_ muss größer oder gleich NULL (0) sein.</span><span class="sxs-lookup"><span data-stu-id="255d4-124">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="255d4-125">Wenn _num_chars_opt_ größer als die Länge des Texts ist, gibt right den gesamten Text zurück.</span><span class="sxs-lookup"><span data-stu-id="255d4-125">If  _num_chars_opt_ is greater than the length of the text, RIGHT returns all of the text.</span></span> <span data-ttu-id="255d4-126">Wenn _num_chars_opt_ ausgelassen wird, wird davon ausgegangen, dass es 1 ist.</span><span class="sxs-lookup"><span data-stu-id="255d4-126">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="255d4-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="255d4-127">Example</span></span>

<span data-ttu-id="255d4-128">RIGHT ("Januar 1, 2004", 4)</span><span class="sxs-lookup"><span data-stu-id="255d4-128">RIGHT ("January 1, 2004", 4)</span></span> 
  
<span data-ttu-id="255d4-129">Gibt den Wert 2004 zurück.</span><span class="sxs-lookup"><span data-stu-id="255d4-129">Returns the value 2004.</span></span> 
  

