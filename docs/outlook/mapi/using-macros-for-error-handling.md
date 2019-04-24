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
ms.openlocfilehash: 9e6901d6583e7a7924a4a7c19c0a262bcef74bd3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329659"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="da599-103">Verwenden von Makros zur Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="da599-103">Using Macros for Error Handling</span></span>

  
  
<span data-ttu-id="da599-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da599-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da599-105">Es gibt mehrere Makros, um die Arbeit mit HRESULT-Werten zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="da599-105">There are several macros for making it easier to work with HRESULT values.</span></span>
  
<span data-ttu-id="da599-106">Es gibt zwei Gruppen von Makros, die auf Fehler oder Erfolg testen: HR_SUCCEEDED und HR_FAILED und erfolgreich und fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="da599-106">There are two sets of macros that test for failure or success: HR_SUCCEEDED and HR_FAILED and SUCCEEDED and FAILED.</span></span> <span data-ttu-id="da599-107">SUCCEEDed ist identisch mit HR_SUCCEEDED und FAILED ist identisch mit HR_FAILED.</span><span class="sxs-lookup"><span data-stu-id="da599-107">SUCCEEDED is the same as HR_SUCCEEDED and FAILED is the same as HR_FAILED.</span></span>
  
<span data-ttu-id="da599-108">Verwenden Sie in diesem Fall das **ResultFromScode** -Makro, um die HRESULT-Variable auf den entsprechenden HRESULT-Wert für S_OK festzulegen.</span><span class="sxs-lookup"><span data-stu-id="da599-108">In this case, use the **ResultFromScode** macro to set the HRESULT variable to the corresponding HRESULT value for S_OK.</span></span> 
  
<span data-ttu-id="da599-109">Häufig verwendete Makros werden in der folgenden Tabelle kurz beschrieben.</span><span class="sxs-lookup"><span data-stu-id="da599-109">Commonly used macros are briefly described in the following table.</span></span>
  
|<span data-ttu-id="da599-110">**Makro**</span><span class="sxs-lookup"><span data-stu-id="da599-110">**Macro**</span></span>|<span data-ttu-id="da599-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="da599-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="da599-112">**MAKE_HRESULT**</span><span class="sxs-lookup"><span data-stu-id="da599-112">**MAKE_HRESULT**</span></span> <br/> |<span data-ttu-id="da599-113">Erstellt ein HRESULT aus seinen Komponenten.</span><span class="sxs-lookup"><span data-stu-id="da599-113">Constructs an HRESULT from its components.</span></span>  <br/> |
|<span data-ttu-id="da599-114">**HR_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="da599-114">**HR_SUCCEEDED**</span></span> <br/> |<span data-ttu-id="da599-115">Testet ein HRESULT für eine Erfolgs-oder Warnungsbedingung.</span><span class="sxs-lookup"><span data-stu-id="da599-115">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="da599-116">**HR_FAILED**</span><span class="sxs-lookup"><span data-stu-id="da599-116">**HR_FAILED**</span></span> <br/> |<span data-ttu-id="da599-117">Testet ein HRESULT auf eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="da599-117">Tests an HRESULT for an error condition.</span></span>  <br/> |
|<span data-ttu-id="da599-118">**HRESULT_CODE**</span><span class="sxs-lookup"><span data-stu-id="da599-118">**HRESULT_CODE**</span></span> <br/> |<span data-ttu-id="da599-119">Extrahiert den Fehlercode Teil von HRESULT.</span><span class="sxs-lookup"><span data-stu-id="da599-119">Extracts the error code part of the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="da599-120">**HRESULT_FACILITY**</span><span class="sxs-lookup"><span data-stu-id="da599-120">**HRESULT_FACILITY**</span></span> <br/> |<span data-ttu-id="da599-121">Extrahiert die Einrichtung aus dem HRESULT.</span><span class="sxs-lookup"><span data-stu-id="da599-121">Extracts the facility from the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="da599-122">**HRESULT_SEVERITY**</span><span class="sxs-lookup"><span data-stu-id="da599-122">**HRESULT_SEVERITY**</span></span> <br/> |<span data-ttu-id="da599-123">Extrahiert das Schweregrad-Bit aus dem Schweregrad.</span><span class="sxs-lookup"><span data-stu-id="da599-123">Extracts the severity bit from the SEVERITY.</span></span>  <br/> |
|<span data-ttu-id="da599-124">**GELUNGEN**</span><span class="sxs-lookup"><span data-stu-id="da599-124">**SUCCEEDED**</span></span> <br/> |<span data-ttu-id="da599-125">Testet ein HRESULT für eine Erfolgs-oder Warnungsbedingung.</span><span class="sxs-lookup"><span data-stu-id="da599-125">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="da599-126">**NICHT**</span><span class="sxs-lookup"><span data-stu-id="da599-126">**FAILED**</span></span> <br/> |<span data-ttu-id="da599-127">Testet ein HRESULT auf eine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="da599-127">Tests an HRESULT for an error condition.</span></span>  <br/> |
   

