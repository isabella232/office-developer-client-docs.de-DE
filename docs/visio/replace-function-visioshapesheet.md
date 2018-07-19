---
title: REPLACE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60108
localization_priority: Normal
ms.assetid: 70c9fc1d-6e7b-479f-effd-0d4bc8ae0f72
description: Ersetzt auf der Grundlage der angegebenen Anzahl von Zeichen einen Teil einer Zeichenfolge durch eine andere Zeichenfolge.
ms.openlocfilehash: 4112339d772248ac033674808d97c3f9c55b6f0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797815"
---
# <a name="replace-function-visioshapesheet"></a><span data-ttu-id="64121-103">REPLACE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="64121-103">REPLACE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="64121-104">Ersetzt auf der Grundlage der angegebenen Anzahl von Zeichen einen Teil einer Zeichenfolge durch eine andere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="64121-104">Replaces part of a text string, based on the number of characters you specify, with a different text string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="64121-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="64121-105">Syntax</span></span>

<span data-ttu-id="64121-106">Ersetzen Sie (** *Alter_Text* **, ** *Erstes_Zeichen* **, ** *Num_chars* **, ** *Neuer_Text* **)</span><span class="sxs-lookup"><span data-stu-id="64121-106">REPLACE (** *old_text* **, ** *start_num* **, ** *num_chars* **, ** *new_text* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="64121-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="64121-107">Parameters</span></span>

|<span data-ttu-id="64121-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="64121-108">**Name**</span></span>|<span data-ttu-id="64121-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="64121-109">**Required/Optional**</span></span>|<span data-ttu-id="64121-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="64121-110">**Data Type**</span></span>|<span data-ttu-id="64121-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="64121-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="64121-112">_Alter_Text_</span><span class="sxs-lookup"><span data-stu-id="64121-112">_old_text_</span></span> <br/> |<span data-ttu-id="64121-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="64121-113">Required</span></span>  <br/> |<span data-ttu-id="64121-114">**String**</span><span class="sxs-lookup"><span data-stu-id="64121-114">**String**</span></span> <br/> |<span data-ttu-id="64121-115">Der Text, in dem einige Zeichen ersetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64121-115">The text in which you want to replace some characters.</span></span>  <br/> |
| <span data-ttu-id="64121-116">_Erstes_Zeichen_</span><span class="sxs-lookup"><span data-stu-id="64121-116">_start_num_</span></span> <br/> |<span data-ttu-id="64121-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="64121-117">Required</span></span>  <br/> |<span data-ttu-id="64121-118">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="64121-118">**Number**</span></span> <br/> |<span data-ttu-id="64121-119">Die Position des Zeichens in _Alter_Text_ , den Sie durch _Neuer_Text_ersetzen möchten.</span><span class="sxs-lookup"><span data-stu-id="64121-119">The position of the character in  _old_text_ that you want to replace with  _new_text_.</span></span> <span data-ttu-id="64121-120">Das erste Zeichen in der Zeichenfolge ist Position 1.</span><span class="sxs-lookup"><span data-stu-id="64121-120">The first character in the string is position 1.</span></span>  <br/> |
| <span data-ttu-id="64121-121">_Anzahl_Zeichen_</span><span class="sxs-lookup"><span data-stu-id="64121-121">_num_chars_</span></span> <br/> |<span data-ttu-id="64121-122">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="64121-122">Required</span></span>  <br/> |<span data-ttu-id="64121-123">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="64121-123">**Number**</span></span> <br/> |<span data-ttu-id="64121-124">Die Anzahl der Zeichen in _Old_text_ , die Sie ersetzen möchten.</span><span class="sxs-lookup"><span data-stu-id="64121-124">The number of characters in  _old_text_ that you want to replace</span></span>  <br/> |
| <span data-ttu-id="64121-125">_Neuer_Text_</span><span class="sxs-lookup"><span data-stu-id="64121-125">_new_text_</span></span> <br/> |<span data-ttu-id="64121-126">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="64121-126">Required</span></span>  <br/> |<span data-ttu-id="64121-127">**String**</span><span class="sxs-lookup"><span data-stu-id="64121-127">**String**</span></span> <br/> |<span data-ttu-id="64121-128">Der Text, der Zeichen in _Old_text_ersetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="64121-128">The text that will replace characters in  _old_text_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="64121-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64121-129">Return value</span></span>

<span data-ttu-id="64121-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="64121-130">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="64121-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64121-131">Remarks</span></span>

<span data-ttu-id="64121-p102">Verwenden Sie die Funktion REPLACE, wenn Sie Text ersetzen möchten, der an einer bestimmten Stelle in der Zeichenfolge auftritt. Wenn Sie bestimmten Text in einer Zeichenkette ersetzen möchten, verwenden Sie die Funktion SUBSTITUTE.</span><span class="sxs-lookup"><span data-stu-id="64121-p102">Use the REPLACE function when you want to replace text that occurs in a specific location in a text string. If you want to replace specific text in a text string, use the SUBSTITUTE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="64121-134">Beispiel</span><span class="sxs-lookup"><span data-stu-id="64121-134">Example</span></span>

<span data-ttu-id="64121-135">REPLACE ("01/03/2002",9,2,"03")</span><span class="sxs-lookup"><span data-stu-id="64121-135">REPLACE ("01/03/2002",9,2,"03")</span></span> 
  
<span data-ttu-id="64121-136">Gibt 01/03/2003 zurück.</span><span class="sxs-lookup"><span data-stu-id="64121-136">Returns 01/03/2003.</span></span> 
  

