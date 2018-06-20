---
title: AND-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251391
localization_priority: Normal
ms.assetid: 434d7ceb-1050-c667-fb3d-b6634440c18e
description: Gibt TRUE (1) zurück, wenn alle angegebenen logischen Ausdrücke wahr sind. Wenn einer der logischen Ausdrücke FALSE oder 0 ist, gibt die Funktion und FALSE (0) zurück.
ms.openlocfilehash: 27b2ef97ef1d0afde37596b18674c6de26355a1b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796409"
---
# <a name="and-function"></a><span data-ttu-id="0165b-104">AND Function</span><span class="sxs-lookup"><span data-stu-id="0165b-104">AND Function</span></span>

<span data-ttu-id="0165b-105">Gibt TRUE (1) zurück, wenn alle angegebenen logischen Ausdrücke wahr sind.</span><span class="sxs-lookup"><span data-stu-id="0165b-105">Returns TRUE (1) if all of the logical expressions supplied are TRUE.</span></span> <span data-ttu-id="0165b-106">Wenn einer der logischen Ausdrücke FALSE oder 0 ist, gibt die Funktion und FALSE (0) zurück.</span><span class="sxs-lookup"><span data-stu-id="0165b-106">If any of the logical expressions are FALSE or 0, the AND function returns FALSE (0).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0165b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0165b-107">Syntax</span></span>

<span data-ttu-id="0165b-108">UND (** *logische expression1* **, ** *logische expression2* **,..., ** *logische ExpressionN* **)</span><span class="sxs-lookup"><span data-stu-id="0165b-108">AND(** *logical expression1* **, ** *logical expression2* **,..., ** *logical expressionN* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0165b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0165b-109">Parameters</span></span>

|<span data-ttu-id="0165b-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="0165b-110">**Name**</span></span>|<span data-ttu-id="0165b-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="0165b-111">**Required/Optional**</span></span>|<span data-ttu-id="0165b-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="0165b-112">**Data Type**</span></span>|<span data-ttu-id="0165b-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0165b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0165b-114">_logische Ausdruck_</span><span class="sxs-lookup"><span data-stu-id="0165b-114">_logical expression_</span></span> <br/> |<span data-ttu-id="0165b-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0165b-115">Required</span></span>  <br/> |<span data-ttu-id="0165b-116">**String**</span><span class="sxs-lookup"><span data-stu-id="0165b-116">**String**</span></span> <br/> | <span data-ttu-id="0165b-p103">Eine Kombination aus Konstanten, Operatoren, Funktionen und Verweisen auf ShapeSheet-Zellen, die einen Wert ergeben. Ein mit einem Wert ungleich null ausgewerteter Ausdruck wird als TRUE angegeben.</span><span class="sxs-lookup"><span data-stu-id="0165b-p103">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value. Any expression that evaluates to a non-zero value is considered to be TRUE.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="0165b-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0165b-119">Example</span></span>

<span data-ttu-id="0165b-120">UND (Höhe \> 1, DrehbezX \> 1)</span><span class="sxs-lookup"><span data-stu-id="0165b-120">AND(Height \> 1, PinX \> 1)</span></span>
  
<span data-ttu-id="0165b-p104">Liefert TRUE, wenn beide Ausdrücke TRUE sind. Liefert FALSE, wenn einer der beiden Ausdrücke FALSE ist.</span><span class="sxs-lookup"><span data-stu-id="0165b-p104">Returns TRUE if both expressions are TRUE. Returns FALSE if either expression is FALSE.</span></span>
  

