---
title: TEXTWIDTH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251505
localization_priority: Normal
ms.assetid: a9b8efcf-edc0-ad99-deae-21df16c58807
description: Gibt die Breite des zusammengesetzten Texts in einer Form zurück.
ms.openlocfilehash: 43848bba4d24a0c31a3a084d123cd56140bf0709
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422033"
---
# <a name="textwidth-function"></a><span data-ttu-id="7ad90-103">TEXTWIDTH Function</span><span class="sxs-lookup"><span data-stu-id="7ad90-103">TEXTWIDTH Function</span></span>

<span data-ttu-id="7ad90-104">Gibt die Breite des zusammengesetzten Texts in einer Form zurück.</span><span class="sxs-lookup"><span data-stu-id="7ad90-104">Returns the width of the composed text in a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7ad90-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ad90-105">Syntax</span></span>

<span data-ttu-id="7ad90-106">TEXTWIDTH(\*\* *shapename! TheText* \*\* \*\* *[,maximumwidth]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="7ad90-106">TEXTWIDTH(\*\* *shapename!TheText* \*\* \*\* *[,maximumwidth]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7ad90-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ad90-107">Parameters</span></span>

|<span data-ttu-id="7ad90-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="7ad90-108">**Name**</span></span>|<span data-ttu-id="7ad90-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="7ad90-109">**Required/Optional**</span></span>|<span data-ttu-id="7ad90-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="7ad90-110">**Data Type**</span></span>|<span data-ttu-id="7ad90-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7ad90-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7ad90-112">_shapename!theText_</span><span class="sxs-lookup"><span data-stu-id="7ad90-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="7ad90-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="7ad90-113">Required</span></span>  <br/> |<span data-ttu-id="7ad90-114">**String**</span><span class="sxs-lookup"><span data-stu-id="7ad90-114">**String**</span></span> <br/> |<span data-ttu-id="7ad90-115">Ein Verweis auf die Zelle mit dem Namen TheText in der Zielform.</span><span class="sxs-lookup"><span data-stu-id="7ad90-115">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="7ad90-116">_shapename!_</span><span class="sxs-lookup"><span data-stu-id="7ad90-116">_shapename!_</span></span> <span data-ttu-id="7ad90-117">ist der Name der Form, aus der Sie den Text abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="7ad90-117">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="7ad90-118">_maximumwidth_</span><span class="sxs-lookup"><span data-stu-id="7ad90-118">_maximumwidth_</span></span> <br/> |<span data-ttu-id="7ad90-119">Optional.</span><span class="sxs-lookup"><span data-stu-id="7ad90-119">Optional</span></span>  <br/> |<span data-ttu-id="7ad90-120">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="7ad90-120">**Numeric**</span></span> <br/> |<span data-ttu-id="7ad90-121">Die maximale Breite eines Textblocks.</span><span class="sxs-lookup"><span data-stu-id="7ad90-121">The maximum width of the text block.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="7ad90-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7ad90-122">Return value</span></span>

<span data-ttu-id="7ad90-123">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7ad90-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7ad90-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7ad90-124">Remarks</span></span>

<span data-ttu-id="7ad90-125">Die TEXTWIDTH-Funktion wird meistens verwendet, um die Breite eines Shapes so anzupassen, dass der enthaltene Text vollständig hineinpasst.</span><span class="sxs-lookup"><span data-stu-id="7ad90-125">The TEXTWIDTH function is commonly used to adjust the width of a shape to fit the text it contains.</span></span>
  
<span data-ttu-id="7ad90-126">Wenn  _sheetN!_</span><span class="sxs-lookup"><span data-stu-id="7ad90-126">If  _sheetN!_</span></span> <span data-ttu-id="7ad90-127">wird nicht angegeben, ist die Standardform die aktuelle Form.</span><span class="sxs-lookup"><span data-stu-id="7ad90-127">is omitted, the default shape is the current shape.</span></span> 
  
<span data-ttu-id="7ad90-128">Wenn _maximumwidth_ angegeben wird, ist das Ergebnis die längste Textzeile, die innerhalb von _Maximumwidth liegt._</span><span class="sxs-lookup"><span data-stu-id="7ad90-128">If  _maximumwidth_ is specified, the result is the longest line of text that fits within  _maximumwidth_.</span></span> <span data-ttu-id="7ad90-129">Wenn  _maximumwidth_ nicht angegeben wird, ist das Ergebnis die Gesamtbreite des Texts.</span><span class="sxs-lookup"><span data-stu-id="7ad90-129">If  _maximumwidth_ is omitted, the result is the total width of the text.</span></span> 
  
## <a name="example"></a><span data-ttu-id="7ad90-130">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7ad90-130">Example</span></span>

<span data-ttu-id="7ad90-131">TEXTWIDTH(TheText)</span><span class="sxs-lookup"><span data-stu-id="7ad90-131">TEXTWIDTH(TheText)</span></span> 
  
<span data-ttu-id="7ad90-132">Gibt die Gesamtlänge des Texts im aktuellen Shape zurück.</span><span class="sxs-lookup"><span data-stu-id="7ad90-132">Returns the total length of the text in the current shape.</span></span> 
  

