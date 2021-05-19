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
ms.openlocfilehash: 6f1c459892331ec30ad93bbc860fcd038e8f4732
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418190"
---
# <a name="char-function"></a><span data-ttu-id="d0a67-103">CHAR Function</span><span class="sxs-lookup"><span data-stu-id="d0a67-103">CHAR Function</span></span>

<span data-ttu-id="d0a67-104">Gibt das ANSI-Zeichen für eine Zahl zurück.</span><span class="sxs-lookup"><span data-stu-id="d0a67-104">Returns the ANSI character for a number.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d0a67-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0a67-105">Syntax</span></span>

<span data-ttu-id="d0a67-106">CHAR(\*\* *number* \*\* )</span><span class="sxs-lookup"><span data-stu-id="d0a67-106">CHAR(\*\* *number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d0a67-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0a67-107">Parameters</span></span>

|<span data-ttu-id="d0a67-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="d0a67-108">**Name**</span></span>|<span data-ttu-id="d0a67-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="d0a67-109">**Required/Optional**</span></span>|<span data-ttu-id="d0a67-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="d0a67-110">**Data Type**</span></span>|<span data-ttu-id="d0a67-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d0a67-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d0a67-112">_Anzahl_</span><span class="sxs-lookup"><span data-stu-id="d0a67-112">_number_</span></span> <br/> |<span data-ttu-id="d0a67-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d0a67-113">Required</span></span>  <br/> |<span data-ttu-id="d0a67-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="d0a67-114">**Number**</span></span> <br/> |<span data-ttu-id="d0a67-115">Die Zahl, deren ANSI-Zeichen Sie erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="d0a67-115">The number whose ANSI character you want to get.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0a67-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d0a67-116">Remarks</span></span>

<span data-ttu-id="d0a67-117">Die resultierende Zeichenfolge ist ein Zeichen lang.</span><span class="sxs-lookup"><span data-stu-id="d0a67-117">The resulting string is one character in length.</span></span> <span data-ttu-id="d0a67-118">Der  _Parameter number_ muss eine ganze Zahl zwischen 1 und 255 (einschließlich) sein, oder die Funktion gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="d0a67-118">The  _number_ parameter must be an integer between 1 and 255 (inclusive), or the function returns an error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d0a67-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d0a67-119">Example</span></span>

<span data-ttu-id="d0a67-120">CHAR(9)</span><span class="sxs-lookup"><span data-stu-id="d0a67-120">CHAR(9)</span></span> 
  
<span data-ttu-id="d0a67-121">Gibt das Tabulatorzeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="d0a67-121">Returns the tab character.</span></span> 
  

