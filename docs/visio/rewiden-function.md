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
description: Konvertiert eine Formel, die 16-Bit-Zeichencodes erstellt, die ein-Byte-oder Multibyte Character-Set-Codes in eine Zeichenfolge mit 16-Bit-Unicode-Zeichencodes unter Verwendung der angegebenen Zeichensätze vergrößert werden.
ms.openlocfilehash: c885487f91e541027b7ba09812e7321a9deb00ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326768"
---
# <a name="rewiden-function"></a><span data-ttu-id="9325a-103">REWIDEN Function</span><span class="sxs-lookup"><span data-stu-id="9325a-103">REWIDEN Function</span></span>

<span data-ttu-id="9325a-104">Konvertiert eine Formel, die 16-Bit-Zeichencodes erstellt, die ein-Byte-oder Multibyte Character-Set-Codes in eine Zeichenfolge mit 16-Bit-Unicode-Zeichencodes unter Verwendung der angegebenen Zeichensätze vergrößert werden.</span><span class="sxs-lookup"><span data-stu-id="9325a-104">Converts a formula that produces 16-bit character codes that are widened single-byte or multibyte character-set codes into a string of 16-bit Unicode character codes, using the specified character sets.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9325a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9325a-105">Syntax</span></span>

<span data-ttu-id="9325a-106">ReWIDEn (\* \* *srcCharSet* \* \*, \* \* *dstCharSet* \* \*, \* \* *Text* \* \*)</span><span class="sxs-lookup"><span data-stu-id="9325a-106">REWIDEN(\*\* *srcCharSet* \*\*, \*\* *dstCharSet* \*\*, \*\* *text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9325a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9325a-107">Parameters</span></span>

|<span data-ttu-id="9325a-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="9325a-108">**Name**</span></span>|<span data-ttu-id="9325a-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="9325a-109">**Required/Optional**</span></span>|<span data-ttu-id="9325a-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9325a-110">**Data Type**</span></span>|<span data-ttu-id="9325a-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9325a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9325a-112">_srcCharSet_</span><span class="sxs-lookup"><span data-stu-id="9325a-112">_srcCharSet_</span></span> <br/> |<span data-ttu-id="9325a-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9325a-113">Required</span></span>  <br/> |<span data-ttu-id="9325a-114">**String**</span><span class="sxs-lookup"><span data-stu-id="9325a-114">**String**</span></span> <br/> |<span data-ttu-id="9325a-115">Der Zeichensatz im Quelldokument.</span><span class="sxs-lookup"><span data-stu-id="9325a-115">The character set in the source document.</span></span>  <br/> |
| <span data-ttu-id="9325a-116">_dstCharSet_</span><span class="sxs-lookup"><span data-stu-id="9325a-116">_dstCharSet_</span></span> <br/> |<span data-ttu-id="9325a-117">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9325a-117">Required</span></span>  <br/> |<span data-ttu-id="9325a-118">**String**</span><span class="sxs-lookup"><span data-stu-id="9325a-118">**String**</span></span> <br/> | <span data-ttu-id="9325a-119">Der Zeichensatz im Zieldokument.</span><span class="sxs-lookup"><span data-stu-id="9325a-119">The character set in the destination document.</span></span>  <br/> |
| <span data-ttu-id="9325a-120">_text_</span><span class="sxs-lookup"><span data-stu-id="9325a-120">_text_</span></span> <br/> |<span data-ttu-id="9325a-121">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="9325a-121">Required</span></span>  <br/> |<span data-ttu-id="9325a-122">**String**</span><span class="sxs-lookup"><span data-stu-id="9325a-122">**String**</span></span> <br/> |<span data-ttu-id="9325a-123">Der zu konvertierende Text.</span><span class="sxs-lookup"><span data-stu-id="9325a-123">The text to convert.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9325a-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9325a-124">Remarks</span></span>

<span data-ttu-id="9325a-p101">Die REWIDEN-Funktion wird zur automatischen Konvertierung von Visio 2002-Dokumenten in Visio 2003-Dokumente verwendet. Eine andere Verwendung wird nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="9325a-p101">The REWIDEN function is used in automatic conversion of Visio 2002 documents to Visio 2003 documents. Other use is not recommended.</span></span>
  

