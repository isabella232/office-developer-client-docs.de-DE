---
title: CHAR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251406
localization_priority: Normal
ms.assetid: 0803d5d3-d804-5ffe-604d-661b35d1fc01
description: Gibt das ANSI-Zeichen für eine Zahl zurück.
ms.openlocfilehash: 209614d20dd663ed2f7ca030c25500d43f925c95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796610"
---
# <a name="char-function"></a><span data-ttu-id="e271b-103">CHAR Function</span><span class="sxs-lookup"><span data-stu-id="e271b-103">CHAR Function</span></span>

<span data-ttu-id="e271b-104">Gibt das ANSI-Zeichen für eine Zahl zurück.</span><span class="sxs-lookup"><span data-stu-id="e271b-104">Returns the ANSI character for a number.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e271b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e271b-105">Syntax</span></span>

<span data-ttu-id="e271b-106">CHAR (** *Anzahl* **)</span><span class="sxs-lookup"><span data-stu-id="e271b-106">CHAR(** *number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e271b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e271b-107">Parameters</span></span>

|<span data-ttu-id="e271b-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e271b-108">**Name**</span></span>|<span data-ttu-id="e271b-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="e271b-109">**Required/Optional**</span></span>|<span data-ttu-id="e271b-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="e271b-110">**Data Type**</span></span>|<span data-ttu-id="e271b-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e271b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e271b-112">_Anzahl_</span><span class="sxs-lookup"><span data-stu-id="e271b-112">_number_</span></span> <br/> |<span data-ttu-id="e271b-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e271b-113">Required</span></span>  <br/> |<span data-ttu-id="e271b-114">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="e271b-114">**Number**</span></span> <br/> |<span data-ttu-id="e271b-115">Die Anzahl, dessen ANSI-Zeichen, die Sie abrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="e271b-115">The number whose ANSI character you want to get.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e271b-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e271b-116">Remarks</span></span>

<span data-ttu-id="e271b-117">Die resultierende Zeichenfolge wird einem Zeichen besteht.</span><span class="sxs-lookup"><span data-stu-id="e271b-117">The resulting string is one character in length.</span></span> <span data-ttu-id="e271b-118">Der _Anzahl_ -Parameter muss eine ganze Zahl zwischen 1 und 255 (einschließlich) sein, oder die Funktion gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="e271b-118">The  _number_ parameter must be an integer between 1 and 255 (inclusive), or the function returns an error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e271b-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e271b-119">Example</span></span>

<span data-ttu-id="e271b-120">CHAR(9)</span><span class="sxs-lookup"><span data-stu-id="e271b-120">CHAR(9)</span></span> 
  
<span data-ttu-id="e271b-121">Gibt das Tabulatorzeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="e271b-121">Returns the tab character.</span></span> 
  

