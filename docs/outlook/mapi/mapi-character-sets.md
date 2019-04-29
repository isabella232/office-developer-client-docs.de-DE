---
title: MAPI-Zeichensätze
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe63916-b3eb-4ea7-bc42-80a8b0281b03
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 898883d8c93b69762883a502b7a4313b3417d0d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417553"
---
# <a name="mapi-character-sets"></a><span data-ttu-id="9dd9b-103">MAPI-Zeichensätze</span><span class="sxs-lookup"><span data-stu-id="9dd9b-103">MAPI Character Sets</span></span>

  
  
<span data-ttu-id="9dd9b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9dd9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9dd9b-105">MAPI-kompatible Clientanwendungen und Dienstanbieter können ANSI-Zeichen (Single Byte) oder Unicode-Zeichen (Double Byte) verwenden.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-105">MAPI-compliant client applications and service providers can use ANSI characters (single byte) or Unicode characters (double byte).</span></span> <span data-ttu-id="9dd9b-106">OEM-Zeichensätze werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-106">OEM character sets are not supported.</span></span> <span data-ttu-id="9dd9b-107">Eine OEM-Zeichenfolge, die an eine MAPI-Methode oder-Funktion übergeben wird, führt zu einer fehlerhaften Methode oder Funktion.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-107">An OEM string passed to a MAPI method or function will cause that method or function to fail.</span></span> <span data-ttu-id="9dd9b-108">Client Anwendungen, die mit Dateinamen im OEM-Zeichensatz arbeiten, müssen darauf achten, Sie in ANSI zu konvertieren, bevor Sie an eine MAPI-Methode oder-Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-108">Client applications that work with filenames in the OEM character set must be careful to convert them to ANSI before passing them to a MAPI method or function.</span></span>
  
<span data-ttu-id="9dd9b-109">Die Unterstützung des Unicode-Zeichensatzes ist optional, sowohl für Clients als auch für Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-109">Supporting the Unicode character set is optional, both for clients and service providers.</span></span> <span data-ttu-id="9dd9b-110">Alle Dienstanbieter sollten Ihren Code schreiben, damit er kompiliert werden kann, unabhängig davon, ob er Unicode unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-110">All service providers should write their code so that they can compile regardless of whether or not they support Unicode.</span></span> <span data-ttu-id="9dd9b-111">Clients können abhängig von der jeweiligen Supportstufe bedingt kompiliert werden, jedoch nicht von Dienstanbietern.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-111">Clients compile conditionally, depending on their level of support, but service providers do not.</span></span> <span data-ttu-id="9dd9b-112">Sie sollten nicht neu kompiliert werden, wenn sich der Zeichensatz ändert.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-112">They should not have to be recompiled when the character set changes.</span></span> <span data-ttu-id="9dd9b-113">Nichts in Dienstanbieter Code sollte abhängig sein.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-113">Nothing in service provider code should be conditional.</span></span> 
  
<span data-ttu-id="9dd9b-114">Wenn Clients oder Dienstanbieter, die Unicode unterstützen, einen Methodenaufruf durchführen, der Zeichenfolgen als Eingabe-oder Ausgabeparameter enthält, legen Sie das MAPI_UNICODE-Flag fest.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-114">When clients or service providers that support Unicode make a method call that includes character strings as input or output parameters, they set the MAPI_UNICODE flag.</span></span> <span data-ttu-id="9dd9b-115">Das Festlegen dieses Flags gibt an, dass alle eingehenden Zeichenfolgen Unicode-Zeichenfolgen sind.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-115">Setting this flag indicates to the implementation that all incoming strings are Unicode strings.</span></span> <span data-ttu-id="9dd9b-116">Bei der Ausgabe fordert das Festlegen dieses Flags, dass alle Zeichenfolgen, die von der Implementierung zurückgegeben werden, nach Möglichkeit Unicode-Zeichenfolgen sein sollten.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-116">On output, setting this flag requests that all strings passed back from the implementation should be Unicode strings if possible.</span></span> <span data-ttu-id="9dd9b-117">Methoden Implementierer, die Unicode unterstützen, erfüllen die Anforderung; Methoden Implementierer, die keine Unicode-Unterstützung bereitstellen, werden nicht erfüllt.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-117">Method implementers that support Unicode will comply with the request; method implementers that do not provide Unicode support will not comply.</span></span> <span data-ttu-id="9dd9b-118">Zeichenfolgeneigenschaften, die nicht im Unicode-Format vorliegen, sind vom Typ PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-118">String properties that are not in Unicode format are of type PT_STRING8.</span></span>
  
<span data-ttu-id="9dd9b-119">MAPI definiert die **fMapiUnicode** -Konstante in der Headerdatei MAPIDEFS. H zur Darstellung des Standardzeichensatz.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-119">MAPI defines the **fMapiUnicode** constant in the header file MAPIDEFS.H to represent the default character set.</span></span> <span data-ttu-id="9dd9b-120">Wenn ein Client oder Dienstanbieter Unicode unterstützt, wird **fMapiUnicode** auf MAPI_UNICODE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-120">If a client or service provider supports Unicode, **fMapiUnicode** is set to MAPI_UNICODE.</span></span> <span data-ttu-id="9dd9b-121">Clients und Dienstanbieter, die den Unicode-Satz **fMapiUnicode** nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-121">Clients and service providers that do not support Unicode set **fMapiUnicode** to zero.</span></span> 
  
<span data-ttu-id="9dd9b-122">Dienstanbieter, die Unicode nicht unterstützen, sollten:</span><span class="sxs-lookup"><span data-stu-id="9dd9b-122">Service providers that do not support Unicode should:</span></span>
  
- <span data-ttu-id="9dd9b-123">Weigern Sie sich, Konvertierungen zwischen Zeichensätzen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-123">Refuse to perform conversions between character sets.</span></span>
    
- <span data-ttu-id="9dd9b-124">Führen Sie das MAPI_UNICODE-Flag nie in Methoden aufrufen weiter.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-124">Never pass the MAPI_UNICODE flag in method calls.</span></span>
    
- <span data-ttu-id="9dd9b-125">Gibt MAPI_E_BAD_CHARWIDTH zurück, wenn das MAPI_UNICODE-Flag übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-125">Return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is passed in.</span></span>
    
- <span data-ttu-id="9dd9b-126">Deklarieren Sie die ANSI-Zeichenfolgeneigenschaften explizit.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-126">Declare ANSI string properties explicitly.</span></span> 
    
<span data-ttu-id="9dd9b-127">Dienstanbieter können auch MAPI_E_BAD_CHARWIDTH zurückgeben, wenn Sie nur Unicode unterstützen und Clients das MAPI_UNICODE-Flag nicht bestehen.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-127">Service providers can also return MAPI_E_BAD_CHARWIDTH when they only support Unicode and clients do not pass the MAPI_UNICODE flag.</span></span> 
  
 <span data-ttu-id="9dd9b-128">Die aktuelle Version von MAPI unterstützt Unicode in den folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="9dd9b-128">The current version of MAPI supports Unicode in the following methods:</span></span> 
  
[<span data-ttu-id="9dd9b-129">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="9dd9b-129">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="9dd9b-130">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="9dd9b-130">IAddrBook::CreateOneOff</span></span>](iaddrbook-createoneoff.md)
  
[<span data-ttu-id="9dd9b-131">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="9dd9b-131">IAddrBook::Details</span></span>](iaddrbook-details.md)
  
[<span data-ttu-id="9dd9b-132">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="9dd9b-132">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
<span data-ttu-id="9dd9b-133">[IMAPIProp:: getlasterroraufzurufen](imapiprop-getlasterror.md) (Nur**IAddrBook** -Implementierung)</span><span class="sxs-lookup"><span data-stu-id="9dd9b-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**IAddrBook** implementation only)</span></span> 
  
<span data-ttu-id="9dd9b-134">Für diese Methoden können Aufrufer davon ausgehen, dass zurückgegebene Zeichenfolgen Unicode-Zeichenfolgen sein.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-134">For these methods, callers can expect any returned strings to be Unicode strings.</span></span> <span data-ttu-id="9dd9b-135">Zeichenfolgen, die von MAPI-Implementierungen anderer Methoden zurückgegeben werden, sind ANSI-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="9dd9b-135">Character strings returned from MAPI implementations of any other method will be ANSI character strings.</span></span>
  

