---
title: GETVAL-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251885
localization_priority: Normal
ms.assetid: 1da42991-5791-ebab-84cc-286cfe984a61
description: Ruft den Wert einer Zelle ab und berechnet die Formel nicht neu, wenn sich der Wert der Zelle ändert.
ms.openlocfilehash: 9449ccd8f849b23faf08ee25826301a1b6efe6d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416888"
---
# <a name="getval-function"></a><span data-ttu-id="ba035-103">GETVAL Function</span><span class="sxs-lookup"><span data-stu-id="ba035-103">GETVAL Function</span></span>

<span data-ttu-id="ba035-104">Ruft den Wert einer Zelle ab und berechnet die Formel nicht neu, wenn sich der Wert der Zelle ändert.</span><span class="sxs-lookup"><span data-stu-id="ba035-104">Gets the value of a cell and doesn't recalculate the formula when the cell's value changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ba035-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba035-105">Syntax</span></span>

<span data-ttu-id="ba035-106">GETVAL (\* \* *cellName* \* \*)</span><span class="sxs-lookup"><span data-stu-id="ba035-106">GETVAL(\*\* *cellname* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ba035-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba035-107">Parameters</span></span>

|<span data-ttu-id="ba035-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="ba035-108">**Name**</span></span>|<span data-ttu-id="ba035-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="ba035-109">**Required/Optional**</span></span>|<span data-ttu-id="ba035-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="ba035-110">**Data Type**</span></span>|<span data-ttu-id="ba035-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ba035-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ba035-112">_cellName_</span><span class="sxs-lookup"><span data-stu-id="ba035-112">_cellname_</span></span> <br/> |<span data-ttu-id="ba035-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ba035-113">Required</span></span>  <br/> |<span data-ttu-id="ba035-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ba035-114">**String**</span></span> <br/> |<span data-ttu-id="ba035-115">Der Name der Zelle, deren Wert abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba035-115">The name of the cell to get the value of.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="ba035-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ba035-116">Example</span></span>

<span data-ttu-id="ba035-117">GETVAL(PinX) + GETVAL(PinY) + Width</span><span class="sxs-lookup"><span data-stu-id="ba035-117">GETVAL(PinX) + GETVAL(PinY) + Width</span></span> 
  
<span data-ttu-id="ba035-118">Gibt den summierten Wert der Zellen PinX, PinY und Width zurück.</span><span class="sxs-lookup"><span data-stu-id="ba035-118">Returns the sum of the value of the PinX, PinY, and Width cells.</span></span> 
  

