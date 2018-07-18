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
description: Name der Seite zurückgegeben als Zeichenfolge.
ms.openlocfilehash: 530707530d60955f460d6a747024b98ebdd5ab62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797590"
---
# <a name="pagename-function"></a><span data-ttu-id="b74c6-103">PAGENAME Function</span><span class="sxs-lookup"><span data-stu-id="b74c6-103">PAGENAME Function</span></span>

<span data-ttu-id="b74c6-104">Name der Seite zurückgegeben als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="b74c6-104">Returns the page name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b74c6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b74c6-105">Syntax</span></span>

<span data-ttu-id="b74c6-106">PAGENAME (** *LangID_opt* **)</span><span class="sxs-lookup"><span data-stu-id="b74c6-106">PAGENAME (** *langID_opt* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b74c6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b74c6-107">Parameters</span></span>

|<span data-ttu-id="b74c6-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="b74c6-108">**Name**</span></span>|<span data-ttu-id="b74c6-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="b74c6-109">**Required/Optional**</span></span>|<span data-ttu-id="b74c6-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="b74c6-110">**Data Type**</span></span>|<span data-ttu-id="b74c6-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b74c6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b74c6-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="b74c6-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="b74c6-113">Optional</span><span class="sxs-lookup"><span data-stu-id="b74c6-113">Optional</span></span>  <br/> |<span data-ttu-id="b74c6-114">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="b74c6-114">**Number**</span></span> <br/> |<span data-ttu-id="b74c6-p101">Optionales Argument. Wird verwendet, um eine Sprache für die von der Funktion zurückgegebene Zeichenfolge anzugeben. Verwenden Sie 0 (Standardwert), um die lokale Sprache anzugeben. Verwenden Sie 750, um die universelle Sprache anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b74c6-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b74c6-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="b74c6-118">Return value</span></span>

<span data-ttu-id="b74c6-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b74c6-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b74c6-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b74c6-120">Remarks</span></span>

<span data-ttu-id="b74c6-121">Wenn Sie einen ungültigen Sprachencode eingeben, wird die lokale Sprache verwendet.</span><span class="sxs-lookup"><span data-stu-id="b74c6-121">If you pass an illegal language code, the local language is used.</span></span>
  

