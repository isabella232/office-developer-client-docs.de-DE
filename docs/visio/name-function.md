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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416797"
---
# <a name="name-function"></a><span data-ttu-id="8999c-103">NAME Function</span><span class="sxs-lookup"><span data-stu-id="8999c-103">NAME Function</span></span>

<span data-ttu-id="8999c-104">Gibt den Namen eines Blatts als Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="8999c-104">Returns a sheet's name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8999c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8999c-105">Syntax</span></span>

<span data-ttu-id="8999c-106">NAME (\* \* *langID_opt* \* \*)</span><span class="sxs-lookup"><span data-stu-id="8999c-106">NAME (\*\* *langID_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8999c-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8999c-107">Parameters</span></span>

|<span data-ttu-id="8999c-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="8999c-108">**Name**</span></span>|<span data-ttu-id="8999c-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="8999c-109">**Required/Optional**</span></span>|<span data-ttu-id="8999c-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="8999c-110">**Data Type**</span></span>|<span data-ttu-id="8999c-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8999c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8999c-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="8999c-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="8999c-113">Optional</span><span class="sxs-lookup"><span data-stu-id="8999c-113">Optional</span></span>  <br/> |<span data-ttu-id="8999c-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="8999c-114">**Number**</span></span> <br/> |<span data-ttu-id="8999c-p101">Optionales Argument. Wird verwendet, um eine Sprache für die von der Funktion zurückgegebene Zeichenfolge anzugeben. Verwenden Sie 0 (Standardwert), um die lokale Sprache anzugeben. Verwenden Sie 750, um die universelle Sprache anzugeben.</span><span class="sxs-lookup"><span data-stu-id="8999c-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8999c-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8999c-118">Return value</span></span>

<span data-ttu-id="8999c-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8999c-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8999c-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8999c-120">Remarks</span></span>

<span data-ttu-id="8999c-121">Wenn Sie einen ungültigen Sprachencode eingeben, wird die lokale Sprache verwendet.</span><span class="sxs-lookup"><span data-stu-id="8999c-121">If you pass an illegal language code, the local language is used.</span></span> 
  

