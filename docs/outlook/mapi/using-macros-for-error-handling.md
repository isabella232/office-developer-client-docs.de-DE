---
title: Verwenden von Makros zur Fehlerbehandlung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 715cd001c5eab89f40c31200a12deaf6981b9a61
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567125"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="005c3-103">Verwenden von Makros zur Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="005c3-103">Using Macros for Error Handling</span></span>

  
  
<span data-ttu-id="005c3-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="005c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="005c3-105">Es gibt mehrere Makros für entwickelt HRESULT-Werte zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="005c3-105">There are several macros for making it easier to work with HRESULT values.</span></span>
  
<span data-ttu-id="005c3-106">Es gibt zwei Sätze von Makros, die für Fehler oder Erfolg zu testen: HR_SUCCEEDED und HR_FAILED und SUCCEEDED und FAILED.</span><span class="sxs-lookup"><span data-stu-id="005c3-106">There are two sets of macros that test for failure or success: HR_SUCCEEDED and HR_FAILED and SUCCEEDED and FAILED.</span></span> <span data-ttu-id="005c3-107">Erfolgreich abgeschlossen wurde, handelt es sich um dieselbe wie HR_SUCCEEDED und fehlgeschlagen HR_FAILED identisch ist.</span><span class="sxs-lookup"><span data-stu-id="005c3-107">SUCCEEDED is the same as HR_SUCCEEDED and FAILED is the same as HR_FAILED.</span></span>
  
<span data-ttu-id="005c3-108">In diesem Fall verwenden Sie das Makro **ResultFromScode** , um die HRESULT-Variable auf den entsprechenden HRESULT-Wert für S_OK festzulegen.</span><span class="sxs-lookup"><span data-stu-id="005c3-108">In this case, use the **ResultFromScode** macro to set the HRESULT variable to the corresponding HRESULT value for S_OK.</span></span> 
  
<span data-ttu-id="005c3-109">Häufig verwendete Makros werden in der folgenden Tabelle kurz beschrieben.</span><span class="sxs-lookup"><span data-stu-id="005c3-109">Commonly used macros are briefly described in the following table.</span></span>
  
|<span data-ttu-id="005c3-110">**Makro**</span><span class="sxs-lookup"><span data-stu-id="005c3-110">**Macro**</span></span>|<span data-ttu-id="005c3-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="005c3-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="005c3-112">**MAKE_HRESULT**</span><span class="sxs-lookup"><span data-stu-id="005c3-112">**MAKE_HRESULT**</span></span> <br/> |<span data-ttu-id="005c3-113">Erstellt ein HRESULT aus seiner Komponenten.</span><span class="sxs-lookup"><span data-stu-id="005c3-113">Constructs an HRESULT from its components.</span></span>  <br/> |
|<span data-ttu-id="005c3-114">**HR_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="005c3-114">**HR_SUCCEEDED**</span></span> <br/> |<span data-ttu-id="005c3-115">Ein HRESULT für einen Erfolg oder eine Warnung Bedingung getestet.</span><span class="sxs-lookup"><span data-stu-id="005c3-115">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="005c3-116">**HR_FAILED**</span><span class="sxs-lookup"><span data-stu-id="005c3-116">**HR_FAILED**</span></span> <br/> |<span data-ttu-id="005c3-117">Ein HRESULT für ein Fehlerzustand getestet.</span><span class="sxs-lookup"><span data-stu-id="005c3-117">Tests an HRESULT for an error condition.</span></span>  <br/> |
|<span data-ttu-id="005c3-118">**HRESULT_CODE**</span><span class="sxs-lookup"><span data-stu-id="005c3-118">**HRESULT_CODE**</span></span> <br/> |<span data-ttu-id="005c3-119">Den Fehler Codeteil der HRESULT extrahiert.</span><span class="sxs-lookup"><span data-stu-id="005c3-119">Extracts the error code part of the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="005c3-120">**HRESULT_FACILITY**</span><span class="sxs-lookup"><span data-stu-id="005c3-120">**HRESULT_FACILITY**</span></span> <br/> |<span data-ttu-id="005c3-121">Extrahiert die Einrichtung von HRESULT.</span><span class="sxs-lookup"><span data-stu-id="005c3-121">Extracts the facility from the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="005c3-122">**HRESULT_SEVERITY**</span><span class="sxs-lookup"><span data-stu-id="005c3-122">**HRESULT_SEVERITY**</span></span> <br/> |<span data-ttu-id="005c3-123">Extrahiert das Severity Bit Schweregrad.</span><span class="sxs-lookup"><span data-stu-id="005c3-123">Extracts the severity bit from the SEVERITY.</span></span>  <br/> |
|<span data-ttu-id="005c3-124">**ERFOLGREICH ABGESCHLOSSEN WURDE**</span><span class="sxs-lookup"><span data-stu-id="005c3-124">**SUCCEEDED**</span></span> <br/> |<span data-ttu-id="005c3-125">Ein HRESULT für einen Erfolg oder eine Warnung Bedingung getestet.</span><span class="sxs-lookup"><span data-stu-id="005c3-125">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="005c3-126">**FEHLER BEI**</span><span class="sxs-lookup"><span data-stu-id="005c3-126">**FAILED**</span></span> <br/> |<span data-ttu-id="005c3-127">Ein HRESULT für ein Fehlerzustand getestet.</span><span class="sxs-lookup"><span data-stu-id="005c3-127">Tests an HRESULT for an error condition.</span></span>  <br/> |
   

