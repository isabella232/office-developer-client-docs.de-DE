---
title: PAGENAME-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251577
localization_priority: Normal
ms.assetid: 12e45f46-e773-9445-4c7f-c726ab648671
description: Gibt den Seitennamen als Zeichenfolge zurück.
ms.openlocfilehash: d5527bde58a68c96bd75773f3a0a8c30f64fa20d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438652"
---
# <a name="pagename-function"></a><span data-ttu-id="c8f65-103">PAGENAME Function</span><span class="sxs-lookup"><span data-stu-id="c8f65-103">PAGENAME Function</span></span>

<span data-ttu-id="c8f65-104">Gibt den Seitennamen als Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="c8f65-104">Returns the page name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c8f65-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8f65-105">Syntax</span></span>

<span data-ttu-id="c8f65-106">PAGEname (\* \* *langID_opt* \* \*)</span><span class="sxs-lookup"><span data-stu-id="c8f65-106">PAGENAME (\*\* *langID_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c8f65-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8f65-107">Parameters</span></span>

|<span data-ttu-id="c8f65-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c8f65-108">**Name**</span></span>|<span data-ttu-id="c8f65-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="c8f65-109">**Required/Optional**</span></span>|<span data-ttu-id="c8f65-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="c8f65-110">**Data Type**</span></span>|<span data-ttu-id="c8f65-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c8f65-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c8f65-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="c8f65-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="c8f65-113">Optional</span><span class="sxs-lookup"><span data-stu-id="c8f65-113">Optional</span></span>  <br/> |<span data-ttu-id="c8f65-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="c8f65-114">**Number**</span></span> <br/> |<span data-ttu-id="c8f65-p101">Optionales Argument. Wird verwendet, um eine Sprache für die von der Funktion zurückgegebene Zeichenfolge anzugeben. Verwenden Sie 0 (Standardwert), um die lokale Sprache anzugeben. Verwenden Sie 750, um die universelle Sprache anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c8f65-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c8f65-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8f65-118">Return value</span></span>

<span data-ttu-id="c8f65-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c8f65-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c8f65-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8f65-120">Remarks</span></span>

<span data-ttu-id="c8f65-121">Wenn Sie einen ungültigen Sprachencode eingeben, wird die lokale Sprache verwendet.</span><span class="sxs-lookup"><span data-stu-id="c8f65-121">If you pass an illegal language code, the local language is used.</span></span>
  

