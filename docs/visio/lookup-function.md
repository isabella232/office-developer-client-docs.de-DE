---
title: LOOKUP-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251457
localization_priority: Normal
ms.assetid: cb6ec664-6062-75d0-1514-8058b98c2c36
description: Gibt einen nullbasierten Index, der gibt die Position der Teilzeichenfolge Schlüssel in einer Liste oder gibt-1 zurück, wenn die Zielzeichenfolge das Trennzeichen enthält.
ms.openlocfilehash: e1fd433282871135d385d1c980c77041cd49cdf4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797423"
---
# <a name="lookup-function"></a><span data-ttu-id="e5912-103">LOOKUP Function</span><span class="sxs-lookup"><span data-stu-id="e5912-103">LOOKUP Function</span></span>

<span data-ttu-id="e5912-104">Gibt einen nullbasierten Index, der gibt die Position der Teilzeichenfolge _Schlüssel_ in einer _Liste_oder gibt-1 zurück, wenn die Zielzeichenfolge das _Trennzeichen_enthält.</span><span class="sxs-lookup"><span data-stu-id="e5912-104">Returns a zero-based index that indicates the location of the substring  _key_ in a  _list_, or returns -1 if the target string contains the  _delimiter_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e5912-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5912-105">Syntax</span></span>

<span data-ttu-id="e5912-106">Nachschlagen ("** *Schlüssel* **","** *Liste* **"[,"** *Trennzeichen* **"])</span><span class="sxs-lookup"><span data-stu-id="e5912-106">LOOKUP(" ** *key* ** "," ** *list* ** "[," ** *delimiter* ** "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e5912-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5912-107">Parameters</span></span>

|<span data-ttu-id="e5912-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e5912-108">**Name**</span></span>|<span data-ttu-id="e5912-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="e5912-109">**Required/Optional**</span></span>|<span data-ttu-id="e5912-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="e5912-110">**Data Type**</span></span>|<span data-ttu-id="e5912-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e5912-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e5912-112">_Schlüssel_</span><span class="sxs-lookup"><span data-stu-id="e5912-112">_key_</span></span> <br/> |<span data-ttu-id="e5912-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e5912-113">Required</span></span>  <br/> |<span data-ttu-id="e5912-114">**String**</span><span class="sxs-lookup"><span data-stu-id="e5912-114">**String**</span></span> <br/> |<span data-ttu-id="e5912-115">Die zu suchende Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e5912-115">The string that you want to look up.</span></span>  <br/> |
| <span data-ttu-id="e5912-116">_list_</span><span class="sxs-lookup"><span data-stu-id="e5912-116">_list_</span></span> <br/> |<span data-ttu-id="e5912-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e5912-117">Required</span></span>  <br/> |<span data-ttu-id="e5912-118">**String**</span><span class="sxs-lookup"><span data-stu-id="e5912-118">**String**</span></span> <br/> | <span data-ttu-id="e5912-119">Die Liste, in der gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="e5912-119">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="e5912-120">_delimiter_</span><span class="sxs-lookup"><span data-stu-id="e5912-120">_delimiter_</span></span> <br/> |<span data-ttu-id="e5912-121">Optional</span><span class="sxs-lookup"><span data-stu-id="e5912-121">Optional</span></span>  <br/> |<span data-ttu-id="e5912-122">**String**</span><span class="sxs-lookup"><span data-stu-id="e5912-122">**String**</span></span> <br/> | <span data-ttu-id="e5912-123">Die Zeichenfolge an, in der _Liste_als Trennzeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e5912-123">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="e5912-124">Zeichenfolge für ein _Trennzeichen_ kann mehr als ein Zeichen lang sein und kann multibyte-Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="e5912-124">A  _delimiter_ string can be more than one character in length and may include multibyte characters.</span></span> <span data-ttu-id="e5912-125">Der Standardwert ist eine durch Semikolons.</span><span class="sxs-lookup"><span data-stu-id="e5912-125">The default is a semicolon.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e5912-126">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="e5912-126">Return value</span></span>

<span data-ttu-id="e5912-127">Numeric</span><span class="sxs-lookup"><span data-stu-id="e5912-127">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e5912-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5912-128">Remarks</span></span>

<span data-ttu-id="e5912-p102">Die LOOKUP-Funktion verwendet eine Suche, die nicht zwischen Klein- und Großschreibung unterscheidet. Ist der Liste ein Trennzeichen voran- bzw. nachgestellt, wird eine leere Zeichenfolge vor bzw. hinter der Liste unterstellt. Aufeinander folgende Trennzeichen implizieren eine eingefügte leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e5912-p102">The LOOKUP function uses a case-insensitive search. If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list. Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="e5912-p103">Sämtliche Argumente müssen Zeichenfolgen oder in Zeichenfolgen konvertierbare Ausdrücke sein. Ist dies nicht der Fall, wird eine leere Zeichenfolge für das fehlerhafte Argument verwendet.</span><span class="sxs-lookup"><span data-stu-id="e5912-p103">All the arguments must be strings or expressions that can be converted to strings. If they are not, an empty string is substituted for the offending argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="e5912-134">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e5912-134">Example 1</span></span>

<span data-ttu-id="e5912-135">LOOKUP("Ratte","Katze;Ratte;;Ziege")</span><span class="sxs-lookup"><span data-stu-id="e5912-135">LOOKUP("rat","cat;rat;;goat")</span></span>
  
<span data-ttu-id="e5912-136">Gibt 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="e5912-136">Returns 1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e5912-137">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e5912-137">Example 2</span></span>

<span data-ttu-id="e5912-138">LOOKUP("",";Katze;Ratte;;Ziege")</span><span class="sxs-lookup"><span data-stu-id="e5912-138">LOOKUP("",";cat;rat;;goat")</span></span>
  
<span data-ttu-id="e5912-139">Gibt 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="e5912-139">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="e5912-140">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e5912-140">Example 3</span></span>

<span data-ttu-id="e5912-141">LOOKUP("t","Katze;Ratte;;Ziege","a")</span><span class="sxs-lookup"><span data-stu-id="e5912-141">LOOKUP("t","cat;rat;;goat","a")</span></span>
  
<span data-ttu-id="e5912-142">Gibt 3 zurück.</span><span class="sxs-lookup"><span data-stu-id="e5912-142">Returns 3.</span></span>
  

