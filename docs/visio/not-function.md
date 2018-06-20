---
title: NOT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251469
localization_priority: Normal
ms.assetid: 65873b32-2406-7c33-8e68-802461f467b2
description: Gibt TRUE (1) zurück, wenn Logicalexpression auf false festgelegt ist. Andernfalls wird FALSE (0) zurückgegeben.
ms.openlocfilehash: e2359aaab18469cd4f272f71aca8d899a12b2120
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797550"
---
# <a name="not-function"></a><span data-ttu-id="a9711-104">NOT Function</span><span class="sxs-lookup"><span data-stu-id="a9711-104">NOT Function</span></span>

<span data-ttu-id="a9711-105">Gibt TRUE (1) zurück, wenn _Logicalexpression_ auf false festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a9711-105">Returns TRUE (1) if  _logicalexpression_ is FALSE.</span></span> <span data-ttu-id="a9711-106">Andernfalls wird FALSE (0) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a9711-106">Otherwise, it returns FALSE (0).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a9711-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9711-107">Syntax</span></span>

<span data-ttu-id="a9711-108">KEINE (** *Logicalexpression* **)</span><span class="sxs-lookup"><span data-stu-id="a9711-108">NOT(** *logicalexpression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a9711-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9711-109">Parameters</span></span>

|<span data-ttu-id="a9711-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="a9711-110">**Name**</span></span>|<span data-ttu-id="a9711-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="a9711-111">**Required/Optional**</span></span>|<span data-ttu-id="a9711-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a9711-112">**Data Type**</span></span>|<span data-ttu-id="a9711-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a9711-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a9711-114">_logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="a9711-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="a9711-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a9711-115">Required</span></span>  <br/> |<span data-ttu-id="a9711-116">**String**</span><span class="sxs-lookup"><span data-stu-id="a9711-116">**String**</span></span> <br/> |<span data-ttu-id="a9711-117">Der logische Ausdruck, der ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9711-117">The logical expression to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a9711-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="a9711-118">Return value</span></span>

<span data-ttu-id="a9711-119">Boolean</span><span class="sxs-lookup"><span data-stu-id="a9711-119">Boolean</span></span>
  
## <a name="example"></a><span data-ttu-id="a9711-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a9711-120">Example</span></span>

<span data-ttu-id="a9711-121">KEINE (Höhe \> 0,75 Zoll)</span><span class="sxs-lookup"><span data-stu-id="a9711-121">NOT(Height \> 0.75 in)</span></span> 
  
<span data-ttu-id="a9711-p103">Gibt 1 zurück, wenn Höhe kleiner als oder gleich 2 cm ist. Gibt 0 zurück, wenn Höhe größer als 2 cm ist.</span><span class="sxs-lookup"><span data-stu-id="a9711-p103">Returns 1 if Height is less than or equal to 0.75 inches. Returns 0 if Height is greater than 0.75 inches.</span></span> 
  

