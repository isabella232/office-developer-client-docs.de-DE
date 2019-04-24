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
description: Gibt den Masternamen eines Blatts als Zeichenfolge zurück oder gibt die Zeichenfolge "kein Master" zurück, wenn das Blatt keinen Master hat.
ms.openlocfilehash: 7732cf9e8b23e2fd0fc2e3f2cc8d9ef4f39fd67f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341797"
---
# <a name="mastername-function"></a><span data-ttu-id="03cf8-103">MASTERNAME Function</span><span class="sxs-lookup"><span data-stu-id="03cf8-103">MASTERNAME Function</span></span>

<span data-ttu-id="03cf8-104">Gibt den Masternamen eines Blatts als Zeichenfolge zurück oder gibt die Zeichen\<Folge "\>kein Master" zurück, wenn das Blatt keinen Master hat.</span><span class="sxs-lookup"><span data-stu-id="03cf8-104">Returns a sheet's master name as a string, or returns the string "\<no master\>" if the sheet doesn't have a master.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="03cf8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="03cf8-105">Syntax</span></span>

<span data-ttu-id="03cf8-106">MASTERname ([\* \* *langID_opt* \* \*])</span><span class="sxs-lookup"><span data-stu-id="03cf8-106">MASTERNAME ([ \*\* *langID_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="03cf8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="03cf8-107">Parameters</span></span>

|<span data-ttu-id="03cf8-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="03cf8-108">**Name**</span></span>|<span data-ttu-id="03cf8-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="03cf8-109">**Required/Optional**</span></span>|<span data-ttu-id="03cf8-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="03cf8-110">**Data Type**</span></span>|<span data-ttu-id="03cf8-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="03cf8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="03cf8-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="03cf8-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="03cf8-113">Optional</span><span class="sxs-lookup"><span data-stu-id="03cf8-113">Optional</span></span>  <br/> |<span data-ttu-id="03cf8-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="03cf8-114">**Number**</span></span> <br/> |<span data-ttu-id="03cf8-p101">Optionales Argument. Wird verwendet, um eine Sprache für die von der Funktion zurückgegebene Zeichenfolge anzugeben. Verwenden Sie 0 (Standardwert), um die lokale Sprache anzugeben. Verwenden Sie 750, um die universelle Sprache anzugeben.</span><span class="sxs-lookup"><span data-stu-id="03cf8-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="03cf8-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03cf8-118">Return value</span></span>

<span data-ttu-id="03cf8-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="03cf8-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="03cf8-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03cf8-120">Remarks</span></span>

<span data-ttu-id="03cf8-121">Wenn Sie einen ungültigen Sprachencode eingeben, wird die lokale Sprache verwendet.</span><span class="sxs-lookup"><span data-stu-id="03cf8-121">If you pass an illegal language code, the local language is used.</span></span> 
  

