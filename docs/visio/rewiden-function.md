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
description: Wandelt eine Formel, die 16-Bit-Zeichencodes erzeugt, die mit einem Byte oder einem Mehrbyte-Zeichensatz in eine Zeichenfolge mit 16-Bit-Unicode-Zeichencodes mit den angegebenen Zeichensätzen verbreitet werden.
ms.openlocfilehash: c885487f91e541027b7ba09812e7321a9deb00ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405212"
---
# <a name="rewiden-function"></a><span data-ttu-id="f5dee-103">REWIDEN Function</span><span class="sxs-lookup"><span data-stu-id="f5dee-103">REWIDEN Function</span></span>

<span data-ttu-id="f5dee-104">Wandelt eine Formel, die 16-Bit-Zeichencodes erzeugt, die mit einem Byte oder einem Mehrbyte-Zeichensatz in eine Zeichenfolge mit 16-Bit-Unicode-Zeichencodes mit den angegebenen Zeichensätzen verbreitet werden.</span><span class="sxs-lookup"><span data-stu-id="f5dee-104">Converts a formula that produces 16-bit character codes that are widened single-byte or multibyte character-set codes into a string of 16-bit Unicode character codes, using the specified character sets.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f5dee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5dee-105">Syntax</span></span>

<span data-ttu-id="f5dee-106">REWIDEN(\*\* *srcCharSet* \*\*, \*\* *dstCharSet* \*\*, \*\* *text* \*\* )</span><span class="sxs-lookup"><span data-stu-id="f5dee-106">REWIDEN(\*\* *srcCharSet* \*\*, \*\* *dstCharSet* \*\*, \*\* *text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f5dee-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5dee-107">Parameters</span></span>

|<span data-ttu-id="f5dee-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="f5dee-108">**Name**</span></span>|<span data-ttu-id="f5dee-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="f5dee-109">**Required/Optional**</span></span>|<span data-ttu-id="f5dee-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="f5dee-110">**Data Type**</span></span>|<span data-ttu-id="f5dee-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f5dee-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f5dee-112">_srcCharSet_</span><span class="sxs-lookup"><span data-stu-id="f5dee-112">_srcCharSet_</span></span> <br/> |<span data-ttu-id="f5dee-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f5dee-113">Required</span></span>  <br/> |<span data-ttu-id="f5dee-114">**String**</span><span class="sxs-lookup"><span data-stu-id="f5dee-114">**String**</span></span> <br/> |<span data-ttu-id="f5dee-115">Der Zeichensatz im Quelldokument.</span><span class="sxs-lookup"><span data-stu-id="f5dee-115">The character set in the source document.</span></span>  <br/> |
| <span data-ttu-id="f5dee-116">_dstCharSet_</span><span class="sxs-lookup"><span data-stu-id="f5dee-116">_dstCharSet_</span></span> <br/> |<span data-ttu-id="f5dee-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f5dee-117">Required</span></span>  <br/> |<span data-ttu-id="f5dee-118">**String**</span><span class="sxs-lookup"><span data-stu-id="f5dee-118">**String**</span></span> <br/> | <span data-ttu-id="f5dee-119">Der Zeichensatz im Zieldokument.</span><span class="sxs-lookup"><span data-stu-id="f5dee-119">The character set in the destination document.</span></span>  <br/> |
| <span data-ttu-id="f5dee-120">_text_</span><span class="sxs-lookup"><span data-stu-id="f5dee-120">_text_</span></span> <br/> |<span data-ttu-id="f5dee-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f5dee-121">Required</span></span>  <br/> |<span data-ttu-id="f5dee-122">**String**</span><span class="sxs-lookup"><span data-stu-id="f5dee-122">**String**</span></span> <br/> |<span data-ttu-id="f5dee-123">Der zu konvertierende Text.</span><span class="sxs-lookup"><span data-stu-id="f5dee-123">The text to convert.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5dee-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f5dee-124">Remarks</span></span>

<span data-ttu-id="f5dee-p101">Die REWIDEN-Funktion wird zur automatischen Konvertierung von Visio 2002-Dokumenten in Visio 2003-Dokumente verwendet. Eine andere Verwendung wird nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="f5dee-p101">The REWIDEN function is used in automatic conversion of Visio 2002 documents to Visio 2003 documents. Other use is not recommended.</span></span>
  

