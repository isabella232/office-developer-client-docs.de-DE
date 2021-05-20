---
title: INDEX-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251443
localization_priority: Normal
ms.assetid: cc46f91e-733f-e25a-17d2-19df8c8febd2
description: Gibt die Teilzeichenfolge am nullbasierten Standortindex in der Durch Trennzeichen getrennten Liste zurück. Wenn sich der Index nicht im Bereich befindet, wird auch eine leere Zeichenfolge oder das optionale Token zurückgegeben, das als Argument errorvalue angegeben wird.
ms.openlocfilehash: 11362ed984a489682d57f007300e60de548ddf11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431575"
---
# <a name="index-function"></a><span data-ttu-id="ddda2-104">INDEX Function</span><span class="sxs-lookup"><span data-stu-id="ddda2-104">INDEX Function</span></span>

<span data-ttu-id="ddda2-105">Gibt die Teilzeichenfolge am nullbasierten _Standortindex_ in der durch Trennzeichen getrennten Liste _zurück._ </span><span class="sxs-lookup"><span data-stu-id="ddda2-105">Returns the substring at the zero-based location  _index_ in the  _list_ delimited by  _delimiter_.</span></span> <span data-ttu-id="ddda2-106">Wenn sich der Index nicht im Bereich befindet, wird auch eine leere Zeichenfolge oder das optionale Token zurückgegeben, das als  *Argument errorvalue angegeben*  wird.</span><span class="sxs-lookup"><span data-stu-id="ddda2-106">Or, if the index is out of range, returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ddda2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddda2-107">Syntax</span></span>

<span data-ttu-id="ddda2-108">INDEX(\*\* *index* \*\*," \*\* *list* \*\* "[,[ \*\* *delimiter* \*\* ][,[ \*\* *errorvalue* \*\* ]]])</span><span class="sxs-lookup"><span data-stu-id="ddda2-108">INDEX(\*\* *index* \*\*," \*\* *list* \*\* "[,[ \*\* *delimiter* \*\* ][,[ \*\* *errorvalue* \*\* ]]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ddda2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ddda2-109">Parameters</span></span>

|<span data-ttu-id="ddda2-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="ddda2-110">**Name**</span></span>|<span data-ttu-id="ddda2-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="ddda2-111">**Required/Optional**</span></span>|<span data-ttu-id="ddda2-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="ddda2-112">**Data Type**</span></span>|<span data-ttu-id="ddda2-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ddda2-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ddda2-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="ddda2-114">_index_</span></span> <br/> |<span data-ttu-id="ddda2-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ddda2-115">Required</span></span>  <br/> |<span data-ttu-id="ddda2-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="ddda2-116">**Number**</span></span> <br/> |<span data-ttu-id="ddda2-117">Die Position, die gefunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="ddda2-117">The location that you want to find.</span></span>  <br/> |
| <span data-ttu-id="ddda2-118">_list_</span><span class="sxs-lookup"><span data-stu-id="ddda2-118">_list_</span></span> <br/> |<span data-ttu-id="ddda2-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="ddda2-119">Required</span></span>  <br/> |<span data-ttu-id="ddda2-120">**String**</span><span class="sxs-lookup"><span data-stu-id="ddda2-120">**String**</span></span> <br/> |<span data-ttu-id="ddda2-121">Die Liste, in der gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="ddda2-121">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="ddda2-122">_delimiter_</span><span class="sxs-lookup"><span data-stu-id="ddda2-122">_delimiter_</span></span> <br/> |<span data-ttu-id="ddda2-123">Optional</span><span class="sxs-lookup"><span data-stu-id="ddda2-123">Optional</span></span>  <br/> |<span data-ttu-id="ddda2-124">**String**</span><span class="sxs-lookup"><span data-stu-id="ddda2-124">**String**</span></span> <br/> | <span data-ttu-id="ddda2-125">Die Zeichenfolge, die als Trennzeichen in der Liste verwendet _werden soll._</span><span class="sxs-lookup"><span data-stu-id="ddda2-125">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="ddda2-126">Eine  _Trennzeichenzeichenfolge_ kann mehr als ein Zeichen lang sein und Mehrbytezeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="ddda2-126">A  _delimiter_ string can be more than one character in length and include multibyte characters.</span></span> <span data-ttu-id="ddda2-127">Das Standardtrennzeichen ist ein Semikolon.</span><span class="sxs-lookup"><span data-stu-id="ddda2-127">The default is a semicolon.</span></span>  <br/> |
| <span data-ttu-id="ddda2-128">_errorvalue_</span><span class="sxs-lookup"><span data-stu-id="ddda2-128">_errorvalue_</span></span> <br/> |<span data-ttu-id="ddda2-129">Optional.</span><span class="sxs-lookup"><span data-stu-id="ddda2-129">Optional</span></span>  <br/> |<span data-ttu-id="ddda2-130">**Number**</span><span class="sxs-lookup"><span data-stu-id="ddda2-130">**Number**</span></span> <br/> | <span data-ttu-id="ddda2-p104">Ein benutzerdefinierter Wert, der zurückgegeben wird, wenn sich der Index außerhalb des gültigen Bereichs befindet. Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ddda2-p104">A user-specified value to return if the index is out of range. The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ddda2-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ddda2-133">Remarks</span></span>

<span data-ttu-id="ddda2-p105">Ist der Liste ein Trennzeichen voran- bzw. nachgestellt, wird eine leere Zeichenfolge vor bzw. hinter der Liste unterstellt. Aufeinander folgende Trennzeichen implizieren eine eingefügte leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ddda2-p105">If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list. Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="ddda2-136">Liegt der Index nicht im Bereich, gibt Visio eine leere Zeichenfolge oder das optionale Token zurück, das als *Argument errorvalue bereitgestellt* wird.</span><span class="sxs-lookup"><span data-stu-id="ddda2-136">If the index is out of range, Visio returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="ddda2-137">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ddda2-137">Example 1</span></span>

<span data-ttu-id="ddda2-138">INDEX(3,"cat;rat;; Ziege")</span><span class="sxs-lookup"><span data-stu-id="ddda2-138">INDEX(3,"cat;rat;;goat")</span></span>
  
<span data-ttu-id="ddda2-139">Gibt "Ziege" zurück.</span><span class="sxs-lookup"><span data-stu-id="ddda2-139">Returns "goat".</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ddda2-140">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ddda2-140">Example 2</span></span>

<span data-ttu-id="ddda2-141">INDEX(54,";1;2;3;",,"ERROR")</span><span class="sxs-lookup"><span data-stu-id="ddda2-141">INDEX(54,";1;2;3;",,"ERROR")</span></span>
  
<span data-ttu-id="ddda2-142">Gibt "ERROR" zurück.</span><span class="sxs-lookup"><span data-stu-id="ddda2-142">Returns "ERROR".</span></span>
  

