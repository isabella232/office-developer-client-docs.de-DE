---
title: MID-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027310
localization_priority: Normal
ms.assetid: 5041d957-1bd9-4d76-cf43-7b4fcd1e7dec
description: Gibt eine bestimmte Anzahl von Zeichen aus einer Textzeichenfolge zurück, beginnend bei der angegebenen Position, basierend auf der Anzahl der Zeichen, die Sie angeben.
ms.openlocfilehash: 58d5e784e49c8e9fba0bf668626049298783c158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410266"
---
# <a name="mid-function-visioshapesheet"></a><span data-ttu-id="47f25-103">MID-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="47f25-103">MID Function (VisioShapeSheet)</span></span>

<span data-ttu-id="47f25-104">Gibt eine bestimmte Anzahl von Zeichen aus einer Textzeichenfolge zurück, beginnend bei der angegebenen Position, basierend auf der Anzahl der Zeichen, die Sie angeben.</span><span class="sxs-lookup"><span data-stu-id="47f25-104">Returns a specific number of characters from a text string, starting at the position you specify, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="47f25-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="47f25-105">Syntax</span></span>

<span data-ttu-id="47f25-106">MID (\* \* *Text* \* \*, \* \* *start_num* \* \*, \* \* *num_chars* \* \*)</span><span class="sxs-lookup"><span data-stu-id="47f25-106">MID (\*\* *text* \*\*, \*\* *start_num* \*\*, \*\* *num_chars* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="47f25-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="47f25-107">Parameters</span></span>

|<span data-ttu-id="47f25-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="47f25-108">**Name**</span></span>|<span data-ttu-id="47f25-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="47f25-109">**Required/Optional**</span></span>|<span data-ttu-id="47f25-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="47f25-110">**Data Type**</span></span>|<span data-ttu-id="47f25-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="47f25-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="47f25-112">_text_</span><span class="sxs-lookup"><span data-stu-id="47f25-112">_text_</span></span> <br/> |<span data-ttu-id="47f25-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="47f25-113">Required</span></span>  <br/> |<span data-ttu-id="47f25-114">**String**</span><span class="sxs-lookup"><span data-stu-id="47f25-114">**String**</span></span> <br/> |<span data-ttu-id="47f25-115">Die Zeichenfolge mit den zu extrahierenden Zeichen.</span><span class="sxs-lookup"><span data-stu-id="47f25-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="47f25-116">_start_num_</span><span class="sxs-lookup"><span data-stu-id="47f25-116">_start_num_</span></span> <br/> |<span data-ttu-id="47f25-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="47f25-117">Required</span></span>  <br/> |<span data-ttu-id="47f25-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="47f25-118">**Number**</span></span> <br/> |<span data-ttu-id="47f25-119">Die Position des ersten Zeichens, das extrahiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="47f25-119">The position of the first character you want to extract.</span></span> <span data-ttu-id="47f25-120">Das erste Zeichen in der Zeichenfolge ist Position 1.</span><span class="sxs-lookup"><span data-stu-id="47f25-120">The first character in the text string is position 1.</span></span>  <br/> |
| <span data-ttu-id="47f25-121">_num_chars_</span><span class="sxs-lookup"><span data-stu-id="47f25-121">_num_chars_</span></span> <br/> |<span data-ttu-id="47f25-122">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="47f25-122">Required</span></span>  <br/> |<span data-ttu-id="47f25-123">**Number**</span><span class="sxs-lookup"><span data-stu-id="47f25-123">**Number**</span></span> <br/> |<span data-ttu-id="47f25-124">Die Anzahl der Zeichen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="47f25-124">The number of characters to return.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="47f25-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47f25-125">Return value</span></span>

<span data-ttu-id="47f25-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="47f25-126">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="47f25-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47f25-127">Remarks</span></span>

<span data-ttu-id="47f25-128">Wenn *start_num* ist:</span><span class="sxs-lookup"><span data-stu-id="47f25-128">If  *start_num*  is:</span></span> 
  
- <span data-ttu-id="47f25-129">Größer als die Länge des *Texts* , Mid gibt "" (leeren Text) zurück.</span><span class="sxs-lookup"><span data-stu-id="47f25-129">Greater than the length of  *text*  , MID returns "" (empty text).</span></span> 
    
- <span data-ttu-id="47f25-130">Kleiner als die Länge des *Texts* , aber *start_num* Plus *num_chars* überschreitet die Länge \*\* des Texts, Mid gibt die Zeichen bis zum Ende des *Texts* zurück.</span><span class="sxs-lookup"><span data-stu-id="47f25-130">Less than the length of  *text*  , but  *start_num*  plus  *num_chars*  exceeds the length of  *text*  , MID returns the characters up to the end of  *text*  .</span></span> 
    
- <span data-ttu-id="47f25-131">kleiner als 1 ist, gibt MID den Fehlerwert #WERT!</span><span class="sxs-lookup"><span data-stu-id="47f25-131">Less than 1, MID returns the #VALUE!</span></span> <span data-ttu-id="47f25-132">zurück.</span><span class="sxs-lookup"><span data-stu-id="47f25-132">error value.</span></span> 
    
<span data-ttu-id="47f25-133">Wenn *num_chars* negativ ist, gibt MID den #VALUE zurück.</span><span class="sxs-lookup"><span data-stu-id="47f25-133">If  *num_chars*  is negative, MID returns the #VALUE!</span></span> <span data-ttu-id="47f25-134">zurück.</span><span class="sxs-lookup"><span data-stu-id="47f25-134">error value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="47f25-135">Beispiel</span><span class="sxs-lookup"><span data-stu-id="47f25-135">Example</span></span>

<span data-ttu-id="47f25-136">MID ("SSN 999-99-9999",5,11)</span><span class="sxs-lookup"><span data-stu-id="47f25-136">MID ("SSN 999-99-9999",5,11)</span></span> 
  
<span data-ttu-id="47f25-137">Gibt 999-99-9999 zurück.</span><span class="sxs-lookup"><span data-stu-id="47f25-137">Returns 999-99-9999.</span></span> 
  

