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
description: Gibt die Breite des zusammengesetzten Texts in einem Shape zurück.
ms.openlocfilehash: d96b9489c08ce38205f8e9ad91e361fcb643c39c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798250"
---
# <a name="textwidth-function"></a><span data-ttu-id="772c1-103">TEXTWIDTH Function</span><span class="sxs-lookup"><span data-stu-id="772c1-103">TEXTWIDTH Function</span></span>

<span data-ttu-id="772c1-104">Gibt die Breite des zusammengesetzten Texts in einem Shape zurück.</span><span class="sxs-lookup"><span data-stu-id="772c1-104">Returns the width of the composed text in a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="772c1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="772c1-105">Syntax</span></span>

<span data-ttu-id="772c1-106">TEXTWIDTH (** *Shapename! TheText* ** ** *[, maxBreite]* **)</span><span class="sxs-lookup"><span data-stu-id="772c1-106">TEXTWIDTH(** *shapename!TheText* ** ** *[,maximumwidth]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="772c1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="772c1-107">Parameters</span></span>

|<span data-ttu-id="772c1-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="772c1-108">**Name**</span></span>|<span data-ttu-id="772c1-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="772c1-109">**Required/Optional**</span></span>|<span data-ttu-id="772c1-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="772c1-110">**Data Type**</span></span>|<span data-ttu-id="772c1-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="772c1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="772c1-112">_Shapename! TheText_</span><span class="sxs-lookup"><span data-stu-id="772c1-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="772c1-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="772c1-113">Required</span></span>  <br/> |<span data-ttu-id="772c1-114">**String**</span><span class="sxs-lookup"><span data-stu-id="772c1-114">**String**</span></span> <br/> |<span data-ttu-id="772c1-115">Ein Verweis auf die Zelle TheText mit der in der Ziel-Shape.</span><span class="sxs-lookup"><span data-stu-id="772c1-115">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="772c1-116">_Shapename!_</span><span class="sxs-lookup"><span data-stu-id="772c1-116">_shapename!_</span></span> <span data-ttu-id="772c1-117">ist der Name des Shapes, von dem Sie den Text abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="772c1-117">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="772c1-118">_maxBreite_</span><span class="sxs-lookup"><span data-stu-id="772c1-118">_maximumwidth_</span></span> <br/> |<span data-ttu-id="772c1-119">Optional</span><span class="sxs-lookup"><span data-stu-id="772c1-119">Optional</span></span>  <br/> |<span data-ttu-id="772c1-120">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="772c1-120">**Numeric**</span></span> <br/> |<span data-ttu-id="772c1-121">Die maximale Breite eines Textblocks.</span><span class="sxs-lookup"><span data-stu-id="772c1-121">The maximum width of the text block.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="772c1-122">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="772c1-122">Return value</span></span>

<span data-ttu-id="772c1-123">String</span><span class="sxs-lookup"><span data-stu-id="772c1-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="772c1-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="772c1-124">Remarks</span></span>

<span data-ttu-id="772c1-125">Die TEXTWIDTH-Funktion wird meistens verwendet, um die Breite eines Shapes so anzupassen, dass der enthaltene Text vollständig hineinpasst.</span><span class="sxs-lookup"><span data-stu-id="772c1-125">The TEXTWIDTH function is commonly used to adjust the width of a shape to fit the text it contains.</span></span>
  
<span data-ttu-id="772c1-126">Wenn _SheetN!_</span><span class="sxs-lookup"><span data-stu-id="772c1-126">If  _sheetN!_</span></span> <span data-ttu-id="772c1-127">wird Length angegeben, das Standard-Shape ist das aktuelle Shape.</span><span class="sxs-lookup"><span data-stu-id="772c1-127">is omitted, the default shape is the current shape.</span></span> 
  
<span data-ttu-id="772c1-128">Wenn _maxBreite_ angegeben ist, ist das Ergebnis der längsten Textzeile in _maxBreite_hineinpasst.</span><span class="sxs-lookup"><span data-stu-id="772c1-128">If  _maximumwidth_ is specified, the result is the longest line of text that fits within  _maximumwidth_.</span></span> <span data-ttu-id="772c1-129">Wenn _maxBreite_ ausgelassen wird, ist das Ergebnis die gesamte Breite des Texts.</span><span class="sxs-lookup"><span data-stu-id="772c1-129">If  _maximumwidth_ is omitted, the result is the total width of the text.</span></span> 
  
## <a name="example"></a><span data-ttu-id="772c1-130">Beispiel</span><span class="sxs-lookup"><span data-stu-id="772c1-130">Example</span></span>

<span data-ttu-id="772c1-131">(TEXTWIDTH(DerText)</span><span class="sxs-lookup"><span data-stu-id="772c1-131">TEXTWIDTH(TheText)</span></span> 
  
<span data-ttu-id="772c1-132">Gibt die Gesamtlänge des Texts im aktuellen Shape zurück.</span><span class="sxs-lookup"><span data-stu-id="772c1-132">Returns the total length of the text in the current shape.</span></span> 
  

