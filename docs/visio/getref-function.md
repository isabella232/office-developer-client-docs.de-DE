---
title: GETREF-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251884
localization_priority: Normal
ms.assetid: 25c9f817-d22b-28c9-1339-dc9f27d0dd41
description: Verweist auf eine Zelle und berechnet die Formel nicht neu, wenn die referenzierte Zelle ändert.
ms.openlocfilehash: 454314b1f156f560c237f22a45492978ca3c31ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797093"
---
# <a name="getref-function"></a><span data-ttu-id="578a1-103">GETREF Function</span><span class="sxs-lookup"><span data-stu-id="578a1-103">GETREF Function</span></span>

<span data-ttu-id="578a1-104">Verweist auf eine Zelle und berechnet die Formel nicht neu, wenn die referenzierte Zelle ändert.</span><span class="sxs-lookup"><span data-stu-id="578a1-104">References a cell and doesn't recalculate the formula when the referenced cell changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="578a1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="578a1-105">Syntax</span></span>

<span data-ttu-id="578a1-106">GETREF (** *Abrufen Cellname* **)</span><span class="sxs-lookup"><span data-stu-id="578a1-106">GETREF(** *cellname* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="578a1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="578a1-107">Parameters</span></span>

|<span data-ttu-id="578a1-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="578a1-108">**Name**</span></span>|<span data-ttu-id="578a1-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="578a1-109">**Required/Optional**</span></span>|<span data-ttu-id="578a1-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="578a1-110">**Data Type**</span></span>|<span data-ttu-id="578a1-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="578a1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="578a1-112">_abrufen cellName_</span><span class="sxs-lookup"><span data-stu-id="578a1-112">_cellname_</span></span> <br/> |<span data-ttu-id="578a1-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="578a1-113">Required</span></span>  <br/> |<span data-ttu-id="578a1-114">**String**</span><span class="sxs-lookup"><span data-stu-id="578a1-114">**String**</span></span> <br/> |<span data-ttu-id="578a1-115">Der Name der abzurufenden einen Verweis auf die Zelle.</span><span class="sxs-lookup"><span data-stu-id="578a1-115">The name of the cell to get a reference to.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="578a1-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="578a1-116">Example</span></span>

<span data-ttu-id="578a1-117">SETF(GETREF(PinX),5.1)</span><span class="sxs-lookup"><span data-stu-id="578a1-117">SETF(GETREF(PinX),5.1)</span></span> 
  
<span data-ttu-id="578a1-118">Legt die Formel der Zelle DrehbezX auf 5,1 fest.</span><span class="sxs-lookup"><span data-stu-id="578a1-118">Sets the formula of the PinX cell to 5.1.</span></span> 
  

