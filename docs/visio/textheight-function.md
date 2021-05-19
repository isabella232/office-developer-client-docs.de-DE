---
title: TEXTHEIGHT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251504
localization_priority: Normal
ms.assetid: 5a10892f-c8fa-c127-2f5a-564009ce5411
description: Gibt die Höhe des zusammengesetzten Texts in einer Form zurück, in der keine Textzeile den maximalen Gesamtwert überschreitet.
ms.openlocfilehash: 7455f58f14f9a4a0ae1fcd5375dba5d5860d3852
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427409"
---
# <a name="textheight-function"></a><span data-ttu-id="6f11f-103">TEXTHÖHE-Funktion</span><span class="sxs-lookup"><span data-stu-id="6f11f-103">TEXTHEIGHT Function</span></span>

<span data-ttu-id="6f11f-104">Gibt die Höhe des zusammengesetzten Texts in einer Form zurück, in der keine Textzeile den _maximalen Wert überschreitet._</span><span class="sxs-lookup"><span data-stu-id="6f11f-104">Returns the height of the composed text in a shape where no text line exceeds  _maximumwidth_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6f11f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f11f-105">Syntax</span></span>

<span data-ttu-id="6f11f-106">TEXTHEIGHT(\*\* *shapename! TheText* \*\* \*\* *[,maximumwidth]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="6f11f-106">TEXTHEIGHT(\*\* *shapename!TheText* \*\* \*\* *[,maximumwidth]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6f11f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f11f-107">Parameters</span></span>

|<span data-ttu-id="6f11f-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="6f11f-108">**Name**</span></span>|<span data-ttu-id="6f11f-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="6f11f-109">**Required/Optional**</span></span>|<span data-ttu-id="6f11f-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="6f11f-110">**Data Type**</span></span>|<span data-ttu-id="6f11f-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6f11f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6f11f-112">_shapename!theText_</span><span class="sxs-lookup"><span data-stu-id="6f11f-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="6f11f-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="6f11f-113">Required</span></span>  <br/> |<span data-ttu-id="6f11f-114">**String**</span><span class="sxs-lookup"><span data-stu-id="6f11f-114">**String**</span></span> <br/> |<span data-ttu-id="6f11f-115">Ein Verweis auf die Zelle mit dem Namen TheText in der Zielform.</span><span class="sxs-lookup"><span data-stu-id="6f11f-115">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="6f11f-116">_shapename!_</span><span class="sxs-lookup"><span data-stu-id="6f11f-116">_shapename!_</span></span> <span data-ttu-id="6f11f-117">ist der Name der Form, aus der Sie den Text abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="6f11f-117">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="6f11f-118">_maximumwidth_</span><span class="sxs-lookup"><span data-stu-id="6f11f-118">_maximumwidth_</span></span> <br/> |<span data-ttu-id="6f11f-119">Optional.</span><span class="sxs-lookup"><span data-stu-id="6f11f-119">Optional</span></span>  <br/> |<span data-ttu-id="6f11f-120">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="6f11f-120">**Numeric**</span></span> <br/> |<span data-ttu-id="6f11f-121">Die maximale Breite eines Textblocks.</span><span class="sxs-lookup"><span data-stu-id="6f11f-121">The maximum width of the text block.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6f11f-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f11f-122">Return value</span></span>

<span data-ttu-id="6f11f-123">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6f11f-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6f11f-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6f11f-124">Remarks</span></span>

<span data-ttu-id="6f11f-p102">Der zurückgegebene Wert enthält die Höhe des Texts einschließlich der Abstände vor und hinter dem Text, des Zeilenabstands im Text und der oberen und unteren Textblockränder. Diese Funktion wird meistens verwendet, um die Höhe eines Shapes so anzupassen, dass der gesamte Text vollständig dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6f11f-p102">The returned value includes the height of the text including the space before and after text, the line spacing in text, and the top and bottom text block margins. This function is commonly used to adjust the height of a shape to fit the text it contains.</span></span>
  
## <a name="example"></a><span data-ttu-id="6f11f-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6f11f-127">Example</span></span>

<span data-ttu-id="6f11f-128">TEXTHEIGHT(TheText,(Width - 0.5 in))</span><span class="sxs-lookup"><span data-stu-id="6f11f-128">TEXTHEIGHT(TheText,(Width - 0.5 in))</span></span> 
  
<span data-ttu-id="6f11f-129">Gibt die Texthöhe zurück, wenn der Text auf die Breite des Shapes abzüglich 0,5 Zoll umgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="6f11f-129">Returns the height of the text when wrapped to the width of the shape minus 0.5 inches.</span></span> 
  

