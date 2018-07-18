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
description: Gibt die Teilzeichenfolge am Index nullbasierte Position in der durch Trennzeichen getrennten Liste zurück. Oder, wenn der Index außerhalb des gültigen Bereichs, gibt eine leere Zeichenfolge oder das optionale als Argument für Errorvalue bereitgestellt.
ms.openlocfilehash: b801f3b2a762f7767f32953806178be3eb264398
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797198"
---
# <a name="index-function"></a><span data-ttu-id="dd5ce-104">INDEX Function</span><span class="sxs-lookup"><span data-stu-id="dd5ce-104">INDEX Function</span></span>

<span data-ttu-id="dd5ce-105">Gibt die Teilzeichenfolge am Speicherort der nullbasierte _Index_ in der durch _Trennzeichen_getrennten _Liste_ zurück.</span><span class="sxs-lookup"><span data-stu-id="dd5ce-105">Returns the substring at the zero-based location  _index_ in the  _list_ delimited by  _delimiter_.</span></span> <span data-ttu-id="dd5ce-106">Oder, wenn der Index außerhalb des gültigen Bereichs, gibt eine leere Zeichenfolge oder das optionale als Argument für *Errorvalue* bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="dd5ce-106">Or, if the index is out of range, returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="dd5ce-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd5ce-107">Syntax</span></span>

<span data-ttu-id="dd5ce-108">INDEX (** *Index* **, "** *Liste* **" [, [** *Trennzeichen* **] [, [** *Errorvalue* **]]])</span><span class="sxs-lookup"><span data-stu-id="dd5ce-108">INDEX(** *index* **," ** *list* ** "[,[ ** *delimiter* ** ][,[ ** *errorvalue* ** ]]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dd5ce-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd5ce-109">Parameters</span></span>

|<span data-ttu-id="dd5ce-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="dd5ce-110">**Name**</span></span>|<span data-ttu-id="dd5ce-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="dd5ce-111">**Required/Optional**</span></span>|<span data-ttu-id="dd5ce-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="dd5ce-112">**Data Type**</span></span>|<span data-ttu-id="dd5ce-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dd5ce-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dd5ce-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="dd5ce-114">_index_</span></span> <br/> |<span data-ttu-id="dd5ce-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dd5ce-115">Required</span></span>  <br/> |<span data-ttu-id="dd5ce-116">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="dd5ce-116">**Number**</span></span> <br/> |<span data-ttu-id="dd5ce-117">Die Position, die gefunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd5ce-117">The location that you want to find.</span></span>  <br/> |
| <span data-ttu-id="dd5ce-118">_list_</span><span class="sxs-lookup"><span data-stu-id="dd5ce-118">_list_</span></span> <br/> |<span data-ttu-id="dd5ce-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dd5ce-119">Required</span></span>  <br/> |<span data-ttu-id="dd5ce-120">**String**</span><span class="sxs-lookup"><span data-stu-id="dd5ce-120">**String**</span></span> <br/> |<span data-ttu-id="dd5ce-121">Die Liste, in der gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd5ce-121">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="dd5ce-122">_delimiter_</span><span class="sxs-lookup"><span data-stu-id="dd5ce-122">_delimiter_</span></span> <br/> |<span data-ttu-id="dd5ce-123">Optional</span><span class="sxs-lookup"><span data-stu-id="dd5ce-123">Optional</span></span>  <br/> |<span data-ttu-id="dd5ce-124">**String**</span><span class="sxs-lookup"><span data-stu-id="dd5ce-124">**String**</span></span> <br/> | <span data-ttu-id="dd5ce-125">Die Zeichenfolge an, in der _Liste_als Trennzeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="dd5ce-125">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="dd5ce-126">Zeichenfolge für ein _Trennzeichen_ kann mehrere Zeichen lang sein und multibyte-Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="dd5ce-126">A  _delimiter_ string can be more than one character in length and include multibyte characters.</span></span> <span data-ttu-id="dd5ce-127">Der Standardwert ist eine durch Semikolons.</span><span class="sxs-lookup"><span data-stu-id="dd5ce-127">The default is a semicolon.</span></span>  <br/> |
| <span data-ttu-id="dd5ce-128">_Fehlerwert_</span><span class="sxs-lookup"><span data-stu-id="dd5ce-128">_errorvalue_</span></span> <br/> |<span data-ttu-id="dd5ce-129">Optional</span><span class="sxs-lookup"><span data-stu-id="dd5ce-129">Optional</span></span>  <br/> |<span data-ttu-id="dd5ce-130">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="dd5ce-130">**Number**</span></span> <br/> | <span data-ttu-id="dd5ce-p104">Ein benutzerdefinierter Wert, der zurückgegeben wird, wenn sich der Index außerhalb des gültigen Bereichs befindet. Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="dd5ce-p104">A user-specified value to return if the index is out of range. The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd5ce-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd5ce-133">Remarks</span></span>

<span data-ttu-id="dd5ce-p105">Ist der Liste ein Trennzeichen voran- bzw. nachgestellt, wird eine leere Zeichenfolge vor bzw. hinter der Liste unterstellt. Aufeinander folgende Trennzeichen implizieren eine eingefügte leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="dd5ce-p105">If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list. Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="dd5ce-136">Wenn der Index außerhalb des gültigen Bereichs befindet, gibt Visio eine leere Zeichenfolge oder das optionale als Argument für *Errorvalue* bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="dd5ce-136">If the index is out of range, Visio returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="dd5ce-137">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dd5ce-137">Example 1</span></span>

<span data-ttu-id="dd5ce-138">INDEX(3,"Katze;Ratte;;Ziege")</span><span class="sxs-lookup"><span data-stu-id="dd5ce-138">INDEX(3,"cat;rat;;goat")</span></span>
  
<span data-ttu-id="dd5ce-139">Gibt "Ziege" zurück.</span><span class="sxs-lookup"><span data-stu-id="dd5ce-139">Returns "goat".</span></span>
  
## <a name="example-2"></a><span data-ttu-id="dd5ce-140">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="dd5ce-140">Example 2</span></span>

<span data-ttu-id="dd5ce-141">INDEX(54,";1;2;3;",,"FEHLER")</span><span class="sxs-lookup"><span data-stu-id="dd5ce-141">INDEX(54,";1;2;3;",,"ERROR")</span></span>
  
<span data-ttu-id="dd5ce-142">Gibt "Fehler".</span><span class="sxs-lookup"><span data-stu-id="dd5ce-142">Returns "ERROR".</span></span>
  

