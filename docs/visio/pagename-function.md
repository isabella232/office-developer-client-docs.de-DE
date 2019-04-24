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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339466"
---
# <a name="pagename-function"></a><span data-ttu-id="def07-103">PAGENAME Function</span><span class="sxs-lookup"><span data-stu-id="def07-103">PAGENAME Function</span></span>

<span data-ttu-id="def07-104">Gibt den Seitennamen als Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="def07-104">Returns the page name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="def07-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="def07-105">Syntax</span></span>

<span data-ttu-id="def07-106">PAGEname (\* \* *langID_opt* \* \*)</span><span class="sxs-lookup"><span data-stu-id="def07-106">PAGENAME (\*\* *langID_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="def07-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="def07-107">Parameters</span></span>

|<span data-ttu-id="def07-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="def07-108">**Name**</span></span>|<span data-ttu-id="def07-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="def07-109">**Required/Optional**</span></span>|<span data-ttu-id="def07-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="def07-110">**Data Type**</span></span>|<span data-ttu-id="def07-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="def07-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="def07-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="def07-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="def07-113">Optional</span><span class="sxs-lookup"><span data-stu-id="def07-113">Optional</span></span>  <br/> |<span data-ttu-id="def07-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="def07-114">**Number**</span></span> <br/> |<span data-ttu-id="def07-p101">Optionales Argument. Wird verwendet, um eine Sprache für die von der Funktion zurückgegebene Zeichenfolge anzugeben. Verwenden Sie 0 (Standardwert), um die lokale Sprache anzugeben. Verwenden Sie 750, um die universelle Sprache anzugeben.</span><span class="sxs-lookup"><span data-stu-id="def07-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="def07-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="def07-118">Return value</span></span>

<span data-ttu-id="def07-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="def07-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="def07-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="def07-120">Remarks</span></span>

<span data-ttu-id="def07-121">Wenn Sie einen ungültigen Sprachencode eingeben, wird die lokale Sprache verwendet.</span><span class="sxs-lookup"><span data-stu-id="def07-121">If you pass an illegal language code, the local language is used.</span></span>
  

