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
ms.openlocfilehash: b396572041e880451ceb1ec6f0508528c0807bfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798319"
---
# <a name="trim-function"></a><span data-ttu-id="902cb-103">TRIM Function</span><span class="sxs-lookup"><span data-stu-id="902cb-103">TRIM Function</span></span>

<span data-ttu-id="902cb-104">Entfernt alle Leerzeichen aus Text, mit Ausnahme einzelner Leerzeichen zwischen Wörtern.</span><span class="sxs-lookup"><span data-stu-id="902cb-104">Removes all space from text, except for single spaces between words.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="902cb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="902cb-105">Syntax</span></span>

<span data-ttu-id="902cb-106">TRIM (** *Text* **)</span><span class="sxs-lookup"><span data-stu-id="902cb-106">TRIM (** *text* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="902cb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="902cb-107">Parameters</span></span>

|<span data-ttu-id="902cb-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="902cb-108">**Name**</span></span>|<span data-ttu-id="902cb-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="902cb-109">**Required/Optional**</span></span>|<span data-ttu-id="902cb-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="902cb-110">**Data Type**</span></span>|<span data-ttu-id="902cb-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="902cb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="902cb-112">_text_</span><span class="sxs-lookup"><span data-stu-id="902cb-112">_text_</span></span> <br/> |<span data-ttu-id="902cb-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="902cb-113">Required</span></span>  <br/> |<span data-ttu-id="902cb-114">**String**</span><span class="sxs-lookup"><span data-stu-id="902cb-114">**String**</span></span> <br/> |<span data-ttu-id="902cb-115">Der Text, aus dem die Leerzeichen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="902cb-115">The text from which you want to remove spaces.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="902cb-116">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="902cb-116">Return value</span></span>

<span data-ttu-id="902cb-117">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="902cb-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="902cb-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="902cb-118">Remarks</span></span>

<span data-ttu-id="902cb-119">Sie können die Funktion TRIM bei Texten verwenden, die aus einer anderen Anwendung übernommen wurden und überzählige Leerzeichen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="902cb-119">You can use the TRIM function on text that you have received from another application that may have irregular spacing.</span></span>
  
## <a name="example"></a><span data-ttu-id="902cb-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="902cb-120">Example</span></span>

<span data-ttu-id="902cb-121">TRIM ("Januar 1, 2003")</span><span class="sxs-lookup"><span data-stu-id="902cb-121">TRIM ("January 1, 2003 ")</span></span> 
  
<span data-ttu-id="902cb-122">Gibt "January 1, 2003" zurück.</span><span class="sxs-lookup"><span data-stu-id="902cb-122">Returns "January 1, 2003".</span></span> 
  

