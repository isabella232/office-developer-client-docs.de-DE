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
description: Ruft den Wert einer Zelle ab und berechnet die Formel nicht neu, wenn der Wert der Zelle ändert.
ms.openlocfilehash: b4c8ea14b7184101a360c9f5ee4af03fd178aa6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797095"
---
# <a name="getval-function"></a><span data-ttu-id="9f974-103">GETVAL Function</span><span class="sxs-lookup"><span data-stu-id="9f974-103">GETVAL Function</span></span>

<span data-ttu-id="9f974-104">Ruft den Wert einer Zelle ab und berechnet die Formel nicht neu, wenn der Wert der Zelle ändert.</span><span class="sxs-lookup"><span data-stu-id="9f974-104">Gets the value of a cell and doesn't recalculate the formula when the cell's value changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="9f974-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f974-105">Syntax</span></span>

<span data-ttu-id="9f974-106">GETVAL (** *Abrufen Cellname* **)</span><span class="sxs-lookup"><span data-stu-id="9f974-106">GETVAL(** *cellname* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9f974-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f974-107">Parameters</span></span>

|<span data-ttu-id="9f974-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="9f974-108">**Name**</span></span>|<span data-ttu-id="9f974-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="9f974-109">**Required/Optional**</span></span>|<span data-ttu-id="9f974-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9f974-110">**Data Type**</span></span>|<span data-ttu-id="9f974-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9f974-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9f974-112">_abrufen cellName_</span><span class="sxs-lookup"><span data-stu-id="9f974-112">_cellname_</span></span> <br/> |<span data-ttu-id="9f974-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9f974-113">Required</span></span>  <br/> |<span data-ttu-id="9f974-114">**String**</span><span class="sxs-lookup"><span data-stu-id="9f974-114">**String**</span></span> <br/> |<span data-ttu-id="9f974-115">Der Name der Zelle, deren Wert abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9f974-115">The name of the cell to get the value of.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="9f974-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9f974-116">Example</span></span>

<span data-ttu-id="9f974-117">GETVAL(PinX) + GETVAL(PinY) + Width</span><span class="sxs-lookup"><span data-stu-id="9f974-117">GETVAL(PinX) + GETVAL(PinY) + Width</span></span> 
  
<span data-ttu-id="9f974-118">Gibt den summierten Wert der Zellen PinX, PinY und Width zurück.</span><span class="sxs-lookup"><span data-stu-id="9f974-118">Returns the sum of the value of the PinX, PinY, and Width cells.</span></span> 
  

