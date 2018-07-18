---
title: MAGNITUDE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251461
localization_priority: Normal
ms.assetid: 9f443687-9861-5f51-94c4-f056805f736b
description: Gibt das Ausmaß der Vektor, dessen Steigung, deren Ausführung B, multipliziert mit den jeweiligen ist KonstanteA und KonstanteB.
ms.openlocfilehash: f4c428b8b381af58958dab66a71ddd0bcaf715c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797435"
---
# <a name="magnitude-function"></a><span data-ttu-id="4cb2c-103">MAGNITUDE Function</span><span class="sxs-lookup"><span data-stu-id="4cb2c-103">MAGNITUDE Function</span></span>

<span data-ttu-id="4cb2c-104">_Gibt dem Ausmaß der Vektor, dessen Steigung, deren Ausführung _B_, multipliziert mit der entsprechenden Konstanten ist_ _KonstanteA_ und _KonstanteB_.</span><span class="sxs-lookup"><span data-stu-id="4cb2c-104">Returns the magnitude of the vector whose rise is  _A_ and whose run is  _B_, multiplied by the respective constants  _constantA_ and  _constantB_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4cb2c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cb2c-105">Syntax</span></span>

<span data-ttu-id="4cb2c-106">MAGNITUDE (** *KonstanteA* **, ** *A* **, ** *KonstanteB* **, ** *B* **)</span><span class="sxs-lookup"><span data-stu-id="4cb2c-106">MAGNITUDE(** *constantA* **, ** *A* **, ** *constantB* **, ** *B* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4cb2c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cb2c-107">Parameters</span></span>

|<span data-ttu-id="4cb2c-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="4cb2c-108">**Name**</span></span>|<span data-ttu-id="4cb2c-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="4cb2c-109">**Required/Optional**</span></span>|<span data-ttu-id="4cb2c-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="4cb2c-110">**Data Type**</span></span>|<span data-ttu-id="4cb2c-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4cb2c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4cb2c-112">_KonstanteA_</span><span class="sxs-lookup"><span data-stu-id="4cb2c-112">_constantA_</span></span> <br/> |<span data-ttu-id="4cb2c-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4cb2c-113">Required</span></span>  <br/> |<span data-ttu-id="4cb2c-114">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="4cb2c-114">**Number**</span></span> <br/> |<span data-ttu-id="4cb2c-115">Die Konstante, mit der die Steigung multipliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4cb2c-115">The constant by which to multiply the rise.</span></span>  <br/> |
| <span data-ttu-id="4cb2c-116">_A_</span><span class="sxs-lookup"><span data-stu-id="4cb2c-116">_A_</span></span> <br/> |<span data-ttu-id="4cb2c-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4cb2c-117">Required</span></span>  <br/> |<span data-ttu-id="4cb2c-118">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="4cb2c-118">**Number**</span></span> <br/> |<span data-ttu-id="4cb2c-119">Die Steigung.</span><span class="sxs-lookup"><span data-stu-id="4cb2c-119">The rise.</span></span>  <br/> |
| <span data-ttu-id="4cb2c-120">_KonstanteB_</span><span class="sxs-lookup"><span data-stu-id="4cb2c-120">_constantB_</span></span> <br/> |<span data-ttu-id="4cb2c-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4cb2c-121">Required</span></span>  <br/> |<span data-ttu-id="4cb2c-122">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="4cb2c-122">**Number**</span></span> <br/> |<span data-ttu-id="4cb2c-123">Die Konstante, mit der die Länge multipliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4cb2c-123">The constant by which to multiply the run.</span></span>  <br/> |
| <span data-ttu-id="4cb2c-124">_B_</span><span class="sxs-lookup"><span data-stu-id="4cb2c-124">_B_</span></span> <br/> |<span data-ttu-id="4cb2c-125">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4cb2c-125">Required</span></span>  <br/> |<span data-ttu-id="4cb2c-126">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="4cb2c-126">**Number**</span></span> <br/> |<span data-ttu-id="4cb2c-127">Die Länge.</span><span class="sxs-lookup"><span data-stu-id="4cb2c-127">The run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4cb2c-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4cb2c-128">Remarks</span></span>

<span data-ttu-id="4cb2c-129">MAGNITUDE wird nach folgender Formel berechnet:</span><span class="sxs-lookup"><span data-stu-id="4cb2c-129">MAGNITUDE is calculated according to the following formula:</span></span>
  
<span data-ttu-id="4cb2c-130">Wurzel ((KonstanteA \* A) ^ 2 + (KonstanteB \* B) ^ 2)</span><span class="sxs-lookup"><span data-stu-id="4cb2c-130">SQRT((constantA \* A)^2 + (constantB \* B)^2)</span></span>
  
## <a name="example"></a><span data-ttu-id="4cb2c-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4cb2c-131">Example</span></span>

<span data-ttu-id="4cb2c-132">MAGNITUDE(1, 3, 1, 4)</span><span class="sxs-lookup"><span data-stu-id="4cb2c-132">MAGNITUDE(1, 3, 1, 4)</span></span> 
  
<span data-ttu-id="4cb2c-133">Gibt 5 zurück.</span><span class="sxs-lookup"><span data-stu-id="4cb2c-133">Returns 5.</span></span> 
  

