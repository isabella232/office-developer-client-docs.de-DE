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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414753"
---
# <a name="mastername-function"></a><span data-ttu-id="8c641-103">MASTERNAME Function</span><span class="sxs-lookup"><span data-stu-id="8c641-103">MASTERNAME Function</span></span>

<span data-ttu-id="8c641-104">Gibt den Masternamen eines Blatts als Zeichenfolge zurück oder gibt die Zeichenfolge "kein Master" zurück, wenn das Blatt keinen \< \> Master hat.</span><span class="sxs-lookup"><span data-stu-id="8c641-104">Returns a sheet's master name as a string, or returns the string "\<no master\>" if the sheet doesn't have a master.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8c641-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c641-105">Syntax</span></span>

<span data-ttu-id="8c641-106">MASTERNAME ([ \*\* *langID_opt* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="8c641-106">MASTERNAME ([ \*\* *langID_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8c641-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c641-107">Parameters</span></span>

|<span data-ttu-id="8c641-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="8c641-108">**Name**</span></span>|<span data-ttu-id="8c641-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="8c641-109">**Required/Optional**</span></span>|<span data-ttu-id="8c641-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="8c641-110">**Data Type**</span></span>|<span data-ttu-id="8c641-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8c641-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8c641-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="8c641-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="8c641-113">Optional.</span><span class="sxs-lookup"><span data-stu-id="8c641-113">Optional</span></span>  <br/> |<span data-ttu-id="8c641-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="8c641-114">**Number**</span></span> <br/> |<span data-ttu-id="8c641-p101">Optionales Argument. Wird verwendet, um eine Sprache für die von der Funktion zurückgegebene Zeichenfolge anzugeben. Verwenden Sie 0 (Standardwert), um die lokale Sprache anzugeben. Verwenden Sie 750, um die universelle Sprache anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8c641-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8c641-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c641-118">Return value</span></span>

<span data-ttu-id="8c641-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8c641-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8c641-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8c641-120">Remarks</span></span>

<span data-ttu-id="8c641-121">Wenn Sie einen ungültigen Sprachencode eingeben, wird die lokale Sprache verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c641-121">If you pass an illegal language code, the local language is used.</span></span> 
  

