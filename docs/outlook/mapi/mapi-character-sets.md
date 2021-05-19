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
# <a name="mapi-character-sets"></a><span data-ttu-id="2bd48-103">MAPI-Zeichensätze</span><span class="sxs-lookup"><span data-stu-id="2bd48-103">MAPI Character Sets</span></span>

  
  
<span data-ttu-id="2bd48-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2bd48-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2bd48-105">MAPI-konforme Clientanwendungen und Dienstanbieter können ANSI-Zeichen (einzelnes Byte) oder Unicode-Zeichen (Doppel-Byte) verwenden.</span><span class="sxs-lookup"><span data-stu-id="2bd48-105">MAPI-compliant client applications and service providers can use ANSI characters (single byte) or Unicode characters (double byte).</span></span> <span data-ttu-id="2bd48-106">OEM-Zeichensätze werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2bd48-106">OEM character sets are not supported.</span></span> <span data-ttu-id="2bd48-107">Eine an eine MAPI-Methode oder -Funktion übergebene OEM-Zeichenfolge verursacht einen Fehler bei dieser Methode oder Funktion.</span><span class="sxs-lookup"><span data-stu-id="2bd48-107">An OEM string passed to a MAPI method or function will cause that method or function to fail.</span></span> <span data-ttu-id="2bd48-108">Clientanwendungen, die mit Dateinamen im OEM-Zeichensatz arbeiten, müssen darauf achten, sie in ANSI zu konvertieren, bevor sie an eine MAPI-Methode oder -Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="2bd48-108">Client applications that work with filenames in the OEM character set must be careful to convert them to ANSI before passing them to a MAPI method or function.</span></span>
  
<span data-ttu-id="2bd48-109">Die Unterstützung des Unicode-Zeichensatz ist optional, sowohl für Clients als auch für Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="2bd48-109">Supporting the Unicode character set is optional, both for clients and service providers.</span></span> <span data-ttu-id="2bd48-110">Alle Dienstanbieter sollten ihren Code schreiben, damit sie kompilieren können, unabhängig davon, ob sie Unicode unterstützen oder nicht.</span><span class="sxs-lookup"><span data-stu-id="2bd48-110">All service providers should write their code so that they can compile regardless of whether or not they support Unicode.</span></span> <span data-ttu-id="2bd48-111">Clients kompilieren abhängig von ihrer Supportstufe bedingt, Dienstanbieter jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="2bd48-111">Clients compile conditionally, depending on their level of support, but service providers do not.</span></span> <span data-ttu-id="2bd48-112">Sie sollten nicht neu kompiliert werden müssen, wenn sich der Zeichensatz ändert.</span><span class="sxs-lookup"><span data-stu-id="2bd48-112">They should not have to be recompiled when the character set changes.</span></span> <span data-ttu-id="2bd48-113">Nichts im Dienstanbietercode sollte bedingt sein.</span><span class="sxs-lookup"><span data-stu-id="2bd48-113">Nothing in service provider code should be conditional.</span></span> 
  
<span data-ttu-id="2bd48-114">Wenn Clients oder Dienstanbieter, die Unicode unterstützen, einen Methodenaufruf mit Zeichenzeichenfolgen als Eingabe- oder Ausgabeparameter erstellen, legen sie das MAPI_UNICODE fest.</span><span class="sxs-lookup"><span data-stu-id="2bd48-114">When clients or service providers that support Unicode make a method call that includes character strings as input or output parameters, they set the MAPI_UNICODE flag.</span></span> <span data-ttu-id="2bd48-115">Wenn Sie dieses Flag festlegen, wird für die Implementierung angegeben, dass alle eingehenden Zeichenfolgen Unicode-Zeichenfolgen sind.</span><span class="sxs-lookup"><span data-stu-id="2bd48-115">Setting this flag indicates to the implementation that all incoming strings are Unicode strings.</span></span> <span data-ttu-id="2bd48-116">Bei der Ausgabe fordert das Festlegen dieses Kennzeichens, dass alle von der Implementierung übergebenen Zeichenfolgen möglichst Unicode-Zeichenfolgen sein sollen.</span><span class="sxs-lookup"><span data-stu-id="2bd48-116">On output, setting this flag requests that all strings passed back from the implementation should be Unicode strings if possible.</span></span> <span data-ttu-id="2bd48-117">Methoden implementierer, die Unicode unterstützen, entsprechen der Anforderung. methoden implementers that do not provide Unicode support will not comply.</span><span class="sxs-lookup"><span data-stu-id="2bd48-117">Method implementers that support Unicode will comply with the request; method implementers that do not provide Unicode support will not comply.</span></span> <span data-ttu-id="2bd48-118">Zeichenfolgeneigenschaften, die nicht im Unicode-Format vorliegen, sind vom Typ PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="2bd48-118">String properties that are not in Unicode format are of type PT_STRING8.</span></span>
  
<span data-ttu-id="2bd48-119">MAPI definiert die **fMapiUnicode-Konstante** in der Headerdatei MAPIDEFS. H, um den Standardzeichensatz zu repräsentieren.</span><span class="sxs-lookup"><span data-stu-id="2bd48-119">MAPI defines the **fMapiUnicode** constant in the header file MAPIDEFS.H to represent the default character set.</span></span> <span data-ttu-id="2bd48-120">Wenn ein Client oder Dienstanbieter Unicode unterstützt, **wird fMapiUnicode** auf MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="2bd48-120">If a client or service provider supports Unicode, **fMapiUnicode** is set to MAPI_UNICODE.</span></span> <span data-ttu-id="2bd48-121">Clients und Dienstanbieter, die Unicode nicht unterstützen, **legen fMapiUnicode auf** Null fest.</span><span class="sxs-lookup"><span data-stu-id="2bd48-121">Clients and service providers that do not support Unicode set **fMapiUnicode** to zero.</span></span> 
  
<span data-ttu-id="2bd48-122">Dienstanbieter, die Unicode nicht unterstützen, sollten:</span><span class="sxs-lookup"><span data-stu-id="2bd48-122">Service providers that do not support Unicode should:</span></span>
  
- <span data-ttu-id="2bd48-123">Konvertierungen zwischen Zeichensätzen verweigern.</span><span class="sxs-lookup"><span data-stu-id="2bd48-123">Refuse to perform conversions between character sets.</span></span>
    
- <span data-ttu-id="2bd48-124">Übergeben Sie das MAPI_UNICODE in Methodenaufrufen nie.</span><span class="sxs-lookup"><span data-stu-id="2bd48-124">Never pass the MAPI_UNICODE flag in method calls.</span></span>
    
- <span data-ttu-id="2bd48-125">Gibt MAPI_E_BAD_CHARWIDTH zurück, wenn das MAPI_UNICODE übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2bd48-125">Return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is passed in.</span></span>
    
- <span data-ttu-id="2bd48-126">Deklarieren Sie die Eigenschaften der ANSI-Zeichenfolge explizit.</span><span class="sxs-lookup"><span data-stu-id="2bd48-126">Declare ANSI string properties explicitly.</span></span> 
    
<span data-ttu-id="2bd48-127">Dienstanbieter können auch MAPI_E_BAD_CHARWIDTH zurückgeben, wenn sie nur Unicode unterstützen und Clients das MAPI_UNICODE übergeben.</span><span class="sxs-lookup"><span data-stu-id="2bd48-127">Service providers can also return MAPI_E_BAD_CHARWIDTH when they only support Unicode and clients do not pass the MAPI_UNICODE flag.</span></span> 
  
 <span data-ttu-id="2bd48-128">Die aktuelle Version von MAPI unterstützt Unicode in den folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="2bd48-128">The current version of MAPI supports Unicode in the following methods:</span></span> 
  
[<span data-ttu-id="2bd48-129">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="2bd48-129">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="2bd48-130">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="2bd48-130">IAddrBook::CreateOneOff</span></span>](iaddrbook-createoneoff.md)
  
[<span data-ttu-id="2bd48-131">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="2bd48-131">IAddrBook::Details</span></span>](iaddrbook-details.md)
  
[<span data-ttu-id="2bd48-132">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="2bd48-132">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
<span data-ttu-id="2bd48-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**nur IAddrBook-Implementierung)**</span><span class="sxs-lookup"><span data-stu-id="2bd48-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**IAddrBook** implementation only)</span></span> 
  
<span data-ttu-id="2bd48-134">Für diese Methoden können Aufrufer erwarten, dass alle zurückgegebenen Zeichenfolgen Unicode-Zeichenfolgen sind.</span><span class="sxs-lookup"><span data-stu-id="2bd48-134">For these methods, callers can expect any returned strings to be Unicode strings.</span></span> <span data-ttu-id="2bd48-135">Zeichenzeichenfolgen, die von MAPI-Implementierungen einer anderen Methode zurückgegeben werden, sind ANSI-Zeichenzeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="2bd48-135">Character strings returned from MAPI implementations of any other method will be ANSI character strings.</span></span>
  

