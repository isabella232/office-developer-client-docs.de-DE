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
description: Gibt einen nullbasierten Index zurück, der die Position des Schlüssels der Teilzeichenfolge in einer Liste angibt, oder gibt-1 zurück, wenn die Zielzeichenfolge das Trennzeichen enthält.
ms.openlocfilehash: 10fc32e6e979ab819246161dedfb1183c2683a99
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410329"
---
# <a name="lookup-function"></a><span data-ttu-id="8a4b6-103">LOOKUP Function</span><span class="sxs-lookup"><span data-stu-id="8a4b6-103">LOOKUP Function</span></span>

<span data-ttu-id="8a4b6-104">Gibt einen nullbasierten Index zurück, der die Position des _Schlüssels_ der Teilzeichenfolge in einer _Liste_angibt, oder gibt-1 zurück, wenn die Zielzeichenfolge das _Trenn_Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="8a4b6-104">Returns a zero-based index that indicates the location of the substring  _key_ in a  _list_, or returns -1 if the target string contains the  _delimiter_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8a4b6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a4b6-105">Syntax</span></span>

<span data-ttu-id="8a4b6-106">Lookup ("\* \* *Key* \* *", "* \* *Liste* \* *" [, "* \* *Trennzeichen* \* \*"])</span><span class="sxs-lookup"><span data-stu-id="8a4b6-106">LOOKUP(" \*\* *key* \*\* "," \*\* *list* \*\* "[," \*\* *delimiter* \*\* "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8a4b6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a4b6-107">Parameters</span></span>

|<span data-ttu-id="8a4b6-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="8a4b6-108">**Name**</span></span>|<span data-ttu-id="8a4b6-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="8a4b6-109">**Required/Optional**</span></span>|<span data-ttu-id="8a4b6-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="8a4b6-110">**Data Type**</span></span>|<span data-ttu-id="8a4b6-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8a4b6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8a4b6-112">_key_</span><span class="sxs-lookup"><span data-stu-id="8a4b6-112">_key_</span></span> <br/> |<span data-ttu-id="8a4b6-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8a4b6-113">Required</span></span>  <br/> |<span data-ttu-id="8a4b6-114">**String**</span><span class="sxs-lookup"><span data-stu-id="8a4b6-114">**String**</span></span> <br/> |<span data-ttu-id="8a4b6-115">Die zu suchende Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="8a4b6-115">The string that you want to look up.</span></span>  <br/> |
| <span data-ttu-id="8a4b6-116">_list_</span><span class="sxs-lookup"><span data-stu-id="8a4b6-116">_list_</span></span> <br/> |<span data-ttu-id="8a4b6-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8a4b6-117">Required</span></span>  <br/> |<span data-ttu-id="8a4b6-118">**String**</span><span class="sxs-lookup"><span data-stu-id="8a4b6-118">**String**</span></span> <br/> | <span data-ttu-id="8a4b6-119">Die Liste, in der gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a4b6-119">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="8a4b6-120">_delimiter_</span><span class="sxs-lookup"><span data-stu-id="8a4b6-120">_delimiter_</span></span> <br/> |<span data-ttu-id="8a4b6-121">Optional</span><span class="sxs-lookup"><span data-stu-id="8a4b6-121">Optional</span></span>  <br/> |<span data-ttu-id="8a4b6-122">**String**</span><span class="sxs-lookup"><span data-stu-id="8a4b6-122">**String**</span></span> <br/> | <span data-ttu-id="8a4b6-123">Die zu verwendende Zeichenfolge in _List_.</span><span class="sxs-lookup"><span data-stu-id="8a4b6-123">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="8a4b6-124">Eine _Trenn_ Zeichen Zeichenfolge kann mehr als ein Zeichen lang sein und Multibyte-Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="8a4b6-124">A  _delimiter_ string can be more than one character in length and may include multibyte characters.</span></span> <span data-ttu-id="8a4b6-125">Das Standardtrennzeichen ist ein Semikolon.</span><span class="sxs-lookup"><span data-stu-id="8a4b6-125">The default is a semicolon.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8a4b6-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a4b6-126">Return value</span></span>

<span data-ttu-id="8a4b6-127">Numeric</span><span class="sxs-lookup"><span data-stu-id="8a4b6-127">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8a4b6-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a4b6-128">Remarks</span></span>

<span data-ttu-id="8a4b6-p102">Die LOOKUP-Funktion verwendet eine Suche, die nicht zwischen Klein- und Großschreibung unterscheidet. Ist der Liste ein Trennzeichen voran- bzw. nachgestellt, wird eine leere Zeichenfolge vor bzw. hinter der Liste unterstellt. Aufeinander folgende Trennzeichen implizieren eine eingefügte leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="8a4b6-p102">The LOOKUP function uses a case-insensitive search. If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list. Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="8a4b6-p103">Sämtliche Argumente müssen Zeichenfolgen oder in Zeichenfolgen konvertierbare Ausdrücke sein. Ist dies nicht der Fall, wird eine leere Zeichenfolge für das fehlerhafte Argument verwendet.</span><span class="sxs-lookup"><span data-stu-id="8a4b6-p103">All the arguments must be strings or expressions that can be converted to strings. If they are not, an empty string is substituted for the offending argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="8a4b6-134">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8a4b6-134">Example 1</span></span>

<span data-ttu-id="8a4b6-135">LOOKUP ("Rat", "Cat; Rat;; Ziege ")</span><span class="sxs-lookup"><span data-stu-id="8a4b6-135">LOOKUP("rat","cat;rat;;goat")</span></span>
  
<span data-ttu-id="8a4b6-136">Gibt 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="8a4b6-136">Returns 1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="8a4b6-137">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8a4b6-137">Example 2</span></span>

<span data-ttu-id="8a4b6-138">LOOKUP ("", "; Cat; Rat;; Ziege ")</span><span class="sxs-lookup"><span data-stu-id="8a4b6-138">LOOKUP("",";cat;rat;;goat")</span></span>
  
<span data-ttu-id="8a4b6-139">Gibt 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="8a4b6-139">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="8a4b6-140">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="8a4b6-140">Example 3</span></span>

<span data-ttu-id="8a4b6-141">LOOKUP ("t", "Cat; Rat;; Ziege "," a ")</span><span class="sxs-lookup"><span data-stu-id="8a4b6-141">LOOKUP("t","cat;rat;;goat","a")</span></span>
  
<span data-ttu-id="8a4b6-142">Gibt 3 zurück.</span><span class="sxs-lookup"><span data-stu-id="8a4b6-142">Returns 3.</span></span>
  

