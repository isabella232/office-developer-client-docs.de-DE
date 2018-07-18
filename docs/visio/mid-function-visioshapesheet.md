---
title: MID Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027310
localization_priority: Normal
ms.assetid: 5041d957-1bd9-4d76-cf43-7b4fcd1e7dec
description: Gibt eine bestimmte Anzahl von Zeichen aus einer Textzeichenfolge zurückgegeben, beginnend bei der Position, die Sie angeben, die anhand der Anzahl der Zeichen, die Sie angeben.
ms.openlocfilehash: 96e697211ebf6ea61ddf0b749d8e1259f2a1e53d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797526"
---
# <a name="mid-function-visioshapesheet"></a><span data-ttu-id="2e528-103">MID Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="2e528-103">MID Function (VisioShapeSheet)</span></span>

<span data-ttu-id="2e528-104">Gibt eine bestimmte Anzahl von Zeichen aus einer Textzeichenfolge zurückgegeben, beginnend bei der Position, die Sie angeben, die anhand der Anzahl der Zeichen, die Sie angeben.</span><span class="sxs-lookup"><span data-stu-id="2e528-104">Returns a specific number of characters from a text string, starting at the position you specify, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="2e528-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e528-105">Syntax</span></span>

<span data-ttu-id="2e528-106">MID (** *Text* **, ** *Erstes_Zeichen* **, ** *Num_chars* **)</span><span class="sxs-lookup"><span data-stu-id="2e528-106">MID (** *text* **, ** *start_num* **, ** *num_chars* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2e528-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e528-107">Parameters</span></span>

|<span data-ttu-id="2e528-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2e528-108">**Name**</span></span>|<span data-ttu-id="2e528-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="2e528-109">**Required/Optional**</span></span>|<span data-ttu-id="2e528-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="2e528-110">**Data Type**</span></span>|<span data-ttu-id="2e528-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2e528-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2e528-112">_text_</span><span class="sxs-lookup"><span data-stu-id="2e528-112">_text_</span></span> <br/> |<span data-ttu-id="2e528-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2e528-113">Required</span></span>  <br/> |<span data-ttu-id="2e528-114">**String**</span><span class="sxs-lookup"><span data-stu-id="2e528-114">**String**</span></span> <br/> |<span data-ttu-id="2e528-115">Die Zeichenfolge mit den zu extrahierenden Zeichen.</span><span class="sxs-lookup"><span data-stu-id="2e528-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="2e528-116">_Erstes_Zeichen_</span><span class="sxs-lookup"><span data-stu-id="2e528-116">_start_num_</span></span> <br/> |<span data-ttu-id="2e528-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2e528-117">Required</span></span>  <br/> |<span data-ttu-id="2e528-118">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="2e528-118">**Number**</span></span> <br/> |<span data-ttu-id="2e528-p101">Die Position des ersten Zeichens, das extrahiert werden soll. Das erste Zeichen in der Zeichenfolge ist Position 1.</span><span class="sxs-lookup"><span data-stu-id="2e528-p101">The position of the first character you want to extract. The first character in the text string is position 1.</span></span>  <br/> |
| <span data-ttu-id="2e528-121">_Anzahl_Zeichen_</span><span class="sxs-lookup"><span data-stu-id="2e528-121">_num_chars_</span></span> <br/> |<span data-ttu-id="2e528-122">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2e528-122">Required</span></span>  <br/> |<span data-ttu-id="2e528-123">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="2e528-123">**Number**</span></span> <br/> |<span data-ttu-id="2e528-124">Die Anzahl der Zeichen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2e528-124">The number of characters to return.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2e528-125">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="2e528-125">Return value</span></span>

<span data-ttu-id="2e528-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2e528-126">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2e528-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e528-127">Remarks</span></span>

<span data-ttu-id="2e528-128">Wenn *start_num*</span><span class="sxs-lookup"><span data-stu-id="2e528-128">If  *start_num*  is:</span></span> 
  
- <span data-ttu-id="2e528-129">Größer als die Länge von *Text* , gibt MID "" (leere Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="2e528-129">Greater than the length of  *text*  , MID returns "" (empty text).</span></span> 
    
- <span data-ttu-id="2e528-130">Kleiner als die Länge von *Text* , aber *Start_num* plus *Num_chars* die Länge des *Textes* überschreitet, gibt MID die Zeichen bis zum Ende des *Texts* zurück.</span><span class="sxs-lookup"><span data-stu-id="2e528-130">Less than the length of  *text*  , but  *start_num*  plus  *num_chars*  exceeds the length of  *text*  , MID returns the characters up to the end of  *text*  .</span></span> 
    
- <span data-ttu-id="2e528-p102">kleiner als 1 ist, gibt MID den Fehlerwert #WERT! zurück.</span><span class="sxs-lookup"><span data-stu-id="2e528-p102">Less than 1, MID returns the #VALUE! error value.</span></span> 
    
<span data-ttu-id="2e528-133">Wenn *Num_chars* negativ ist, gibt MID den #VALUE!</span><span class="sxs-lookup"><span data-stu-id="2e528-133">If  *num_chars*  is negative, MID returns the #VALUE!</span></span> <span data-ttu-id="2e528-134">Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="2e528-134">error value.</span></span> 
  
## <a name="example"></a><span data-ttu-id="2e528-135">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2e528-135">Example</span></span>

<span data-ttu-id="2e528-136">MID ("SSN 999-99-9999",5,11)</span><span class="sxs-lookup"><span data-stu-id="2e528-136">MID ("SSN 999-99-9999",5,11)</span></span> 
  
<span data-ttu-id="2e528-137">Gibt 999-99-9999 zurück.</span><span class="sxs-lookup"><span data-stu-id="2e528-137">Returns 999-99-9999.</span></span> 
  

