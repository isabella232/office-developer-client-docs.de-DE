---
title: MASTERNAME-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251581
localization_priority: Normal
ms.assetid: 519d79d4-9178-2231-c26d-aa7f31a43412
description: Gibt den Namen eines Zeichenblatts Master-Shape als Zeichenfolge zurück, oder gibt die Zeichenfolge "kein Master-Shape" zurück, wenn das Blatt nicht über ein Master-Shape verfügt.
ms.openlocfilehash: c1d5891fba0f967cde4a4e9ca58d07f87239f0b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797456"
---
# <a name="mastername-function"></a><span data-ttu-id="b89bc-103">MASTERNAME Function</span><span class="sxs-lookup"><span data-stu-id="b89bc-103">MASTERNAME Function</span></span>

<span data-ttu-id="b89bc-104">Gibt den Namen eines Zeichenblatts Master-Shape als Zeichenfolge zurück oder die Zeichenfolge "\<kein Master-Shape\>" Wenn das Blatt nicht über ein Master-Shape verfügt.</span><span class="sxs-lookup"><span data-stu-id="b89bc-104">Returns a sheet's master name as a string, or returns the string "\<no master\>" if the sheet doesn't have a master.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b89bc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b89bc-105">Syntax</span></span>

<span data-ttu-id="b89bc-106">MASTERNAME ([** *LangID_opt* **])</span><span class="sxs-lookup"><span data-stu-id="b89bc-106">MASTERNAME ([ ** *langID_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b89bc-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b89bc-107">Parameters</span></span>

|<span data-ttu-id="b89bc-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="b89bc-108">**Name**</span></span>|<span data-ttu-id="b89bc-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="b89bc-109">**Required/Optional**</span></span>|<span data-ttu-id="b89bc-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="b89bc-110">**Data Type**</span></span>|<span data-ttu-id="b89bc-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b89bc-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b89bc-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="b89bc-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="b89bc-113">Optional</span><span class="sxs-lookup"><span data-stu-id="b89bc-113">Optional</span></span>  <br/> |<span data-ttu-id="b89bc-114">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="b89bc-114">**Number**</span></span> <br/> |<span data-ttu-id="b89bc-p101">Optionales Argument. Wird verwendet, um eine Sprache für die von der Funktion zurückgegebene Zeichenfolge anzugeben. Verwenden Sie 0 (Standardwert), um die lokale Sprache anzugeben. Verwenden Sie 750, um die universelle Sprache anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b89bc-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b89bc-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="b89bc-118">Return value</span></span>

<span data-ttu-id="b89bc-119">String</span><span class="sxs-lookup"><span data-stu-id="b89bc-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b89bc-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b89bc-120">Remarks</span></span>

<span data-ttu-id="b89bc-121">Wenn Sie einen ungültigen Sprachencode eingeben, wird die lokale Sprache verwendet.</span><span class="sxs-lookup"><span data-stu-id="b89bc-121">If you pass an illegal language code, the local language is used.</span></span> 
  

