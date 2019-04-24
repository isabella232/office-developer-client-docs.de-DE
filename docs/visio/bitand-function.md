---
title: BITAND-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251398
localization_priority: Normal
ms.assetid: c437de23-d2e0-469d-62e6-8eb8b8cfea5c
description: Gibt eine 16-Bit-Binärzahl zurück, in der jedes Bit nur dann auf 1 festgelegt ist, wenn das entsprechende Bit in binarynumber1 und binarynumber2 1 ist. Andernfalls ist das Bit auf 0 festgelegt.
ms.openlocfilehash: 495ad645a422c0333d02a22c3c600dd1e0d567bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284469"
---
# <a name="bitand-function"></a><span data-ttu-id="ba31b-104">BITAND Function</span><span class="sxs-lookup"><span data-stu-id="ba31b-104">BITAND Function</span></span>

<span data-ttu-id="ba31b-105">Gibt eine 16-Bit-Binärzahl zurück, in der jedes Bit nur dann auf 1 festgelegt ist, wenn das entsprechende Bit in binarynumber1 und binarynumber2 1 ist.</span><span class="sxs-lookup"><span data-stu-id="ba31b-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in both binarynumber1 and binarynumber2 is 1.</span></span> <span data-ttu-id="ba31b-106">Andernfalls ist das Bit auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ba31b-106">Otherwise, the bit is set to 0.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ba31b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba31b-107">Syntax</span></span>

<span data-ttu-id="ba31b-108">BITUND (\* \* *binarynumber1* \* \*, \* \* *binarynumber2* \* \*)</span><span class="sxs-lookup"><span data-stu-id="ba31b-108">BITAND(\*\* *binarynumber1* \*\*, \*\* *binarynumber2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ba31b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba31b-109">Parameters</span></span>

|<span data-ttu-id="ba31b-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="ba31b-110">**Name**</span></span>|<span data-ttu-id="ba31b-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="ba31b-111">**Required/Optional**</span></span>|<span data-ttu-id="ba31b-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="ba31b-112">**Data Type**</span></span>|<span data-ttu-id="ba31b-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ba31b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ba31b-114">_binäre number1_</span><span class="sxs-lookup"><span data-stu-id="ba31b-114">_binary number1_</span></span> <br/> |<span data-ttu-id="ba31b-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ba31b-115">Required</span></span>  <br/> |<span data-ttu-id="ba31b-116">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="ba31b-116">**Numeric**</span></span> <br/> |<span data-ttu-id="ba31b-117">Die erste 16-Bit-Binärzahl.</span><span class="sxs-lookup"><span data-stu-id="ba31b-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="ba31b-118">_binäre number2_</span><span class="sxs-lookup"><span data-stu-id="ba31b-118">_binary number2_</span></span> <br/> |<span data-ttu-id="ba31b-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ba31b-119">Required</span></span>  <br/> |<span data-ttu-id="ba31b-120">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="ba31b-120">**Numeric**</span></span> <br/> |<span data-ttu-id="ba31b-121">Die zweite 16-Bit-Binärzahl.</span><span class="sxs-lookup"><span data-stu-id="ba31b-121">The second 16-bit binary number.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba31b-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba31b-122">Remarks</span></span>

<span data-ttu-id="ba31b-123">Mit dieser Funktion können Sie in Bitmasken gespeicherte Shape-Eigenschaften testen und ändern, z. B. das Textformat des Shapes.</span><span class="sxs-lookup"><span data-stu-id="ba31b-123">You can use this function to test and change properties of a shape that are stored as bitmasks, for example, the shape's text format.</span></span>
  
## <a name="example"></a><span data-ttu-id="ba31b-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ba31b-124">Example</span></span>

<span data-ttu-id="ba31b-125">BITUND (12, 6)</span><span class="sxs-lookup"><span data-stu-id="ba31b-125">BITAND(12,6)</span></span>
  
<span data-ttu-id="ba31b-p103">Gibt 4 zurück. 12 entspricht 0...01100. 6 entspricht 0...00110. Das Ergebnis von BITAND(12,6) lautet 0...00100.</span><span class="sxs-lookup"><span data-stu-id="ba31b-p103">Returns 4. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITAND(12,6) = 0...00100.</span></span>
  

