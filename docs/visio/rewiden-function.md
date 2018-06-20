---
title: REWIDEN-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033808
localization_priority: Normal
ms.assetid: c20842cd-86b1-83fa-49ba-118936013b6f
description: Konvertiert eine Formel, die 16-Bit-Zeichencodes, die erweiterte Einzel-Byte oder multibyte-Zeichensatz Codes in eine Zeichenfolge von 16-Bit-Unicode-Zeichencodes erzeugt, mithilfe der angegebenen Zeichensätze aufweisen.
ms.openlocfilehash: 66dc3e801585077a9521cd93f8ae78c47f8a746b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797862"
---
# <a name="rewiden-function"></a><span data-ttu-id="71ed2-103">REWIDEN-Funktion</span><span class="sxs-lookup"><span data-stu-id="71ed2-103">REWIDEN Function</span></span>

<span data-ttu-id="71ed2-104">Konvertiert eine Formel, die 16-Bit-Zeichencodes, die erweiterte Einzel-Byte oder multibyte-Zeichensatz Codes in eine Zeichenfolge von 16-Bit-Unicode-Zeichencodes erzeugt, mithilfe der angegebenen Zeichensätze aufweisen.</span><span class="sxs-lookup"><span data-stu-id="71ed2-104">Converts a formula that produces 16-bit character codes that are widened single-byte or multibyte character-set codes into a string of 16-bit Unicode character codes, using the specified character sets.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="71ed2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="71ed2-105">Syntax</span></span>

<span data-ttu-id="71ed2-106">REWIDEN (** *SrcCharSet* **, ** *DstCharSet* **, ** *Text* **)</span><span class="sxs-lookup"><span data-stu-id="71ed2-106">REWIDEN(** *srcCharSet* **, ** *dstCharSet* **, ** *text* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="71ed2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="71ed2-107">Parameters</span></span>

|<span data-ttu-id="71ed2-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="71ed2-108">**Name**</span></span>|<span data-ttu-id="71ed2-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="71ed2-109">**Required/Optional**</span></span>|<span data-ttu-id="71ed2-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="71ed2-110">**Data Type**</span></span>|<span data-ttu-id="71ed2-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="71ed2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="71ed2-112">_srcCharSet_</span><span class="sxs-lookup"><span data-stu-id="71ed2-112">_srcCharSet_</span></span> <br/> |<span data-ttu-id="71ed2-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="71ed2-113">Required</span></span>  <br/> |<span data-ttu-id="71ed2-114">**String**</span><span class="sxs-lookup"><span data-stu-id="71ed2-114">**String**</span></span> <br/> |<span data-ttu-id="71ed2-115">Der Zeichensatz im Quelldokument.</span><span class="sxs-lookup"><span data-stu-id="71ed2-115">The character set in the source document.</span></span>  <br/> |
| <span data-ttu-id="71ed2-116">_dstCharSet_</span><span class="sxs-lookup"><span data-stu-id="71ed2-116">_dstCharSet_</span></span> <br/> |<span data-ttu-id="71ed2-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="71ed2-117">Required</span></span>  <br/> |<span data-ttu-id="71ed2-118">**String**</span><span class="sxs-lookup"><span data-stu-id="71ed2-118">**String**</span></span> <br/> | <span data-ttu-id="71ed2-119">Der Zeichensatz im Zieldokument.</span><span class="sxs-lookup"><span data-stu-id="71ed2-119">The character set in the destination document.</span></span>  <br/> |
| <span data-ttu-id="71ed2-120">_text_</span><span class="sxs-lookup"><span data-stu-id="71ed2-120">_text_</span></span> <br/> |<span data-ttu-id="71ed2-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="71ed2-121">Required</span></span>  <br/> |<span data-ttu-id="71ed2-122">**String**</span><span class="sxs-lookup"><span data-stu-id="71ed2-122">**String**</span></span> <br/> |<span data-ttu-id="71ed2-123">Der zu konvertierende Text.</span><span class="sxs-lookup"><span data-stu-id="71ed2-123">The text to convert.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71ed2-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="71ed2-124">Remarks</span></span>

<span data-ttu-id="71ed2-p101">Die REWIDEN-Funktion wird zur automatischen Konvertierung von Visio 2002-Dokumenten in Visio 2003-Dokumente verwendet. Eine andere Verwendung wird nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="71ed2-p101">The REWIDEN function is used in automatic conversion of Visio 2002 documents to Visio 2003 documents. Other use is not recommended.</span></span>
  

