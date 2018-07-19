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
ms.openlocfilehash: 3f94823eb3f90ff9ac0f472a2de64e1904920d9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792960"
---
# <a name="mapi-character-sets"></a><span data-ttu-id="5964b-103">MAPI-Zeichensätze</span><span class="sxs-lookup"><span data-stu-id="5964b-103">MAPI Character Sets</span></span>

  
  
<span data-ttu-id="5964b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5964b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5964b-105">MAPI-kompatible Clientanwendungen und Dienstanbieter können ANSI-Zeichen (Einzelbyte) oder Unicode-Zeichen (Doppelbyte) verwenden.</span><span class="sxs-lookup"><span data-stu-id="5964b-105">MAPI-compliant client applications and service providers can use ANSI characters (single byte) or Unicode characters (double byte).</span></span> <span data-ttu-id="5964b-106">OEM-Zeichensätze werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5964b-106">OEM character sets are not supported.</span></span> <span data-ttu-id="5964b-107">OEM-Zeichenfolge an eine MAPI-Methode übergeben, oder Funktion bewirkt, dass diese Methode oder die Funktion ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="5964b-107">An OEM string passed to a MAPI method or function will cause that method or function to fail.</span></span> <span data-ttu-id="5964b-108">Clientanwendungen, die Dateinamen in der OEM-Zeichensatz entwickelt dürfen in ANSI umwandeln, bevor sie ein MAPI-Methode oder die Funktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="5964b-108">Client applications that work with filenames in the OEM character set must be careful to convert them to ANSI before passing them to a MAPI method or function.</span></span>
  
<span data-ttu-id="5964b-109">Mit der Unicode-Unterstützung ist Zeichensatz optional, sowohl für Clients und -Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="5964b-109">Supporting the Unicode character set is optional, both for clients and service providers.</span></span> <span data-ttu-id="5964b-110">Alle-Dienstanbieter sollte ihr Code geschrieben werden, damit sie kompilieren können, unabhängig davon, ob sie Unicode unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5964b-110">All service providers should write their code so that they can compile regardless of whether or not they support Unicode.</span></span> <span data-ttu-id="5964b-111">Clients bedingt, je nach ihrer Ebene der Unterstützung von kompilieren, Dienstanbieter jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="5964b-111">Clients compile conditionally, depending on their level of support, but service providers do not.</span></span> <span data-ttu-id="5964b-112">Sie sollten keine erneut kompiliert werden, wenn der Zeichensatz geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5964b-112">They should not have to be recompiled when the character set changes.</span></span> <span data-ttu-id="5964b-113">Nichts Service Provider Code sollte bedingte sein.</span><span class="sxs-lookup"><span data-stu-id="5964b-113">Nothing in service provider code should be conditional.</span></span> 
  
<span data-ttu-id="5964b-114">Bei Festlegung Clients oder Dienstanbieter, die Unicode-stellen einen Methodenaufruf unterstützen, der Zeichenfolgen als ein-oder Ausgabeparameter enthält sie die Option MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="5964b-114">When clients or service providers that support Unicode make a method call that includes character strings as input or output parameters, they set the MAPI_UNICODE flag.</span></span> <span data-ttu-id="5964b-115">Wenn Sie dieses Flag die Implementierung zeigt an, dass alle eingehende Zeichenfolgen Unicode-Zeichenfolgen werden.</span><span class="sxs-lookup"><span data-stu-id="5964b-115">Setting this flag indicates to the implementation that all incoming strings are Unicode strings.</span></span> <span data-ttu-id="5964b-116">Bei der Ausgabe sollte das Festlegen dieses Flag-Anforderungen, die alle Zeichenfolgen übergeben von der Implementierung zu sichern sein Unicode-Zeichenfolgen wenn möglich.</span><span class="sxs-lookup"><span data-stu-id="5964b-116">On output, setting this flag requests that all strings passed back from the implementation should be Unicode strings if possible.</span></span> <span data-ttu-id="5964b-117">Methode Implementierer, die Unicode unterstützen, werden die Anforderung entsprechen. Methode Implementierer, die keine Unicode-Unterstützung bieten werden nicht entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5964b-117">Method implementers that support Unicode will comply with the request; method implementers that do not provide Unicode support will not comply.</span></span> <span data-ttu-id="5964b-118">String-Eigenschaften, die nicht im Unicode-Format sind, sind vom Typ PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="5964b-118">String properties that are not in Unicode format are of type PT_STRING8.</span></span>
  
<span data-ttu-id="5964b-119">MAPI definiert die **fMapiUnicode** -Konstante in der Headerdatei MAPIDEFS. H, um den Standardzeichensatz darstellen.</span><span class="sxs-lookup"><span data-stu-id="5964b-119">MAPI defines the **fMapiUnicode** constant in the header file MAPIDEFS.H to represent the default character set.</span></span> <span data-ttu-id="5964b-120">Wenn ein Client oder Dienstanbieter Unicode unterstützt, wird auf Parameter MAPI_UNICODE **fMapiUnicode** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5964b-120">If a client or service provider supports Unicode, **fMapiUnicode** is set to MAPI_UNICODE.</span></span> <span data-ttu-id="5964b-121">**FMapiUnicode** festlegen auf NULL, Clients und Dienstanbieter, die Unicode nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5964b-121">Clients and service providers that do not support Unicode set **fMapiUnicode** to zero.</span></span> 
  
<span data-ttu-id="5964b-122">Dienstanbieter, die Unicode nicht unterstützen soll:</span><span class="sxs-lookup"><span data-stu-id="5964b-122">Service providers that do not support Unicode should:</span></span>
  
- <span data-ttu-id="5964b-123">Zum Durchführen von Konvertierungen zwischen Zeichensätzen ablehnen.</span><span class="sxs-lookup"><span data-stu-id="5964b-123">Refuse to perform conversions between character sets.</span></span>
    
- <span data-ttu-id="5964b-124">Übergeben Sie die Option MAPI_UNICODE nie-Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5964b-124">Never pass the MAPI_UNICODE flag in method calls.</span></span>
    
- <span data-ttu-id="5964b-125">MAPI_E_BAD_CHARWIDTH zurück, wenn die Option MAPI_UNICODE übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5964b-125">Return MAPI_E_BAD_CHARWIDTH when the MAPI_UNICODE flag is passed in.</span></span>
    
- <span data-ttu-id="5964b-126">Deklarieren Sie ANSI-Zeichenfolgeneigenschaften explizit.</span><span class="sxs-lookup"><span data-stu-id="5964b-126">Declare ANSI string properties explicitly.</span></span> 
    
<span data-ttu-id="5964b-127">Dienstanbieter können auch zurückgeben MAPI_E_BAD_CHARWIDTH, wenn sie nur Unicode- und -Clients unterstützen die Option MAPI_UNICODE nicht übergeben.</span><span class="sxs-lookup"><span data-stu-id="5964b-127">Service providers can also return MAPI_E_BAD_CHARWIDTH when they only support Unicode and clients do not pass the MAPI_UNICODE flag.</span></span> 
  
 <span data-ttu-id="5964b-128">Die aktuelle Version von MAPI unterstützt Unicode in den folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="5964b-128">The current version of MAPI supports Unicode in the following methods:</span></span> 
  
[<span data-ttu-id="5964b-129">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="5964b-129">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="5964b-130">IAddrBook::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="5964b-130">IAddrBook::CreateOneOff</span></span>](iaddrbook-createoneoff.md)
  
[<span data-ttu-id="5964b-131">IAddrBook::Details</span><span class="sxs-lookup"><span data-stu-id="5964b-131">IAddrBook::Details</span></span>](iaddrbook-details.md)
  
[<span data-ttu-id="5964b-132">IAddrBook::ResolveName</span><span class="sxs-lookup"><span data-stu-id="5964b-132">IAddrBook::ResolveName</span></span>](iaddrbook-resolvename.md)
  
<span data-ttu-id="5964b-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (Nur**IAddrBook** -Implementierung)</span><span class="sxs-lookup"><span data-stu-id="5964b-133">[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**IAddrBook** implementation only)</span></span> 
  
<span data-ttu-id="5964b-134">Für diese Methoden können Anrufer zurückgegebenen Zeichenfolgen Unicode-Zeichenfolgen zu erwarten.</span><span class="sxs-lookup"><span data-stu-id="5964b-134">For these methods, callers can expect any returned strings to be Unicode strings.</span></span> <span data-ttu-id="5964b-135">Von MAPI-Implementierungen von einer anderen Methode zurückgegebene Zeichenfolgen werden ANSI-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="5964b-135">Character strings returned from MAPI implementations of any other method will be ANSI character strings.</span></span>
  

