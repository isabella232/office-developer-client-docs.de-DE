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
description: Wertet den Text in Shapename wie eine Formel aus und gibt das Ergebnis zurück.
ms.openlocfilehash: 69e79a23faa9d09aa2ad51f83363064b54742152
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796950"
---
# <a name="evaltext-function"></a><span data-ttu-id="00e58-103">EVALTEXT-Funktion</span><span class="sxs-lookup"><span data-stu-id="00e58-103">EVALTEXT Function</span></span>

<span data-ttu-id="00e58-104">Wertet den Text in _Shapename_ wie eine Formel aus und gibt das Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="00e58-104">Evaluates the text in  _shapename_ as if it were a formula and returns the result.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="00e58-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="00e58-105">Syntax</span></span>

<span data-ttu-id="00e58-106">EVALTEXT (** *Shapename! TheText* **)</span><span class="sxs-lookup"><span data-stu-id="00e58-106">EVALTEXT(** *shapename!theText* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="00e58-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="00e58-107">Parameters</span></span>

|<span data-ttu-id="00e58-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="00e58-108">**Name**</span></span>|<span data-ttu-id="00e58-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="00e58-109">**Required/Optional**</span></span>|<span data-ttu-id="00e58-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="00e58-110">**Data Type**</span></span>|<span data-ttu-id="00e58-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="00e58-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="00e58-112">_Shapename! TheText_</span><span class="sxs-lookup"><span data-stu-id="00e58-112">_shapename!theText_</span></span> <br/> |<span data-ttu-id="00e58-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="00e58-113">Required</span></span>  <br/> |<span data-ttu-id="00e58-114">**String**</span><span class="sxs-lookup"><span data-stu-id="00e58-114">**String**</span></span> <br/> |<span data-ttu-id="00e58-115">Eine Zelle, die bei Änderungen an der Textgestaltung des zugeordneten Shapes ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="00e58-115">A cell that is triggered when the associated shape's text composition changes.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="00e58-116">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="00e58-116">Return value</span></span>

<span data-ttu-id="00e58-117">String</span><span class="sxs-lookup"><span data-stu-id="00e58-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00e58-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="00e58-118">Remarks</span></span>

 <span data-ttu-id="00e58-119">_Shapename_ kann verwendet werden, um auf den Text eines Shapes als das aktuelle Shape zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="00e58-119">_shapename_ can be used to refer to the text of a shape other than the current shape.</span></span> 
  
<span data-ttu-id="00e58-p101">Wenn kein Text vorhanden ist, ist das Ergebnis 0. Wenn der Text nicht ausgewertet werden kann, gibt die Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="00e58-p101">If there is no text, the result is zero. If the text cannot be evaluated, the function returns an error.</span></span>
  
## <a name="example"></a><span data-ttu-id="00e58-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="00e58-122">Example</span></span>

<span data-ttu-id="00e58-123">EVALTEXT(Line.2!theText)</span><span class="sxs-lookup"><span data-stu-id="00e58-123">EVALTEXT(Line.2!theText)</span></span> 
  
<span data-ttu-id="00e58-p102">Wertet den Text des Shapes Line.2 aus. Wenn Line.2 beispielsweise den Text "4 ft + 0,5 ft" enthält, wird der Wert 4,5 ft zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="00e58-p102">Evaluates the text contained in the shape Line.2. For example, if Line.2 contains "4 ft + 0.5 ft", returns the value 4.5 ft.</span></span> 
  

