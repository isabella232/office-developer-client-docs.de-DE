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
ms.openlocfilehash: 06f97717ee4d5965253b0da7cfd5c35faf0ca2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798350"
---
# <a name="unichar-function"></a><span data-ttu-id="3806b-103">UNICHAR Function</span><span class="sxs-lookup"><span data-stu-id="3806b-103">UNICHAR Function</span></span>

<span data-ttu-id="3806b-104">Gibt das Unicode-Zeichen einer Zahl zurück.</span><span class="sxs-lookup"><span data-stu-id="3806b-104">Returns the Unicode character from a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3806b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3806b-105">Syntax</span></span>

<span data-ttu-id="3806b-106">UNICHAR (** *Anzahl* **)</span><span class="sxs-lookup"><span data-stu-id="3806b-106">UNICHAR (** *number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3806b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3806b-107">Parameters</span></span>

|<span data-ttu-id="3806b-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="3806b-108">**Name**</span></span>|<span data-ttu-id="3806b-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="3806b-109">**Required/Optional**</span></span>|<span data-ttu-id="3806b-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="3806b-110">**Data Type**</span></span>|<span data-ttu-id="3806b-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3806b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3806b-112">_Anzahl_</span><span class="sxs-lookup"><span data-stu-id="3806b-112">_number_</span></span> <br/> |<span data-ttu-id="3806b-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="3806b-113">Required</span></span>  <br/> |<span data-ttu-id="3806b-114">**Integer**</span><span class="sxs-lookup"><span data-stu-id="3806b-114">**Integer**</span></span> <br/> |<span data-ttu-id="3806b-115">Eine ganze Zahl zwischen 1 und 65.535 (einschließlich); andernfalls gibt die Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="3806b-115">An integer between 1 and 65,535 (inclusive), or the function returns an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3806b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3806b-116">Remarks</span></span>

<span data-ttu-id="3806b-117">Die resultierende Zeichenfolge hat eine Länge von einem Unicode-Zeichen (zwei Zeichen).</span><span class="sxs-lookup"><span data-stu-id="3806b-117">The resulting string is one Unicode character (two characters) in length.</span></span> 
  
## <a name="example"></a><span data-ttu-id="3806b-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3806b-118">Example</span></span>

<span data-ttu-id="3806b-119">UNICHAR(65)</span><span class="sxs-lookup"><span data-stu-id="3806b-119">UNICHAR(65)</span></span> 
  
<span data-ttu-id="3806b-120">Gibt ein (lateinischen Großbuchstaben A)</span><span class="sxs-lookup"><span data-stu-id="3806b-120">Returns A (Latin Capital Letter A)</span></span> 
  

