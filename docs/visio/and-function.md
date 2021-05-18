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
description: Gibt TRUE (1) zurück, wenn alle angegebenen logischen Ausdrücke TRUE sind. Wenn einer der logischen Ausdrücke FALSE oder 0 ist, gibt die AND-Funktion FALSE (0) zurück.
ms.openlocfilehash: 74e8301718e69a2ab61f6bf9992d0d6855bbc6f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422012"
---
# <a name="and-function"></a><span data-ttu-id="0bac8-104">AND Function</span><span class="sxs-lookup"><span data-stu-id="0bac8-104">AND Function</span></span>

<span data-ttu-id="0bac8-105">Gibt TRUE (1) zurück, wenn alle angegebenen logischen Ausdrücke TRUE sind.</span><span class="sxs-lookup"><span data-stu-id="0bac8-105">Returns TRUE (1) if all of the logical expressions supplied are TRUE.</span></span> <span data-ttu-id="0bac8-106">Wenn einer der logischen Ausdrücke FALSE oder 0 ist, gibt die AND-Funktion FALSE (0) zurück.</span><span class="sxs-lookup"><span data-stu-id="0bac8-106">If any of the logical expressions are FALSE or 0, the AND function returns FALSE (0).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0bac8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0bac8-107">Syntax</span></span>

<span data-ttu-id="0bac8-108">AND(\*\* *logischer Ausdruck1* \*\*, \*\* *logischer Ausdruck2* \*\*,..., \*\* *logischer AusdruckN* \*\* )</span><span class="sxs-lookup"><span data-stu-id="0bac8-108">AND(\*\* *logical expression1* \*\*, \*\* *logical expression2* \*\*,..., \*\* *logical expressionN* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0bac8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0bac8-109">Parameters</span></span>

|<span data-ttu-id="0bac8-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="0bac8-110">**Name**</span></span>|<span data-ttu-id="0bac8-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="0bac8-111">**Required/Optional**</span></span>|<span data-ttu-id="0bac8-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="0bac8-112">**Data Type**</span></span>|<span data-ttu-id="0bac8-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0bac8-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0bac8-114">_logischer Ausdruck_</span><span class="sxs-lookup"><span data-stu-id="0bac8-114">_logical expression_</span></span> <br/> |<span data-ttu-id="0bac8-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0bac8-115">Required</span></span>  <br/> |<span data-ttu-id="0bac8-116">**String**</span><span class="sxs-lookup"><span data-stu-id="0bac8-116">**String**</span></span> <br/> | <span data-ttu-id="0bac8-p103">Eine Kombination aus Konstanten, Operatoren, Funktionen und Verweisen auf ShapeSheet-Zellen, die einen Wert ergeben. Ein mit einem Wert ungleich null ausgewerteter Ausdruck wird als TRUE angegeben.</span><span class="sxs-lookup"><span data-stu-id="0bac8-p103">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value. Any expression that evaluates to a non-zero value is considered to be TRUE.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="0bac8-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0bac8-119">Example</span></span>

<span data-ttu-id="0bac8-120">AND(Height \> 1, PinX \> 1)</span><span class="sxs-lookup"><span data-stu-id="0bac8-120">AND(Height \> 1, PinX \> 1)</span></span>
  
<span data-ttu-id="0bac8-p104">Liefert TRUE, wenn beide Ausdrücke TRUE sind. Liefert FALSE, wenn einer der beiden Ausdrücke FALSE ist.</span><span class="sxs-lookup"><span data-stu-id="0bac8-p104">Returns TRUE if both expressions are TRUE. Returns FALSE if either expression is FALSE.</span></span>
  

