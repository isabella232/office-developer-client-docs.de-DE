---
title: UNICHAR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60117
localization_priority: Normal
ms.assetid: 371a475d-50f7-6b4c-4b47-581cd778dcba
description: Gibt das Unicode-Zeichen einer Zahl zurück.
ms.openlocfilehash: 81e76b72da35f79dee9ad6afbde51bc2e228483c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417581"
---
# <a name="unichar-function"></a><span data-ttu-id="c93a2-103">UNICHAR Function</span><span class="sxs-lookup"><span data-stu-id="c93a2-103">UNICHAR Function</span></span>

<span data-ttu-id="c93a2-104">Gibt das Unicode-Zeichen einer Zahl zurück.</span><span class="sxs-lookup"><span data-stu-id="c93a2-104">Returns the Unicode character from a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c93a2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c93a2-105">Syntax</span></span>

<span data-ttu-id="c93a2-106">UNICHAR (\*\* *number* \*\* )</span><span class="sxs-lookup"><span data-stu-id="c93a2-106">UNICHAR (\*\* *number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c93a2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c93a2-107">Parameters</span></span>

|<span data-ttu-id="c93a2-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c93a2-108">**Name**</span></span>|<span data-ttu-id="c93a2-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="c93a2-109">**Required/Optional**</span></span>|<span data-ttu-id="c93a2-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="c93a2-110">**Data Type**</span></span>|<span data-ttu-id="c93a2-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c93a2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c93a2-112">_Anzahl_</span><span class="sxs-lookup"><span data-stu-id="c93a2-112">_number_</span></span> <br/> |<span data-ttu-id="c93a2-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c93a2-113">Required</span></span>  <br/> |<span data-ttu-id="c93a2-114">**Integer**</span><span class="sxs-lookup"><span data-stu-id="c93a2-114">**Integer**</span></span> <br/> |<span data-ttu-id="c93a2-115">Eine ganze Zahl zwischen 1 und 65.535 (einschließlich); andernfalls gibt die Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="c93a2-115">An integer between 1 and 65,535 (inclusive), or the function returns an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c93a2-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c93a2-116">Remarks</span></span>

<span data-ttu-id="c93a2-117">Die resultierende Zeichenfolge hat eine Länge von einem Unicode-Zeichen (zwei Zeichen).</span><span class="sxs-lookup"><span data-stu-id="c93a2-117">The resulting string is one Unicode character (two characters) in length.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c93a2-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c93a2-118">Example</span></span>

<span data-ttu-id="c93a2-119">UNICHAR(65)</span><span class="sxs-lookup"><span data-stu-id="c93a2-119">UNICHAR(65)</span></span> 
  
<span data-ttu-id="c93a2-120">Gibt A zurück (lateinischer Großbuchstabe A)</span><span class="sxs-lookup"><span data-stu-id="c93a2-120">Returns A (Latin Capital Letter A)</span></span> 
  

