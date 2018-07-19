---
title: LEFT Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1021757
localization_priority: Normal
ms.assetid: 0c2f6e06-b772-2006-ec7b-8695d097f146
description: Gibt das am weitesten links oder die Zeichen in einer Textzeichenfolge, basierend auf der Anzahl der Zeichen an, die Sie angeben.
ms.openlocfilehash: 4e8deb3098ce6d217dcce0cae23d07ed723d9fb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797309"
---
# <a name="left-function-visioshapesheet"></a><span data-ttu-id="8c013-103">LEFT Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="8c013-103">LEFT Function (VisioShapeSheet)</span></span>

<span data-ttu-id="8c013-104">Gibt das am weitesten links oder die Zeichen in einer Textzeichenfolge, basierend auf der Anzahl der Zeichen an, die Sie angeben.</span><span class="sxs-lookup"><span data-stu-id="8c013-104">Returns the left-most character or characters in a text string, based on the number of characters you specify.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8c013-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c013-105">Syntax</span></span>

<span data-ttu-id="8c013-106">Links (** *Text* **, [, ** *Num_chars_opt* **])</span><span class="sxs-lookup"><span data-stu-id="8c013-106">LEFT(** *text* **, [, ** *num_chars_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8c013-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c013-107">Parameters</span></span>

|<span data-ttu-id="8c013-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="8c013-108">**Name**</span></span>|<span data-ttu-id="8c013-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="8c013-109">**Required/Optional**</span></span>|<span data-ttu-id="8c013-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="8c013-110">**Data Type**</span></span>|<span data-ttu-id="8c013-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8c013-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8c013-112">_text_</span><span class="sxs-lookup"><span data-stu-id="8c013-112">_text_</span></span> <br/> |<span data-ttu-id="8c013-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8c013-113">Required</span></span>  <br/> |<span data-ttu-id="8c013-114">**String**</span><span class="sxs-lookup"><span data-stu-id="8c013-114">**String**</span></span> <br/> |<span data-ttu-id="8c013-115">Die Zeichenfolge mit den zu extrahierenden Zeichen.</span><span class="sxs-lookup"><span data-stu-id="8c013-115">The text string that contains the characters you want to extract.</span></span>  <br/> |
| <span data-ttu-id="8c013-116">_num_chars_opt_</span><span class="sxs-lookup"><span data-stu-id="8c013-116">_num_chars_opt_</span></span> <br/> |<span data-ttu-id="8c013-117">Optional</span><span class="sxs-lookup"><span data-stu-id="8c013-117">Optional</span></span>  <br/> |<span data-ttu-id="8c013-118">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="8c013-118">**Numeric**</span></span> <br/> |<span data-ttu-id="8c013-119">Die Anzahl der Zeichen, die extrahiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8c013-119">The number of characters you want to extract.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8c013-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c013-120">Return value</span></span>

<span data-ttu-id="8c013-121">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="8c013-121">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8c013-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c013-122">Remarks</span></span>

<span data-ttu-id="8c013-123">Der Wert von _Num_chars_opt_ muss größer als oder gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="8c013-123">The value of  _num_chars_opt_ must be greater than or equal to zero (0).</span></span> 
  
<span data-ttu-id="8c013-124">Wenn _Num_chars_opt_ größer als die Länge des Texts ist, gibt links des gesamten Texts.</span><span class="sxs-lookup"><span data-stu-id="8c013-124">If  _num_chars_opt_ is greater than the length of the text, LEFT returns all of the text.</span></span> <span data-ttu-id="8c013-125">Wenn _Num_chars_opt_ ausgelassen wird, wird angenommen, 1 sein.</span><span class="sxs-lookup"><span data-stu-id="8c013-125">If  _num_chars_opt_ is omitted, it is assumed to be 1.</span></span> 
  
## <a name="example"></a><span data-ttu-id="8c013-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8c013-126">Example</span></span>

<span data-ttu-id="8c013-127">LEFT ("Januar 1, 2004", 3)</span><span class="sxs-lookup"><span data-stu-id="8c013-127">LEFT ("January 1, 2004", 3)</span></span> 
  
<span data-ttu-id="8c013-128">Ergibt den Wert Jan.</span><span class="sxs-lookup"><span data-stu-id="8c013-128">Returns the value "Jan".</span></span> 
  

