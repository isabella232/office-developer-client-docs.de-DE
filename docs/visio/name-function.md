---
title: NAME-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251580
localization_priority: Normal
ms.assetid: 1ca67a09-9df2-37f5-b269-e761d76bb011
description: Gibt den Namen eines Blatts als Zeichenfolge zurück.
ms.openlocfilehash: 7d0a4e9f3c5f70be07e9cc5691f52afcbc7bea68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319425"
---
# <a name="name-function"></a><span data-ttu-id="2e749-103">NAME Function</span><span class="sxs-lookup"><span data-stu-id="2e749-103">NAME Function</span></span>

<span data-ttu-id="2e749-104">Gibt den Namen eines Blatts als Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="2e749-104">Returns a sheet's name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="2e749-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e749-105">Syntax</span></span>

<span data-ttu-id="2e749-106">NAME (\* \* *langID_opt* \* \*)</span><span class="sxs-lookup"><span data-stu-id="2e749-106">NAME (\*\* *langID_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2e749-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e749-107">Parameters</span></span>

|<span data-ttu-id="2e749-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="2e749-108">**Name**</span></span>|<span data-ttu-id="2e749-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="2e749-109">**Required/Optional**</span></span>|<span data-ttu-id="2e749-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="2e749-110">**Data Type**</span></span>|<span data-ttu-id="2e749-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2e749-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2e749-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="2e749-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="2e749-113">Optional</span><span class="sxs-lookup"><span data-stu-id="2e749-113">Optional</span></span>  <br/> |<span data-ttu-id="2e749-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="2e749-114">**Number**</span></span> <br/> |<span data-ttu-id="2e749-p101">Optionales Argument. Wird verwendet, um eine Sprache für die von der Funktion zurückgegebene Zeichenfolge anzugeben. Verwenden Sie 0 (Standardwert), um die lokale Sprache anzugeben. Verwenden Sie 750, um die universelle Sprache anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2e749-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2e749-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e749-118">Return value</span></span>

<span data-ttu-id="2e749-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2e749-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2e749-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e749-120">Remarks</span></span>

<span data-ttu-id="2e749-121">Wenn Sie einen ungültigen Sprachencode eingeben, wird die lokale Sprache verwendet.</span><span class="sxs-lookup"><span data-stu-id="2e749-121">If you pass an illegal language code, the local language is used.</span></span> 
  

