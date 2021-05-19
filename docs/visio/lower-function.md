---
title: LOWER-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251459
localization_priority: Normal
ms.assetid: 1d198ea6-49e0-e462-b2cf-b65fbb920b55
description: Gibt eine Zeichenfolge zurück, die in Kleinbuchstaben konvertiert wurde.
ms.openlocfilehash: 275e5cc40bed5c3ca7d6f40b0882f523334611c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421242"
---
# <a name="lower-function"></a><span data-ttu-id="8e572-103">LOWER Function</span><span class="sxs-lookup"><span data-stu-id="8e572-103">LOWER Function</span></span>

<span data-ttu-id="8e572-104">Gibt eine Zeichenfolge zurück, die in Kleinbuchstaben konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8e572-104">Returns a string converted to lowercase.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8e572-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e572-105">Syntax</span></span>

<span data-ttu-id="8e572-106">LOWER(\*\* *Expression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="8e572-106">LOWER(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8e572-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e572-107">Parameters</span></span>

|<span data-ttu-id="8e572-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="8e572-108">**Name**</span></span>|<span data-ttu-id="8e572-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="8e572-109">**Required/Optional**</span></span>|<span data-ttu-id="8e572-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="8e572-110">**Data Type**</span></span>|<span data-ttu-id="8e572-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8e572-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8e572-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="8e572-112">_expression_</span></span> <br/> |<span data-ttu-id="8e572-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8e572-113">Required</span></span>  <br/> |<span data-ttu-id="8e572-114">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="8e572-114">**Varies**</span></span> <br/> | <span data-ttu-id="8e572-115">Eine Zeichenfolge, ein Zellbezug oder ein Ausdruck. Das Ergebnis wird in eine Zeichenfolge konvertiert, die anschließend in Kleinbuchstaben konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="8e572-115">A string, a cell reference, or an expression; the result is converted to a string which is then converted to lowercase.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8e572-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e572-116">Return value</span></span>

<span data-ttu-id="8e572-117">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8e572-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8e572-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8e572-118">Remarks</span></span>

<span data-ttu-id="8e572-119">Die Konvertierung von Groß-/Kleinbuchstaben ist länderspezifisch und basiert auf den aktuellen Benutzereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="8e572-119">The case conversion is locale-specific, based on the current user settings.</span></span> 
  
## <a name="example"></a><span data-ttu-id="8e572-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8e572-120">Example</span></span>

<span data-ttu-id="8e572-121">LOWER("gEmiScHt")</span><span class="sxs-lookup"><span data-stu-id="8e572-121">LOWER("mIxEd CAse")</span></span> 
  
<span data-ttu-id="8e572-122">Gibt "gemischt" zurück.</span><span class="sxs-lookup"><span data-stu-id="8e572-122">Returns "mixed case".</span></span> 
  

