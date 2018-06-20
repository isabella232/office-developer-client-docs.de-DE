---
title: RIGHT Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027314
localization_priority: Normal
ms.assetid: 910f0297-d588-2048-f308-03f3c2389bba
description: Gibt das letzte Zeichen oder Zeichen in einer Textzeichenfolge, basierend auf der Anzahl der Zeichen an, die Sie angeben.
ms.openlocfilehash: e35cc4918809d5f134f9519c01cb3c93407258e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797855"
---
# <a name="right-function-visioshapesheet"></a><span data-ttu-id="50049-103">RIGHT Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="50049-103">RIGHT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="50049-104">Gibt das letzte Zeichen oder Zeichen in einer Textzeichenfolge, basierend auf der Anzahl der Zeichen an, die Sie angeben.</span><span class="sxs-lookup"><span data-stu-id="50049-104">Returns the last character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="50049-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="50049-105">Syntax</span></span>

<span data-ttu-id="50049-106">RECHTS (** *Text* ** [, ** *Num_chars_opt* **])</span><span class="sxs-lookup"><span data-stu-id="50049-106">RIGHT(** *text* ** [, ** *num_chars_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="50049-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="50049-107">Parameters</span></span>

|<span data-ttu-id="50049-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="50049-108">**Name**</span></span>|<span data-ttu-id="50049-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="50049-109">**Required/Optional**</span></span>|<span data-ttu-id="50049-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="50049-110">**Data Type**</span></span>|<span data-ttu-id="50049-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="50049-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="50049-112">_text_</span><span class="sxs-lookup"><span data-stu-id="50049-112">_text_</span></span> <br/> |<span data-ttu-id="50049-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="50049-113">Required</span></span>  <br/> |<span data-ttu-id="50049-114">**String**</span><span class="sxs-lookup"><span data-stu-id="50049-114">**String**</span></span> <br/> | <span data-ttu-id="50049-115">Die Textzeichenfolge mit den zu extrahierenden Zeichen.</span><span class="sxs-lookup"><span data-stu-id="50049-115">The text string containing the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="50049-116">_num_chars_opt_</span><span class="sxs-lookup"><span data-stu-id="50049-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="50049-117">Optional</span><span class="sxs-lookup"><span data-stu-id="50049-117">Optional</span></span>  <br/> |<span data-ttu-id="50049-118">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="50049-118">**Number**</span></span> <br/> |<span data-ttu-id="50049-p101">Die Anzahl der Zeichen, die extrahiert werden sollen. Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="50049-p101">The number of characters you want to extract. The default is 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="50049-121">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="50049-121">Return value</span></span>

<span data-ttu-id="50049-122">String</span><span class="sxs-lookup"><span data-stu-id="50049-122">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="50049-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="50049-123">Remarks</span></span>

<span data-ttu-id="50049-124">Der Wert von _Num_chars_opt_ muss größer als oder gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="50049-124">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="50049-125">Wenn _Num_chars_opt_ größer als die Länge des Texts ist, gibt rechts des gesamten Texts.</span><span class="sxs-lookup"><span data-stu-id="50049-125">If  _num_chars_opt_ is greater than the length of the text, RIGHT returns all of the text.</span></span> <span data-ttu-id="50049-126">Wenn _Num_chars_opt_ ausgelassen wird, wird angenommen, 1 sein.</span><span class="sxs-lookup"><span data-stu-id="50049-126">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="50049-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="50049-127">Example</span></span>

<span data-ttu-id="50049-128">RIGHT ("Januar 1, 2004", 4)</span><span class="sxs-lookup"><span data-stu-id="50049-128">RIGHT ("January 1, 2004", 4)</span></span> 
  
<span data-ttu-id="50049-129">Gibt den Wert 2004 zurück.</span><span class="sxs-lookup"><span data-stu-id="50049-129">Returns the value 2004.</span></span> 
  

