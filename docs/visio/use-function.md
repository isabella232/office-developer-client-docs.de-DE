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
description: Wendet das Linienmuster, Füllmuster oder Linienende namens Name mit dem Shape in die Zelle LinePattern, FillPattern, BeginArrow oder EndArrow platziert.
ms.openlocfilehash: 0b6668e57a8f997a69fece51cbc5bd1b1574a576
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798355"
---
# <a name="use-function"></a><span data-ttu-id="c0081-103">USE Function</span><span class="sxs-lookup"><span data-stu-id="c0081-103">USE Function</span></span>

<span data-ttu-id="c0081-104">Wendet das Linienmuster, Füllmuster oder Linienende namens _Name_ mit dem Shape in die Zelle LinePattern, FillPattern, BeginArrow oder EndArrow platziert.</span><span class="sxs-lookup"><span data-stu-id="c0081-104">Applies the line pattern, fill pattern, or line end called  _name_ to the shape when placed in the LinePattern, FillPattern, BeginArrow, or EndArrow cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c0081-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0081-105">Syntax</span></span>

<span data-ttu-id="c0081-106">VERWENDEN ("** *Namen* **")</span><span class="sxs-lookup"><span data-stu-id="c0081-106">USE(" ** *name* ** ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c0081-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0081-107">Parameters</span></span>

|<span data-ttu-id="c0081-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c0081-108">**Name**</span></span>|<span data-ttu-id="c0081-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="c0081-109">**Required/Optional**</span></span>|<span data-ttu-id="c0081-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="c0081-110">**Data Type**</span></span>|<span data-ttu-id="c0081-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c0081-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c0081-112">_Name_</span><span class="sxs-lookup"><span data-stu-id="c0081-112">_name_</span></span> <br/> |<span data-ttu-id="c0081-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c0081-113">Required</span></span>  <br/> |<span data-ttu-id="c0081-114">**String**</span><span class="sxs-lookup"><span data-stu-id="c0081-114">**String**</span></span> <br/> |<span data-ttu-id="c0081-115">Beliebige Zeichenfolge, die für einen gültigen Master-Shape-Namen steht.</span><span class="sxs-lookup"><span data-stu-id="c0081-115">Any string that is a valid master name.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c0081-116">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="c0081-116">Return value</span></span>

<span data-ttu-id="c0081-117">Zahl</span><span class="sxs-lookup"><span data-stu-id="c0081-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c0081-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0081-118">Remarks</span></span>

<span data-ttu-id="c0081-119">Wenn ein Master-Shape mit dem Namen _Name_ in der Dokumentschablone des Dokuments vorhanden ist, wird das Muster als Linienmuster, Füllmuster, PfeilAnfang oder Pfeilende beginnen angewendet.</span><span class="sxs-lookup"><span data-stu-id="c0081-119">If a master named  _name_ is present on the document stencil of the document, the pattern is applied as a line pattern, fill pattern, begin arrow, or end arrow.</span></span> 
  
<span data-ttu-id="c0081-120">Diese Funktion gibt immer 254 zurück.</span><span class="sxs-lookup"><span data-stu-id="c0081-120">This function always returns 254.</span></span>
  
## <a name="example"></a><span data-ttu-id="c0081-121">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c0081-121">Example</span></span>

<span data-ttu-id="c0081-122">USE("Railroad Tracks")</span><span class="sxs-lookup"><span data-stu-id="c0081-122">USE("Railroad Tracks")</span></span> 
  
<span data-ttu-id="c0081-123">Formatiert das Shape, indem das Mastermuster namens Railroad Tracks auf das Shape, das die Formel enthält, angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c0081-123">Formats the shape by applying the master pattern named Railroad Tracks to the shape containing the formula.</span></span> 
  

