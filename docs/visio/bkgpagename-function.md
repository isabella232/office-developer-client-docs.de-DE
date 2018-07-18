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
description: Gibt den Namen einer Hintergrund als Zeichenfolge zurück.
ms.openlocfilehash: 290fa62242298b3c513bf2870df37204fab31bf3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796528"
---
# <a name="bkgpagename-function"></a><span data-ttu-id="23be5-103">BKGPAGENAME Function</span><span class="sxs-lookup"><span data-stu-id="23be5-103">BKGPAGENAME Function</span></span>

<span data-ttu-id="23be5-104">Gibt den Namen einer Hintergrund als Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="23be5-104">Returns a background page name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="23be5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="23be5-105">Syntax</span></span>

<span data-ttu-id="23be5-106">BKGPAGENAME (** *LangID_opt* **)</span><span class="sxs-lookup"><span data-stu-id="23be5-106">BKGPAGENAME (** *langID_opt* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="23be5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="23be5-107">Parameters</span></span>

|<span data-ttu-id="23be5-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="23be5-108">**Name**</span></span>|<span data-ttu-id="23be5-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="23be5-109">**Required/Optional**</span></span>|<span data-ttu-id="23be5-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="23be5-110">**Data Type**</span></span>|<span data-ttu-id="23be5-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="23be5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="23be5-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="23be5-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="23be5-113">Optional</span><span class="sxs-lookup"><span data-stu-id="23be5-113">Optional</span></span>  <br/> |<span data-ttu-id="23be5-114">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="23be5-114">**Numeric**</span></span> <br/> |<span data-ttu-id="23be5-p101">Optionales Argument. Wird verwendet, um eine Sprache für die von der Funktion zurückgegebene Zeichenfolge anzugeben. Verwenden Sie 0 (Standardwert), um die lokale Sprache anzugeben. Verwenden Sie 750, um die universelle Sprache anzugeben.</span><span class="sxs-lookup"><span data-stu-id="23be5-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="23be5-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="23be5-118">Return value</span></span>

<span data-ttu-id="23be5-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="23be5-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="23be5-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23be5-120">Remarks</span></span>

<span data-ttu-id="23be5-121">Wenn die Seite für die Sie die Funktion verwenden ein Hintergrundblatt die Zeichenfolge nicht "\<kein Hintergrund\>" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="23be5-121">If the page for which you are using the function doesn't have a background page, the string "\<no background\>" is returned.</span></span> 
  
<span data-ttu-id="23be5-122">Wenn Sie einen ungültigen Sprachencode eingeben, wird die lokale Sprache verwendet.</span><span class="sxs-lookup"><span data-stu-id="23be5-122">If you pass an illegal language code, the local language is used.</span></span> 
  

