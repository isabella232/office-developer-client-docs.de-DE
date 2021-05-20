---
title: FIELDPICTURE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251592
localization_priority: Normal
ms.assetid: df88c55f-c098-dd4c-bf53-c7d7b60cf719
description: Gibt eine Zeichenfolge zum Formatieren von Bildern zurück, die dem internen Textfeld-Formatcode von Microsoft Visio entspricht.
ms.openlocfilehash: 1ab24c602c7975cf6be22a564a8b9ee9aa0d6f46
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431456"
---
# <a name="fieldpicture-function"></a><span data-ttu-id="533df-103">FIELDPICTURE Function</span><span class="sxs-lookup"><span data-stu-id="533df-103">FIELDPICTURE Function</span></span>

<span data-ttu-id="533df-104">Gibt eine Zeichenfolge zum Formatieren von Bildern zurück, die dem internen Textfeld-Formatcode von Microsoft Visio entspricht.</span><span class="sxs-lookup"><span data-stu-id="533df-104">Returns a format-picture string that matches the Microsoft Visio internal text field format code.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="533df-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="533df-105">Syntax</span></span>

<span data-ttu-id="533df-106">FIELDPICTURE(\*\* *code* \*\* )</span><span class="sxs-lookup"><span data-stu-id="533df-106">FIELDPICTURE(\*\* *code* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="533df-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="533df-107">Parameters</span></span>

|<span data-ttu-id="533df-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="533df-108">**Name**</span></span>|<span data-ttu-id="533df-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="533df-109">**Required/Optional**</span></span>|<span data-ttu-id="533df-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="533df-110">**Data Type**</span></span>|<span data-ttu-id="533df-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="533df-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="533df-112">_code_</span><span class="sxs-lookup"><span data-stu-id="533df-112">_code_</span></span> <br/> |<span data-ttu-id="533df-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="533df-113">Required</span></span>  <br/> |<span data-ttu-id="533df-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="533df-114">**Number**</span></span> <br/> | <span data-ttu-id="533df-115">Ein Textfeld-Formatcode.</span><span class="sxs-lookup"><span data-stu-id="533df-115">A text field format code.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="533df-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="533df-116">Return value</span></span>

<span data-ttu-id="533df-117">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="533df-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="533df-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="533df-118">Remarks</span></span>

<span data-ttu-id="533df-119">Zeichenfolgen für Formatierungsangaben werden in der FORMAT-Funktion verwendet, um die Expandierung von Werten zu Datumsangaben, Zeitangaben, Zahlen und Einheitenbeschriftungen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="533df-119">Format picture strings are used in the FORMAT function to define the expansion of values to dates, times, numbers, and unit labels.</span></span>
  
## <a name="example"></a><span data-ttu-id="533df-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="533df-120">Example</span></span>

<span data-ttu-id="533df-121">FIELDPICTURE(0)</span><span class="sxs-lookup"><span data-stu-id="533df-121">FIELDPICTURE(0)</span></span> 
  
<span data-ttu-id="533df-122">Gibt die Zeichenfolge für eine Formatierungsangabe "0,0" zurück, die eine Zahl mit einer Dezimalstelle und eine Einheitenbeschreibung in Kleinbuchstaben festlegt, wenn sie in der FORMAT-Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="533df-122">Returns the format picture string "esc(0)", which specifies a number that has one decimal place and a lowercase unit description when used in the FORMAT function.</span></span> 
  

