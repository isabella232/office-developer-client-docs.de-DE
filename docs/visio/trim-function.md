---
title: TRIM-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027318
localization_priority: Normal
ms.assetid: 6f2d84fd-27eb-4c2f-a2e1-43d20e0c78be
description: Entfernt alle Leerzeichen aus Text, mit Ausnahme einzelner Leerzeichen zwischen Wörtern.
ms.openlocfilehash: b947c9500012d0ceefe3e8044be387f7b810dda9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435719"
---
# <a name="trim-function"></a><span data-ttu-id="4d34e-103">TRIM Function</span><span class="sxs-lookup"><span data-stu-id="4d34e-103">TRIM Function</span></span>

<span data-ttu-id="4d34e-104">Entfernt alle Leerzeichen aus Text, mit Ausnahme einzelner Leerzeichen zwischen Wörtern.</span><span class="sxs-lookup"><span data-stu-id="4d34e-104">Removes all space from text, except for single spaces between words.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4d34e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d34e-105">Syntax</span></span>

<span data-ttu-id="4d34e-106">TRIM (\*\* *text* \*\* )</span><span class="sxs-lookup"><span data-stu-id="4d34e-106">TRIM (\*\* *text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4d34e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d34e-107">Parameters</span></span>

|<span data-ttu-id="4d34e-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="4d34e-108">**Name**</span></span>|<span data-ttu-id="4d34e-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="4d34e-109">**Required/Optional**</span></span>|<span data-ttu-id="4d34e-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="4d34e-110">**Data Type**</span></span>|<span data-ttu-id="4d34e-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4d34e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4d34e-112">_text_</span><span class="sxs-lookup"><span data-stu-id="4d34e-112">_text_</span></span> <br/> |<span data-ttu-id="4d34e-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="4d34e-113">Required</span></span>  <br/> |<span data-ttu-id="4d34e-114">**String**</span><span class="sxs-lookup"><span data-stu-id="4d34e-114">**String**</span></span> <br/> |<span data-ttu-id="4d34e-115">Der Text, aus dem die Leerzeichen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4d34e-115">The text from which you want to remove spaces.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4d34e-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d34e-116">Return value</span></span>

<span data-ttu-id="4d34e-117">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4d34e-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4d34e-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4d34e-118">Remarks</span></span>

<span data-ttu-id="4d34e-119">Sie können die Funktion TRIM bei Texten verwenden, die aus einer anderen Anwendung übernommen wurden und überzählige Leerzeichen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4d34e-119">You can use the TRIM function on text that you have received from another application that may have irregular spacing.</span></span>
  
## <a name="example"></a><span data-ttu-id="4d34e-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4d34e-120">Example</span></span>

<span data-ttu-id="4d34e-121">TRIM ("1. Januar 2003 ")</span><span class="sxs-lookup"><span data-stu-id="4d34e-121">TRIM ("January 1, 2003 ")</span></span> 
  
<span data-ttu-id="4d34e-122">Gibt "January 1, 2003" zurück.</span><span class="sxs-lookup"><span data-stu-id="4d34e-122">Returns "January 1, 2003".</span></span> 
  

