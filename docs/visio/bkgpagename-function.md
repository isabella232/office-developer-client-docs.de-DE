---
title: BKGPAGENAME-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253219
localization_priority: Normal
ms.assetid: f6e410ef-54d5-9c08-926b-97a2a9786622
description: Gibt einen Hintergrundseiten Namen als Zeichenfolge zurück.
ms.openlocfilehash: 3b628315052117fe853c8f9c0fc36572de25d871
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358541"
---
# <a name="bkgpagename-function"></a><span data-ttu-id="54e61-103">BKGPAGENAME Function</span><span class="sxs-lookup"><span data-stu-id="54e61-103">BKGPAGENAME Function</span></span>

<span data-ttu-id="54e61-104">Gibt einen Hintergrundseiten Namen als Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="54e61-104">Returns a background page name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="54e61-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="54e61-105">Syntax</span></span>

<span data-ttu-id="54e61-106">BKGPAGENAME (\* \* *langID_opt* \* \*)</span><span class="sxs-lookup"><span data-stu-id="54e61-106">BKGPAGENAME (\*\* *langID_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="54e61-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="54e61-107">Parameters</span></span>

|<span data-ttu-id="54e61-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="54e61-108">**Name**</span></span>|<span data-ttu-id="54e61-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="54e61-109">**Required/Optional**</span></span>|<span data-ttu-id="54e61-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="54e61-110">**Data Type**</span></span>|<span data-ttu-id="54e61-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="54e61-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="54e61-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="54e61-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="54e61-113">Optional</span><span class="sxs-lookup"><span data-stu-id="54e61-113">Optional</span></span>  <br/> |<span data-ttu-id="54e61-114">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="54e61-114">**Numeric**</span></span> <br/> |<span data-ttu-id="54e61-p101">Optionales Argument. Wird verwendet, um eine Sprache für die von der Funktion zurückgegebene Zeichenfolge anzugeben. Verwenden Sie 0 (Standardwert), um die lokale Sprache anzugeben. Verwenden Sie 750, um die universelle Sprache anzugeben.</span><span class="sxs-lookup"><span data-stu-id="54e61-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="54e61-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54e61-118">Return value</span></span>

<span data-ttu-id="54e61-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="54e61-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="54e61-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54e61-120">Remarks</span></span>

<span data-ttu-id="54e61-121">Wenn die Seite, für die Sie die Funktion verwenden, keinen Hintergrund enthält, wird die Zeichenfolge\<"kein\>Hintergrund" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="54e61-121">If the page for which you are using the function doesn't have a background page, the string "\<no background\>" is returned.</span></span> 
  
<span data-ttu-id="54e61-122">Wenn Sie einen ungültigen Sprachencode eingeben, wird die lokale Sprache verwendet.</span><span class="sxs-lookup"><span data-stu-id="54e61-122">If you pass an illegal language code, the local language is used.</span></span> 
  

