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
description: Gibt eine 16-Bit-Binärzahl in der jedes Bit auf 1 festgelegt ist, nur, wenn das entsprechende Bit in Binärzahl1 und binarynumber2 1 ist. Andernfalls wird das Bit auf 0 festgelegt.
ms.openlocfilehash: 0b501bb383596e3f2f39ea14f2cb9eb4bf40b25b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796496"
---
# <a name="bitand-function"></a><span data-ttu-id="dba9c-104">BITAND Function</span><span class="sxs-lookup"><span data-stu-id="dba9c-104">BITAND Function</span></span>

<span data-ttu-id="dba9c-105">Gibt eine 16-Bit-Binärzahl in der jedes Bit auf 1 festgelegt ist, nur, wenn das entsprechende Bit in Binärzahl1 und binarynumber2 1 ist.</span><span class="sxs-lookup"><span data-stu-id="dba9c-105">Returns a 16-bit binary number in which each bit is set to 1 only if the corresponding bit in both binarynumber1 and binarynumber2 is 1.</span></span> <span data-ttu-id="dba9c-106">Andernfalls wird das Bit auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dba9c-106">Otherwise, the bit is set to 0.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="dba9c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dba9c-107">Syntax</span></span>

<span data-ttu-id="dba9c-108">BITAND (** *Binärzahl1* **, ** *binarynumber2* **)</span><span class="sxs-lookup"><span data-stu-id="dba9c-108">BITAND(** *binarynumber1* **, ** *binarynumber2* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dba9c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="dba9c-109">Parameters</span></span>

|<span data-ttu-id="dba9c-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="dba9c-110">**Name**</span></span>|<span data-ttu-id="dba9c-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="dba9c-111">**Required/Optional**</span></span>|<span data-ttu-id="dba9c-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="dba9c-112">**Data Type**</span></span>|<span data-ttu-id="dba9c-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dba9c-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dba9c-114">_binäre Zahl1_</span><span class="sxs-lookup"><span data-stu-id="dba9c-114">_binary number1_</span></span> <br/> |<span data-ttu-id="dba9c-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dba9c-115">Required</span></span>  <br/> |<span data-ttu-id="dba9c-116">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="dba9c-116">**Numeric**</span></span> <br/> |<span data-ttu-id="dba9c-117">Die erste 16-Bit-Binärzahl.</span><span class="sxs-lookup"><span data-stu-id="dba9c-117">The first 16-bit binary number.</span></span>  <br/> |
| <span data-ttu-id="dba9c-118">_binäre Zahl2_</span><span class="sxs-lookup"><span data-stu-id="dba9c-118">_binary number2_</span></span> <br/> |<span data-ttu-id="dba9c-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dba9c-119">Required</span></span>  <br/> |<span data-ttu-id="dba9c-120">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="dba9c-120">**Numeric**</span></span> <br/> |<span data-ttu-id="dba9c-121">Die zweite 16-Bit-Binärzahl.</span><span class="sxs-lookup"><span data-stu-id="dba9c-121">The second 16-bit binary number.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dba9c-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dba9c-122">Remarks</span></span>

<span data-ttu-id="dba9c-123">Mit dieser Funktion können Sie in Bitmasken gespeicherte Shape-Eigenschaften testen und ändern, z. B. das Textformat des Shapes.</span><span class="sxs-lookup"><span data-stu-id="dba9c-123">You can use this function to test and change properties of a shape that are stored as bitmasks, for example, the shape's text format.</span></span>
  
## <a name="example"></a><span data-ttu-id="dba9c-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="dba9c-124">Example</span></span>

<span data-ttu-id="dba9c-125">BITAND(12,6)</span><span class="sxs-lookup"><span data-stu-id="dba9c-125">BITAND(12,6)</span></span>
  
<span data-ttu-id="dba9c-p103">Gibt 4 zurück. 12 entspricht 0...01100. 6 entspricht 0...00110. Das Ergebnis von BITAND(12,6) lautet 0...00100.</span><span class="sxs-lookup"><span data-stu-id="dba9c-p103">Returns 4. The 12 = 0...01100. The 6 = 0...00110. Therefore, BITAND(12,6) = 0...00100.</span></span>
  

