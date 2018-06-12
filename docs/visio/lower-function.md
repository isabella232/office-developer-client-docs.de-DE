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
description: Gibt eine Zeichenfolge in Kleinbuchstaben konvertiert.
ms.openlocfilehash: da626ee0bb0474fceafcf93ed5c835aacd0034fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797431"
---
# <a name="lower-function"></a><span data-ttu-id="91246-103">LOWER Function</span><span class="sxs-lookup"><span data-stu-id="91246-103">LOWER Function</span></span>

<span data-ttu-id="91246-104">Gibt eine Zeichenfolge in Kleinbuchstaben konvertiert.</span><span class="sxs-lookup"><span data-stu-id="91246-104">Returns a string converted to lowercase.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="91246-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="91246-105">Syntax</span></span>

<span data-ttu-id="91246-106">NIEDRIGERE (** *Ausdruck* **)</span><span class="sxs-lookup"><span data-stu-id="91246-106">LOWER(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="91246-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="91246-107">Parameters</span></span>

|<span data-ttu-id="91246-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="91246-108">**Name**</span></span>|<span data-ttu-id="91246-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="91246-109">**Required/Optional**</span></span>|<span data-ttu-id="91246-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="91246-110">**Data Type**</span></span>|<span data-ttu-id="91246-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="91246-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="91246-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="91246-112">_expression_</span></span> <br/> |<span data-ttu-id="91246-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="91246-113">Required</span></span>  <br/> |<span data-ttu-id="91246-114">**Variiert**</span><span class="sxs-lookup"><span data-stu-id="91246-114">**Varies**</span></span> <br/> | <span data-ttu-id="91246-115">Eine Zeichenfolge, ein Zellbezug oder ein Ausdruck. Das Ergebnis wird in eine Zeichenfolge konvertiert, die anschließend in Kleinbuchstaben konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="91246-115">A string, a cell reference, or an expression; the result is converted to a string which is then converted to lowercase.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="91246-116">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="91246-116">Return value</span></span>

<span data-ttu-id="91246-117">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="91246-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="91246-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91246-118">Remarks</span></span>

<span data-ttu-id="91246-119">Die Konvertierung von Groß-/Kleinbuchstaben ist länderspezifisch und basiert auf den aktuellen Benutzereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="91246-119">The case conversion is locale-specific, based on the current user settings.</span></span> 
  
## <a name="example"></a><span data-ttu-id="91246-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="91246-120">Example</span></span>

<span data-ttu-id="91246-121">LOWER("gEmiScHt")</span><span class="sxs-lookup"><span data-stu-id="91246-121">LOWER("mIxEd CAse")</span></span> 
  
<span data-ttu-id="91246-122">Gibt "gemischt" zurück.</span><span class="sxs-lookup"><span data-stu-id="91246-122">Returns "mixed case".</span></span> 
  

