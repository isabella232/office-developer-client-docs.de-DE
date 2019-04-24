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
description: Gibt TRUE (1) zurück, wenn logicive auf FALSE festgelegt ist. Andernfalls wird FALSE (0) zurückgegeben.
ms.openlocfilehash: 3359e21654bcc318caf31405093f851eca064119
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341139"
---
# <a name="not-function"></a><span data-ttu-id="62aff-104">NOT Function</span><span class="sxs-lookup"><span data-stu-id="62aff-104">NOT Function</span></span>

<span data-ttu-id="62aff-105">Gibt TRUE (1) zurück __ , wenn logicIVE auf FALSE festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="62aff-105">Returns TRUE (1) if  _logicalexpression_ is FALSE.</span></span> <span data-ttu-id="62aff-106">Andernfalls wird FALSE (0) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="62aff-106">Otherwise, it returns FALSE (0).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="62aff-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="62aff-107">Syntax</span></span>

<span data-ttu-id="62aff-108">NOT (\* \* *logischer* \* \*)</span><span class="sxs-lookup"><span data-stu-id="62aff-108">NOT(\*\* *logicalexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="62aff-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="62aff-109">Parameters</span></span>

|<span data-ttu-id="62aff-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="62aff-110">**Name**</span></span>|<span data-ttu-id="62aff-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="62aff-111">**Required/Optional**</span></span>|<span data-ttu-id="62aff-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="62aff-112">**Data Type**</span></span>|<span data-ttu-id="62aff-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="62aff-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="62aff-114">_Logik_</span><span class="sxs-lookup"><span data-stu-id="62aff-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="62aff-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="62aff-115">Required</span></span>  <br/> |<span data-ttu-id="62aff-116">**String**</span><span class="sxs-lookup"><span data-stu-id="62aff-116">**String**</span></span> <br/> |<span data-ttu-id="62aff-117">Der logische Ausdruck, der ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="62aff-117">The logical expression to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="62aff-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62aff-118">Return value</span></span>

<span data-ttu-id="62aff-119">Boolesch</span><span class="sxs-lookup"><span data-stu-id="62aff-119">Boolean</span></span>
  
## <a name="example"></a><span data-ttu-id="62aff-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="62aff-120">Example</span></span>

<span data-ttu-id="62aff-121">NICHT (Höhe \> 0,75 in)</span><span class="sxs-lookup"><span data-stu-id="62aff-121">NOT(Height \> 0.75 in)</span></span> 
  
<span data-ttu-id="62aff-122">Gibt 1 zurück, wenn Höhe kleiner als oder gleich 2 cm ist.</span><span class="sxs-lookup"><span data-stu-id="62aff-122">Returns 1 if Height is less than or equal to 0.75 inches.</span></span> <span data-ttu-id="62aff-123">Gibt 0 zurück, wenn Höhe größer als 2 cm ist.</span><span class="sxs-lookup"><span data-stu-id="62aff-123">Returns 0 if Height is greater than 0.75 inches.</span></span> 
  

