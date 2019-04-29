---
title: EVALTEXT-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251422
localization_priority: Normal
ms.assetid: c9b5b96c-d8c8-6119-e3f1-a2ce9d7c043e
description: Wertet den Text in Shapename so aus, als ob er eine Formel wäre, und gibt das Ergebnis zurück.
ms.openlocfilehash: 6600d9d6ddaf630a93fdb5c37639ce50a21a4307
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438358"
---
# <a name="evaltext-function"></a><span data-ttu-id="f4f16-103">EVALTEXT Function</span><span class="sxs-lookup"><span data-stu-id="f4f16-103">EVALTEXT Function</span></span>

<span data-ttu-id="f4f16-104">Wertet den Text __ in Shapename so aus, als ob er eine Formel wäre, und gibt das Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="f4f16-104">Evaluates the text in  _shapename_ as if it were a formula and returns the result.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f4f16-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4f16-105">Syntax</span></span>

<span data-ttu-id="f4f16-106">EVALTEXT (\* \* *Shapename! DerText* \* \*)</span><span class="sxs-lookup"><span data-stu-id="f4f16-106">EVALTEXT(\*\* *shapename!theText* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f4f16-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4f16-107">Parameters</span></span>

|<span data-ttu-id="f4f16-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="f4f16-108">**Name**</span></span>|<span data-ttu-id="f4f16-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="f4f16-109">**Required/Optional**</span></span>|<span data-ttu-id="f4f16-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="f4f16-110">**Data Type**</span></span>|<span data-ttu-id="f4f16-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f4f16-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f4f16-112">_Shapename! DerText_</span><span class="sxs-lookup"><span data-stu-id="f4f16-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="f4f16-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f4f16-113">Required</span></span>  <br/> |<span data-ttu-id="f4f16-114">**String**</span><span class="sxs-lookup"><span data-stu-id="f4f16-114">**String**</span></span> <br/> |<span data-ttu-id="f4f16-115">Eine Zelle, die bei Änderungen an der Textgestaltung des zugeordneten Shapes ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="f4f16-115">A cell that is triggered when the associated shape's text composition changes.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f4f16-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4f16-116">Return value</span></span>

<span data-ttu-id="f4f16-117">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f4f16-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f4f16-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4f16-118">Remarks</span></span>

 <span data-ttu-id="f4f16-119">Mit _shapename_ kann auf den Text eines anderen Shapes (statt auf den Text des aktuellen Shapes) verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="f4f16-119">_shapename_ can be used to refer to the text of a shape other than the current shape.</span></span> 
  
<span data-ttu-id="f4f16-120">Wenn kein Text vorhanden ist, ist das Ergebnis 0.</span><span class="sxs-lookup"><span data-stu-id="f4f16-120">If there is no text, the result is zero.</span></span> <span data-ttu-id="f4f16-121">Wenn der Text nicht ausgewertet werden kann, gibt die Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="f4f16-121">If the text cannot be evaluated, the function returns an error.</span></span>
  
## <a name="example"></a><span data-ttu-id="f4f16-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f4f16-122">Example</span></span>

<span data-ttu-id="f4f16-123">EVALTEXT (Leitung 2! DerText)</span><span class="sxs-lookup"><span data-stu-id="f4f16-123">EVALTEXT(Line.2!theText)</span></span> 
  
<span data-ttu-id="f4f16-p102">Wertet den Text des Shapes Line.2 aus. Wenn Line.2 beispielsweise den Text "4 ft + 0,5 ft" enthält, wird der Wert 4,5 ft zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f4f16-p102">Evaluates the text contained in the shape Line.2. For example, if Line.2 contains "4 ft + 0.5 ft", returns the value 4.5 ft.</span></span> 
  

