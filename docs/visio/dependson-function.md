---
title: DEPENDSON-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251420
localization_priority: Normal
ms.assetid: 8fcfcfdd-69e2-b061-fdb6-d29389d14403
description: Erstellt eine Zelle Verweis Abhängigkeit.
ms.openlocfilehash: 07c0d79668230cbf2b1e8d51b50e67835c87e2f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796835"
---
# <a name="dependson-function"></a><span data-ttu-id="5198b-103">DEPENDSON Function</span><span class="sxs-lookup"><span data-stu-id="5198b-103">DEPENDSON Function</span></span>

<span data-ttu-id="5198b-104">Erstellt eine Zelle Verweis Abhängigkeit.</span><span class="sxs-lookup"><span data-stu-id="5198b-104">Creates a cell reference dependency.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5198b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5198b-105">Syntax</span></span>

<span data-ttu-id="5198b-106">DEPENDSON (** *Cellref* ** [, ** *cellref2* **,...])</span><span class="sxs-lookup"><span data-stu-id="5198b-106">DEPENDSON(** *cellref* ** [, ** *cellref2* **,...])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5198b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5198b-107">Parameters</span></span>

|<span data-ttu-id="5198b-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="5198b-108">**Name**</span></span>|<span data-ttu-id="5198b-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="5198b-109">**Required/Optional**</span></span>|<span data-ttu-id="5198b-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="5198b-110">**Data Type**</span></span>|<span data-ttu-id="5198b-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5198b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5198b-112">_CellRef_</span><span class="sxs-lookup"><span data-stu-id="5198b-112">_cellref_</span></span> <br/> |<span data-ttu-id="5198b-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="5198b-113">Required</span></span>  <br/> |<span data-ttu-id="5198b-114">**String**</span><span class="sxs-lookup"><span data-stu-id="5198b-114">**String**</span></span> <br/> |<span data-ttu-id="5198b-115">Der erste Zellbezug.</span><span class="sxs-lookup"><span data-stu-id="5198b-115">The first cell reference.</span></span>  <br/> |
| <span data-ttu-id="5198b-116">_cellref2_</span><span class="sxs-lookup"><span data-stu-id="5198b-116">_cellref2_</span></span> <br/> |<span data-ttu-id="5198b-117">Optional</span><span class="sxs-lookup"><span data-stu-id="5198b-117">Optional</span></span>  <br/> |<span data-ttu-id="5198b-118">**String**</span><span class="sxs-lookup"><span data-stu-id="5198b-118">**String**</span></span> <br/> |<span data-ttu-id="5198b-119">Der zweite Zellbezug.</span><span class="sxs-lookup"><span data-stu-id="5198b-119">The second cell reference.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5198b-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5198b-120">Remarks</span></span>

<span data-ttu-id="5198b-p101">Diese Funktion gibt immer FALSE zurück. Sie hat keine Auswirkung, wenn Sie in einer Ereigniszeile oder in einer Aktionszelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5198b-p101">This function always returns FALSE. It has no effect when used in an Event row or an Action cell.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5198b-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5198b-123">Example</span></span>

<span data-ttu-id="5198b-124">OPENTEXTWIN() + DEPENDSON(PinX,PinY)</span><span class="sxs-lookup"><span data-stu-id="5198b-124">OPENTEXTWIN() + DEPENDSON(PinX,PinY)</span></span> 
  
<span data-ttu-id="5198b-125">Öffnet den Textblock eines Shapes, sobald sich die Zellen PinX oder PinY des Shapes ändern.</span><span class="sxs-lookup"><span data-stu-id="5198b-125">Opens the text block for a shape whenever the shape's PinX or PinY cells change.</span></span> 
  

