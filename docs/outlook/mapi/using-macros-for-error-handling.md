---
title: Verwenden von Makros zur Fehlerbehandlung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c4e216f2204f4ee97d9eeac81f77ce6a82fff3f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795822"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="e28a6-103">Verwenden von Makros zur Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="e28a6-103">Using Macros for Error Handling</span></span>

  
  
<span data-ttu-id="e28a6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e28a6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e28a6-105">Es gibt mehrere Makros für entwickelt HRESULT-Werte zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="e28a6-105">There are several macros for making it easier to work with HRESULT values.</span></span>
  
<span data-ttu-id="e28a6-106">Es gibt zwei Sätze von Makros, die für Fehler oder Erfolg zu testen: HR_SUCCEEDED und HR_FAILED und SUCCEEDED und FAILED.</span><span class="sxs-lookup"><span data-stu-id="e28a6-106">There are two sets of macros that test for failure or success: HR_SUCCEEDED and HR_FAILED and SUCCEEDED and FAILED.</span></span> <span data-ttu-id="e28a6-107">Erfolgreich abgeschlossen wurde, handelt es sich um dieselbe wie HR_SUCCEEDED und fehlgeschlagen HR_FAILED identisch ist.</span><span class="sxs-lookup"><span data-stu-id="e28a6-107">SUCCEEDED is the same as HR_SUCCEEDED and FAILED is the same as HR_FAILED.</span></span>
  
<span data-ttu-id="e28a6-108">In diesem Fall verwenden Sie das Makro **ResultFromScode** , um die HRESULT-Variable auf den entsprechenden HRESULT-Wert für S_OK festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e28a6-108">In this case, use the **ResultFromScode** macro to set the HRESULT variable to the corresponding HRESULT value for S_OK.</span></span> 
  
<span data-ttu-id="e28a6-109">Häufig verwendete Makros werden in der folgenden Tabelle kurz beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e28a6-109">Commonly used macros are briefly described in the following table.</span></span>
  
|<span data-ttu-id="e28a6-110">**Makro**</span><span class="sxs-lookup"><span data-stu-id="e28a6-110">**Macro**</span></span>|<span data-ttu-id="e28a6-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e28a6-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e28a6-112">**MAKE_HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e28a6-112">**MAKE_HRESULT**</span></span> <br/> |<span data-ttu-id="e28a6-113">Erstellt ein HRESULT aus seiner Komponenten.</span><span class="sxs-lookup"><span data-stu-id="e28a6-113">Constructs an HRESULT from its components.</span></span>  <br/> |
|<span data-ttu-id="e28a6-114">**HR_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="e28a6-114">**HR_SUCCEEDED**</span></span> <br/> |<span data-ttu-id="e28a6-115">Ein HRESULT für einen Erfolg oder eine Warnung Bedingung getestet.</span><span class="sxs-lookup"><span data-stu-id="e28a6-115">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="e28a6-116">**HR_FAILED**</span><span class="sxs-lookup"><span data-stu-id="e28a6-116">**HR_FAILED**</span></span> <br/> |<span data-ttu-id="e28a6-117">Ein HRESULT für ein Fehlerzustand getestet.</span><span class="sxs-lookup"><span data-stu-id="e28a6-117">Tests an HRESULT for an error condition.</span></span>  <br/> |
|<span data-ttu-id="e28a6-118">**HRESULT_CODE**</span><span class="sxs-lookup"><span data-stu-id="e28a6-118">**HRESULT_CODE**</span></span> <br/> |<span data-ttu-id="e28a6-119">Den Fehler Codeteil der HRESULT extrahiert.</span><span class="sxs-lookup"><span data-stu-id="e28a6-119">Extracts the error code part of the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="e28a6-120">**HRESULT_FACILITY**</span><span class="sxs-lookup"><span data-stu-id="e28a6-120">**HRESULT_FACILITY**</span></span> <br/> |<span data-ttu-id="e28a6-121">Extrahiert die Einrichtung von HRESULT.</span><span class="sxs-lookup"><span data-stu-id="e28a6-121">Extracts the facility from the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="e28a6-122">**HRESULT_SEVERITY**</span><span class="sxs-lookup"><span data-stu-id="e28a6-122">**HRESULT_SEVERITY**</span></span> <br/> |<span data-ttu-id="e28a6-123">Extrahiert das Severity Bit Schweregrad.</span><span class="sxs-lookup"><span data-stu-id="e28a6-123">Extracts the severity bit from the SEVERITY.</span></span>  <br/> |
|<span data-ttu-id="e28a6-124">**ERFOLGREICH ABGESCHLOSSEN WURDE**</span><span class="sxs-lookup"><span data-stu-id="e28a6-124">**SUCCEEDED**</span></span> <br/> |<span data-ttu-id="e28a6-125">Ein HRESULT für einen Erfolg oder eine Warnung Bedingung getestet.</span><span class="sxs-lookup"><span data-stu-id="e28a6-125">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="e28a6-126">**FEHLER BEI**</span><span class="sxs-lookup"><span data-stu-id="e28a6-126">**FAILED**</span></span> <br/> |<span data-ttu-id="e28a6-127">Ein HRESULT für ein Fehlerzustand getestet.</span><span class="sxs-lookup"><span data-stu-id="e28a6-127">Tests an HRESULT for an error condition.</span></span>  <br/> |
   

