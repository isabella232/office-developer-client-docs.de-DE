---
title: USE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251510
localization_priority: Normal
ms.assetid: 410c4187-21f3-d959-750e-9dc6095fba9a
description: Wendet das Linienmuster, das Füllmuster oder das Zeilenende namens name auf die Form an, wenn sie in der Zelle LinePattern, FillPattern, BeginArrow oder EndArrow platziert wird.
ms.openlocfilehash: ddd15c1c127fafa1a230545d544c74956f5c0262
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422824"
---
# <a name="use-function"></a><span data-ttu-id="52fc6-103">USE Function</span><span class="sxs-lookup"><span data-stu-id="52fc6-103">USE Function</span></span>

<span data-ttu-id="52fc6-104">Wendet das Linienmuster, das Füllmuster  oder das Zeilenende namens name auf die Form an, wenn sie in der Zelle LinePattern, FillPattern, BeginArrow oder EndArrow platziert wird.</span><span class="sxs-lookup"><span data-stu-id="52fc6-104">Applies the line pattern, fill pattern, or line end called  _name_ to the shape when placed in the LinePattern, FillPattern, BeginArrow, or EndArrow cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="52fc6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="52fc6-105">Syntax</span></span>

<span data-ttu-id="52fc6-106">USE(" \*\* *Name* \*\* ")</span><span class="sxs-lookup"><span data-stu-id="52fc6-106">USE(" \*\* *name* \*\* ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="52fc6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="52fc6-107">Parameters</span></span>

|<span data-ttu-id="52fc6-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="52fc6-108">**Name**</span></span>|<span data-ttu-id="52fc6-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="52fc6-109">**Required/Optional**</span></span>|<span data-ttu-id="52fc6-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="52fc6-110">**Data Type**</span></span>|<span data-ttu-id="52fc6-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="52fc6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="52fc6-112">_Name_</span><span class="sxs-lookup"><span data-stu-id="52fc6-112">_name_</span></span> <br/> |<span data-ttu-id="52fc6-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="52fc6-113">Required</span></span>  <br/> |<span data-ttu-id="52fc6-114">**String**</span><span class="sxs-lookup"><span data-stu-id="52fc6-114">**String**</span></span> <br/> |<span data-ttu-id="52fc6-115">Beliebige Zeichenfolge, die für einen gültigen Master-Shape-Namen steht.</span><span class="sxs-lookup"><span data-stu-id="52fc6-115">Any string that is a valid master name.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="52fc6-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52fc6-116">Return value</span></span>

<span data-ttu-id="52fc6-117">Nummer</span><span class="sxs-lookup"><span data-stu-id="52fc6-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="52fc6-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="52fc6-118">Remarks</span></span>

<span data-ttu-id="52fc6-119">Wenn in  der Dokumentschablone des Dokuments ein Mastername vorhanden ist, wird das Muster als Linienmuster, Füllmuster, Startpfeil oder Endpfeil angewendet.</span><span class="sxs-lookup"><span data-stu-id="52fc6-119">If a master named  _name_ is present on the document stencil of the document, the pattern is applied as a line pattern, fill pattern, begin arrow, or end arrow.</span></span> 
  
<span data-ttu-id="52fc6-120">Diese Funktion gibt immer 254 zurück.</span><span class="sxs-lookup"><span data-stu-id="52fc6-120">This function always returns 254.</span></span>
  
## <a name="example"></a><span data-ttu-id="52fc6-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="52fc6-121">Example</span></span>

<span data-ttu-id="52fc6-122">USE("Railroad Tracks")</span><span class="sxs-lookup"><span data-stu-id="52fc6-122">USE("Railroad Tracks")</span></span> 
  
<span data-ttu-id="52fc6-123">Formatiert das Shape, indem das Mastermuster namens Railroad Tracks auf das Shape, das die Formel enthält, angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="52fc6-123">Formats the shape by applying the master pattern named Railroad Tracks to the shape containing the formula.</span></span> 
  

