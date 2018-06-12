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
description: Gibt den Namen eines Zeichenblatts als Zeichenfolge zurück.
ms.openlocfilehash: 0d3a70573177d8e16a16972d0a08245381b209dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797537"
---
# <a name="name-function"></a><span data-ttu-id="5ab41-103">NAME Function</span><span class="sxs-lookup"><span data-stu-id="5ab41-103">NAME Function</span></span>

<span data-ttu-id="5ab41-104">Gibt den Namen eines Zeichenblatts als Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="5ab41-104">Returns a sheet's name as a string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5ab41-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ab41-105">Syntax</span></span>

<span data-ttu-id="5ab41-106">NAME (** *LangID_opt* **)</span><span class="sxs-lookup"><span data-stu-id="5ab41-106">NAME (** *langID_opt* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5ab41-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ab41-107">Parameters</span></span>

|<span data-ttu-id="5ab41-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="5ab41-108">**Name**</span></span>|<span data-ttu-id="5ab41-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="5ab41-109">**Required/Optional**</span></span>|<span data-ttu-id="5ab41-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="5ab41-110">**Data Type**</span></span>|<span data-ttu-id="5ab41-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5ab41-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5ab41-112">_langID_opt_</span><span class="sxs-lookup"><span data-stu-id="5ab41-112">_langID_opt_</span></span> <br/> |<span data-ttu-id="5ab41-113">Optional</span><span class="sxs-lookup"><span data-stu-id="5ab41-113">Optional</span></span>  <br/> |<span data-ttu-id="5ab41-114">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="5ab41-114">**Number**</span></span> <br/> |<span data-ttu-id="5ab41-p101">Optionales Argument. Wird verwendet, um eine Sprache für die von der Funktion zurückgegebene Zeichenfolge anzugeben. Verwenden Sie 0 (Standardwert), um die lokale Sprache anzugeben. Verwenden Sie 750, um die universelle Sprache anzugeben.</span><span class="sxs-lookup"><span data-stu-id="5ab41-p101">Use to specify a language for the string the function returns. Use 0 (default value) to specify the local language. Use 750 to specify universal language.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5ab41-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="5ab41-118">Return value</span></span>

<span data-ttu-id="5ab41-119">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5ab41-119">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5ab41-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ab41-120">Remarks</span></span>

<span data-ttu-id="5ab41-121">Wenn Sie einen ungültigen Sprachencode eingeben, wird die lokale Sprache verwendet.</span><span class="sxs-lookup"><span data-stu-id="5ab41-121">If you pass an illegal language code, the local language is used.</span></span> 
  

