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
description: Gibt die Höhe des zusammengesetzten Texts in einem Shape zurück, in dem keine Textzeile maxBreite überschreitet.
ms.openlocfilehash: 9a80dafcf80a1dcba968a0f60465aae4e2a2758b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798252"
---
# <a name="textheight-function"></a><span data-ttu-id="d495c-103">TEXTHEIGHT Function</span><span class="sxs-lookup"><span data-stu-id="d495c-103">TEXTHEIGHT Function</span></span>

<span data-ttu-id="d495c-104">Gibt die Höhe des zusammengesetzten Texts in einem Shape zurück, in dem keine Textzeile _maxBreite_überschreitet.</span><span class="sxs-lookup"><span data-stu-id="d495c-104">Returns the height of the composed text in a shape where no text line exceeds  _maximumwidth_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d495c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d495c-105">Syntax</span></span>

<span data-ttu-id="d495c-106">TEXTHEIGHT (** *Shapename! TheText* ** ** *[, maxBreite]* **)</span><span class="sxs-lookup"><span data-stu-id="d495c-106">TEXTHEIGHT(** *shapename!TheText* ** ** *[,maximumwidth]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d495c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d495c-107">Parameters</span></span>

|<span data-ttu-id="d495c-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="d495c-108">**Name**</span></span>|<span data-ttu-id="d495c-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="d495c-109">**Required/Optional**</span></span>|<span data-ttu-id="d495c-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="d495c-110">**Data Type**</span></span>|<span data-ttu-id="d495c-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d495c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d495c-112">_Shapename! TheText_</span><span class="sxs-lookup"><span data-stu-id="d495c-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="d495c-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d495c-113">Required</span></span>  <br/> |<span data-ttu-id="d495c-114">**String**</span><span class="sxs-lookup"><span data-stu-id="d495c-114">**String**</span></span> <br/> |<span data-ttu-id="d495c-115">Ein Verweis auf die Zelle TheText mit der in der Ziel-Shape.</span><span class="sxs-lookup"><span data-stu-id="d495c-115">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="d495c-116">_Shapename!_</span><span class="sxs-lookup"><span data-stu-id="d495c-116">_shapename!_</span></span> <span data-ttu-id="d495c-117">ist der Name des Shapes, von dem Sie den Text abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="d495c-117">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="d495c-118">_maxBreite_</span><span class="sxs-lookup"><span data-stu-id="d495c-118">_maximumwidth_</span></span> <br/> |<span data-ttu-id="d495c-119">Optional</span><span class="sxs-lookup"><span data-stu-id="d495c-119">Optional</span></span>  <br/> |<span data-ttu-id="d495c-120">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="d495c-120">**Numeric**</span></span> <br/> |<span data-ttu-id="d495c-121">Die maximale Breite eines Textblocks.</span><span class="sxs-lookup"><span data-stu-id="d495c-121">The maximum width of the text block.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d495c-122">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="d495c-122">Return value</span></span>

<span data-ttu-id="d495c-123">String</span><span class="sxs-lookup"><span data-stu-id="d495c-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d495c-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d495c-124">Remarks</span></span>

<span data-ttu-id="d495c-p102">Der zurückgegebene Wert enthält die Höhe des Texts einschließlich der Abstände vor und hinter dem Text, des Zeilenabstands im Text und der oberen und unteren Textblockränder. Diese Funktion wird meistens verwendet, um die Höhe eines Shapes so anzupassen, dass der gesamte Text vollständig dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d495c-p102">The returned value includes the height of the text including the space before and after text, the line spacing in text, and the top and bottom text block margins. This function is commonly used to adjust the height of a shape to fit the text it contains.</span></span>
  
## <a name="example"></a><span data-ttu-id="d495c-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d495c-127">Example</span></span>

<span data-ttu-id="d495c-128">TEXTHEIGHT(TheText,(Width - 0.5 in))</span><span class="sxs-lookup"><span data-stu-id="d495c-128">TEXTHEIGHT(TheText,(Width - 0.5 in))</span></span> 
  
<span data-ttu-id="d495c-129">Gibt die Texthöhe zurück, wenn der Text auf die Breite des Shapes abzüglich 0,5 Zoll umgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="d495c-129">Returns the height of the text when wrapped to the width of the shape minus 0.5 inches.</span></span> 
  

