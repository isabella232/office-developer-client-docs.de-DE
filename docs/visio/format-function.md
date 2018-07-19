---
title: FORMAT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251424
localization_priority: Normal
ms.assetid: 52f5ef4d-07c6-ab36-bf74-b30b50eea221
description: Gibt das Ergebnis von Expression als Zeichenfolge entsprechend der Formatierungsangabe formatiert.
ms.openlocfilehash: dcb898b3cb21d8cc5ebee7e56540d9e2eefcffdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797067"
---
# <a name="format-function"></a><span data-ttu-id="e98b6-103">FORMAT Function</span><span class="sxs-lookup"><span data-stu-id="e98b6-103">FORMAT Function</span></span>

<span data-ttu-id="e98b6-104">Gibt das Ergebnis von _Expression_ als eine _Formatierungsangabe_Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="e98b6-104">Returns the result of  _expression_ as a string formatted according to  _formatpicture_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e98b6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e98b6-105">Syntax</span></span>

<span data-ttu-id="e98b6-106">FORMAT (** *Ausdruck* **, "** *Formatierungsangabe* **")</span><span class="sxs-lookup"><span data-stu-id="e98b6-106">FORMAT(** *expression* **," ** *formatpicture* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e98b6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e98b6-107">Parameters</span></span>

|<span data-ttu-id="e98b6-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e98b6-108">**Name**</span></span>|<span data-ttu-id="e98b6-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="e98b6-109">**Required/Optional**</span></span>|<span data-ttu-id="e98b6-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="e98b6-110">**Data Type**</span></span>|<span data-ttu-id="e98b6-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e98b6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e98b6-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="e98b6-112">_expression_</span></span> <br/> |<span data-ttu-id="e98b6-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e98b6-113">Required</span></span>  <br/> |<span data-ttu-id="e98b6-114">**String**</span><span class="sxs-lookup"><span data-stu-id="e98b6-114">**String**</span></span> <br/> |<span data-ttu-id="e98b6-115">Eine Kombination aus Konstanten, Operatoren, Funktionen und Bezügen auf ShapeSheet-Zellen, die einen Wert ergeben.</span><span class="sxs-lookup"><span data-stu-id="e98b6-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
| <span data-ttu-id="e98b6-116">_die Funktion_</span><span class="sxs-lookup"><span data-stu-id="e98b6-116">_formatpicture_</span></span> <br/> |<span data-ttu-id="e98b6-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e98b6-117">Required</span></span>  <br/> |<span data-ttu-id="e98b6-118">**String**</span><span class="sxs-lookup"><span data-stu-id="e98b6-118">**String**</span></span> <br/> |<span data-ttu-id="e98b6-119">Die Formatierungsangabe zum Formatieren der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e98b6-119">The format picture used to fomat the string.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e98b6-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e98b6-120">Return value</span></span>

<span data-ttu-id="e98b6-121">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e98b6-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e98b6-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e98b6-122">Remarks</span></span>

<span data-ttu-id="e98b6-123">Der Typ des Ausdrucks und der in der Formatierungsangabe angegebene Typ bestimmen das Verhalten der zurückgegebenen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e98b6-123">The type of the expression and the type specified in the format picture govern the behavior of the returned string.</span></span> <span data-ttu-id="e98b6-124">Die _Formatierungsangabe_ muss für den Typ des Ausdrucks sein.</span><span class="sxs-lookup"><span data-stu-id="e98b6-124">The  _formatpicture_ must be appropriate for the type of expression.</span></span> <span data-ttu-id="e98b6-125">Weitere Informationen zu Formatierungsangaben angeben finden Sie unter [Informationen zu Formatierungsangaben](about-format-pictures.md).</span><span class="sxs-lookup"><span data-stu-id="e98b6-125">For more information about specifying format pictures, see [About format pictures](about-format-pictures.md).</span></span>
  
<span data-ttu-id="e98b6-126">Gibt einen Fehler zurück, wenn das Ergebnis von _Expression_ und der erwartete Typ in _Formatpicture_ unterschiedlich sind oder wenn _Formatpicture_Syntaxfehler vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="e98b6-126">Returns an error if the result of  _expression_ and the type expected in  _formatpicture_ are of a different kind or if there are syntax errors in  _formatpicture_.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="e98b6-127">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e98b6-127">Example 1</span></span>

<span data-ttu-id="e98b6-128">FORMAT(1cm/4, "0,000 u")</span><span class="sxs-lookup"><span data-stu-id="e98b6-128">FORMAT(1cm/4, "0.000 u")</span></span>
  
<span data-ttu-id="e98b6-129">Gibt 0,250 cm zurück.</span><span class="sxs-lookup"><span data-stu-id="e98b6-129">Returns "0.250 cm."</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e98b6-130">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e98b6-130">Example 2</span></span>

<span data-ttu-id="e98b6-131">FORMAT(1cm/4, "0,00 U")</span><span class="sxs-lookup"><span data-stu-id="e98b6-131">FORMAT(1cm/4, "0.00 U")</span></span>
  
<span data-ttu-id="e98b6-132">Gibt 0,25 cm zurück.</span><span class="sxs-lookup"><span data-stu-id="e98b6-132">Returns "0.25 CM."</span></span>
  
## <a name="example-3"></a><span data-ttu-id="e98b6-133">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e98b6-133">Example 3</span></span>

<span data-ttu-id="e98b6-134">FORMAT(1cm/4, "0,0 u")</span><span class="sxs-lookup"><span data-stu-id="e98b6-134">FORMAT(1cm/4, "0.0 u")</span></span>
  
<span data-ttu-id="e98b6-135">Gibt 0.3 cm zurück.</span><span class="sxs-lookup"><span data-stu-id="e98b6-135">Returns "0.3 cm."</span></span>
  

