---
title: LEFT-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1021757
localization_priority: Normal
ms.assetid: 0c2f6e06-b772-2006-ec7b-8695d097f146
description: Gibt die am weitesten links liegenden Zeichen oder Zeichen in einer Textzeichenfolge basierend auf der Anzahl der Zeichen zurück, die Sie angeben.
ms.openlocfilehash: aa4141cfc53bd41a6d58e8bc666b18a06fc80245
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309464"
---
# <a name="left-function-visioshapesheet"></a><span data-ttu-id="55697-103">LEFT-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="55697-103">LEFT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="55697-104">Gibt die am weitesten links liegenden Zeichen oder Zeichen in einer Textzeichenfolge basierend auf der Anzahl der Zeichen zurück, die Sie angeben.</span><span class="sxs-lookup"><span data-stu-id="55697-104">Returns the left-most character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="55697-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="55697-105">Syntax</span></span>

<span data-ttu-id="55697-106">Left (\* \* *Text* \* \*, [, \* \* *num_chars_opt* \* \*])</span><span class="sxs-lookup"><span data-stu-id="55697-106">LEFT(\*\* *text* \*\*, [, \*\* *num_chars_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="55697-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="55697-107">Parameters</span></span>

|<span data-ttu-id="55697-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="55697-108">**Name**</span></span>|<span data-ttu-id="55697-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="55697-109">**Required/Optional**</span></span>|<span data-ttu-id="55697-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="55697-110">**Data Type**</span></span>|<span data-ttu-id="55697-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="55697-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="55697-112">_text_</span><span class="sxs-lookup"><span data-stu-id="55697-112">_text_</span></span> <br/> |<span data-ttu-id="55697-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="55697-113">Required</span></span>  <br/> |<span data-ttu-id="55697-114">**String**</span><span class="sxs-lookup"><span data-stu-id="55697-114">**String**</span></span> <br/> |<span data-ttu-id="55697-115">Die Zeichenfolge mit den zu extrahierenden Zeichen.</span><span class="sxs-lookup"><span data-stu-id="55697-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="55697-116">_num_chars_opt_</span><span class="sxs-lookup"><span data-stu-id="55697-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="55697-117">Optional</span><span class="sxs-lookup"><span data-stu-id="55697-117">Optional</span></span>  <br/> |<span data-ttu-id="55697-118">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="55697-118">**Numeric**</span></span> <br/> |<span data-ttu-id="55697-119">Die Anzahl der Zeichen, die extrahiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="55697-119">The number of characters you want to extract.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="55697-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55697-120">Return value</span></span>

<span data-ttu-id="55697-121">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="55697-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="55697-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55697-122">Remarks</span></span>

<span data-ttu-id="55697-123">Der Wert von _num_chars_opt_ muss größer oder gleich NULL (0) sein.</span><span class="sxs-lookup"><span data-stu-id="55697-123">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="55697-124">Wenn _num_chars_opt_ größer als die Länge des Texts ist, gibt Left den gesamten Text zurück.</span><span class="sxs-lookup"><span data-stu-id="55697-124">If  _num_chars_opt_ is greater than the length of the text, LEFT returns all of the text.</span></span> <span data-ttu-id="55697-125">Wenn _num_chars_opt_ ausgelassen wird, wird davon ausgegangen, dass es 1 ist.</span><span class="sxs-lookup"><span data-stu-id="55697-125">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="55697-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="55697-126">Example</span></span>

<span data-ttu-id="55697-127">LEFT ("Januar 1, 2004", 3)</span><span class="sxs-lookup"><span data-stu-id="55697-127">LEFT ("January 1, 2004", 3)</span></span> 
  
<span data-ttu-id="55697-128">Ergibt den Wert Jan.</span><span class="sxs-lookup"><span data-stu-id="55697-128">Returns the value "Jan".</span></span> 
  

