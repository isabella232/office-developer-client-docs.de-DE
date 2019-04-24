---
title: BITXOR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251401
localization_priority: Normal
ms.assetid: 672eacaf-a374-c7e2-b39b-8d42d2371aee
description: Gibt eine 16-Bit-Binärzahl zurück, in der jedes Bit auf 1 festgelegt ist, wenn das entsprechende Bit in beiden, aber nicht binären number1 und binären number2 1 ist. Andernfalls ist das Bit auf 0 festgelegt.
ms.openlocfilehash: ab8ff46fe98512d963ef4ecd5c37127353827725
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302989"
---
# <a name="bitxor-function"></a><span data-ttu-id="a66a0-104">BITXOR Function</span><span class="sxs-lookup"><span data-stu-id="a66a0-104">BITXOR Function</span></span>

<span data-ttu-id="a66a0-105">Gibt eine 16-Bit-Binärzahl zurück, in der jedes Bit auf 1 festgelegt ist, wenn das entsprechende Bit in beiden, aber nicht binären number1 und binären number2 1 ist.</span><span class="sxs-lookup"><span data-stu-id="a66a0-105">Returns a 16-bit binary number in which each bit is set to 1 if the corresponding bit in either but not both binary number1 and binary number2 is 1.</span></span> <span data-ttu-id="a66a0-106">Andernfalls ist das Bit auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a66a0-106">Otherwise, the bit is set to 0.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a66a0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a66a0-107">Syntax</span></span>

<span data-ttu-id="a66a0-108">BITXOR (\* \* *Binary number1* \* \*, \* \* *Binary number2* \* \*)</span><span class="sxs-lookup"><span data-stu-id="a66a0-108">BITXOR(\*\* *binary number1* \*\*, \*\* *binary number2* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a66a0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a66a0-109">Parameters</span></span>

|<span data-ttu-id="a66a0-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="a66a0-110">**Name**</span></span>|<span data-ttu-id="a66a0-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="a66a0-111">**Required/Optional**</span></span>|<span data-ttu-id="a66a0-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a66a0-112">**Data Type**</span></span>|<span data-ttu-id="a66a0-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a66a0-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a66a0-114">_binäre number1_</span><span class="sxs-lookup"><span data-stu-id="a66a0-114">_binary number1_</span></span> <br/> |<span data-ttu-id="a66a0-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a66a0-115">Required</span></span>  <br/> |<span data-ttu-id="a66a0-116">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="a66a0-116">**Numeric**</span></span> <br/> |<span data-ttu-id="a66a0-117">Die erste 16-Bit-Binärzahl.</span><span class="sxs-lookup"><span data-stu-id="a66a0-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="a66a0-118">_binäre number2_</span><span class="sxs-lookup"><span data-stu-id="a66a0-118">_binary number2_</span></span> <br/> |<span data-ttu-id="a66a0-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a66a0-119">Required</span></span>  <br/> |<span data-ttu-id="a66a0-120">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="a66a0-120">**Numeric**</span></span> <br/> |<span data-ttu-id="a66a0-121">Die zweite 16-Bit-Binärzahl.</span><span class="sxs-lookup"><span data-stu-id="a66a0-121">The second 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a66a0-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a66a0-122">Return value</span></span>

<span data-ttu-id="a66a0-123">16-bit Binary</span><span class="sxs-lookup"><span data-stu-id="a66a0-123">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="a66a0-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a66a0-124">Example</span></span>

<span data-ttu-id="a66a0-125">BITXOR (12, 6)</span><span class="sxs-lookup"><span data-stu-id="a66a0-125">BITXOR(12,6)</span></span>
  
<span data-ttu-id="a66a0-p103">Gibt 10 zurück. Die Zahl 12 entspricht 0...01100. Die Zahl 6 entspricht 0...00110. Daher ergibt BITXOR(12,6) den Wert 0...0,01010.</span><span class="sxs-lookup"><span data-stu-id="a66a0-p103">Returns 10. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITXOR(12,6) = 0...01010.</span></span>
  

