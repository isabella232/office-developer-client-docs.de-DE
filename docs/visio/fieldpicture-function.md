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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322547"
---
# <a name="fieldpicture-function"></a><span data-ttu-id="58045-103">FIELDPICTURE Function</span><span class="sxs-lookup"><span data-stu-id="58045-103">FIELDPICTURE Function</span></span>

<span data-ttu-id="58045-104">Gibt eine Zeichenfolge zum Formatieren von Bildern zurück, die dem internen Textfeld-Formatcode von Microsoft Visio entspricht.</span><span class="sxs-lookup"><span data-stu-id="58045-104">Returns a format-picture string that matches the Microsoft Visio internal text field format code.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="58045-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="58045-105">Syntax</span></span>

<span data-ttu-id="58045-106">FIELDPICTURE (\* \* *Code* \* \*)</span><span class="sxs-lookup"><span data-stu-id="58045-106">FIELDPICTURE(\*\* *code* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="58045-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="58045-107">Parameters</span></span>

|<span data-ttu-id="58045-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="58045-108">**Name**</span></span>|<span data-ttu-id="58045-109">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="58045-109">**Required/Optional**</span></span>|<span data-ttu-id="58045-110">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="58045-110">**Data Type**</span></span>|<span data-ttu-id="58045-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="58045-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="58045-112">_code_</span><span class="sxs-lookup"><span data-stu-id="58045-112">_code_</span></span> <br/> |<span data-ttu-id="58045-113">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="58045-113">Required</span></span>  <br/> |<span data-ttu-id="58045-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="58045-114">**Number**</span></span> <br/> | <span data-ttu-id="58045-115">Ein Textfeld-Formatcode.</span><span class="sxs-lookup"><span data-stu-id="58045-115">A text field format code.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="58045-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58045-116">Return value</span></span>

<span data-ttu-id="58045-117">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="58045-117">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="58045-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58045-118">Remarks</span></span>

<span data-ttu-id="58045-119">Zeichenfolgen für Formatierungsangaben werden in der FORMAT-Funktion verwendet, um die Expandierung von Werten zu Datumsangaben, Zeitangaben, Zahlen und Einheitenbeschriftungen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="58045-119">Format picture strings are used in the FORMAT function to define the expansion of values to dates, times, numbers, and unit labels.</span></span>
  
## <a name="example"></a><span data-ttu-id="58045-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="58045-120">Example</span></span>

<span data-ttu-id="58045-121">FIELDPICTURE (0)</span><span class="sxs-lookup"><span data-stu-id="58045-121">FIELDPICTURE(0)</span></span> 
  
<span data-ttu-id="58045-122">Gibt die Zeichenfolge für eine Formatierungsangabe "0,0" zurück, die eine Zahl mit einer Dezimalstelle und eine Einheitenbeschreibung in Kleinbuchstaben festlegt, wenn sie in der FORMAT-Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="58045-122">Returns the format picture string "esc(0)", which specifies a number that has one decimal place and a lowercase unit description when used in the FORMAT function.</span></span> 
  

