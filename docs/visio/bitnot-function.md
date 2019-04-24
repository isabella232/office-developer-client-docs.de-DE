---
title: BITNOT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251399
localization_priority: Normal
ms.assetid: 7b6486bb-3618-3747-4b00-93bd55767c1c
description: Gibt eine 16-Bit-Binärzahl zurück, in der jedes Bit nur dann auf 1 festgelegt ist, wenn das entsprechende Bit in binary number 0 ist. Andernfalls ist das Bit auf 0 festgelegt.
ms.openlocfilehash: 34ea6fd614feae8e3c8e97e34b7ff6c531f4c123
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330009"
---
# <a name="bitnot-function"></a><span data-ttu-id="8e89c-104">BITNOT Function</span><span class="sxs-lookup"><span data-stu-id="8e89c-104">BITNOT Function</span></span>

<span data-ttu-id="8e89c-105">Gibt eine 16-Bit-Binärzahl zurück, in der jedes Bit nur dann auf 1 festgelegt ist, wenn das entsprechende Bit in binary number 0 ist.</span><span class="sxs-lookup"><span data-stu-id="8e89c-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in binary number is 0.</span></span> <span data-ttu-id="8e89c-106">Andernfalls ist das Bit auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8e89c-106">Otherwise, the bit is set to 0.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8e89c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e89c-107">Syntax</span></span>

<span data-ttu-id="8e89c-108">BITNOT (\* \* *Binärzahl* \* \*)</span><span class="sxs-lookup"><span data-stu-id="8e89c-108">BITNOT(\*\* *binary number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8e89c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e89c-109">Parameters</span></span>

|<span data-ttu-id="8e89c-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="8e89c-110">**Name**</span></span>|<span data-ttu-id="8e89c-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="8e89c-111">**Required/Optional**</span></span>|<span data-ttu-id="8e89c-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="8e89c-112">**Data Type**</span></span>|<span data-ttu-id="8e89c-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8e89c-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8e89c-114">_binäre Zahl_</span><span class="sxs-lookup"><span data-stu-id="8e89c-114">_binary number_</span></span> <br/> |<span data-ttu-id="8e89c-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8e89c-115">Required</span></span>  <br/> |<span data-ttu-id="8e89c-116">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="8e89c-116">**Numeric**</span></span> <br/> |<span data-ttu-id="8e89c-117">Eine 16-Bit-Binärzahl.</span><span class="sxs-lookup"><span data-stu-id="8e89c-117">A 16-bit binary number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8e89c-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e89c-118">Return value</span></span>

<span data-ttu-id="8e89c-119">16-bit Binary</span><span class="sxs-lookup"><span data-stu-id="8e89c-119">16-bit Binary</span></span>
  
## <a name="example"></a><span data-ttu-id="8e89c-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8e89c-120">Example</span></span>

<span data-ttu-id="8e89c-121">BITNOT (6)</span><span class="sxs-lookup"><span data-stu-id="8e89c-121">BITNOT(6)</span></span>
  
<span data-ttu-id="8e89c-p103">Gibt 65529 zurück. Die Zahl 6 entspricht 0...00110. Daher ergibt BITNOT(6) den Wert 1...11001.</span><span class="sxs-lookup"><span data-stu-id="8e89c-p103">Returns 65529. The 6 = 0...00110. Therefore, BITNOT(6) = 1...11001.</span></span>
  

