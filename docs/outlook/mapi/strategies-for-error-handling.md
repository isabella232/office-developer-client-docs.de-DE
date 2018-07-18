---
title: Strategien zur Fehlerbehandlung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e778df216d0fe9b901cd9f7136c8014a6b8f0d0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795637"
---
# <a name="strategies-for-error-handling"></a><span data-ttu-id="1b528-103">Strategien zur Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="1b528-103">Strategies for Error Handling</span></span>

  
  
<span data-ttu-id="1b528-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1b528-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1b528-105">Da Schnittstellenmethoden virtuellen sind, ist es nicht möglich, als ein Anrufer den vollständigen Satz von Werten kennen, die von jeder einen Aufruf zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="1b528-105">Because interface methods are virtual, it is not possible to know, as a caller, the full set of values that can be returned from any one call.</span></span> <span data-ttu-id="1b528-106">Eine Implementierung einer Methode möglicherweise fünf Werte zurück. eine andere möglicherweise acht zurück.</span><span class="sxs-lookup"><span data-stu-id="1b528-106">One implementation of a method might return five values; another might return eight.</span></span> <span data-ttu-id="1b528-107">Die Einträge Verweis in der Dokumentation zu MAPI-einige Werte aufgeführt, die für jede Methode zurückgegeben werden können; Dies sind die Werte, die der Client oder Dienstanbieter suchen und verarbeiten, da sie eine besondere Bedeutung haben kann.</span><span class="sxs-lookup"><span data-stu-id="1b528-107">The reference entries in the MAPI documentation list a few values that can be returned for each method; these are the values that your client or service provider can check for and handle because they have special meanings.</span></span> <span data-ttu-id="1b528-108">Andere Werte zurückgegeben werden können, aber, da sie nicht aussagekräftig sind, ist die Behandlung von spezieller Code nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1b528-108">Other values can be returned, but because they are not meaningful, special code to handle those is not necessary.</span></span> <span data-ttu-id="1b528-109">Eine einfache Überprüfung Erfolg oder Fehler ist ausreichend.</span><span class="sxs-lookup"><span data-stu-id="1b528-109">A simple check for success or failure is adequate.</span></span>
  
<span data-ttu-id="1b528-110">Wenige-Schnittstellenmethoden zurückgeben Warnungen.</span><span class="sxs-lookup"><span data-stu-id="1b528-110">A few of the interface methods return warnings.</span></span> <span data-ttu-id="1b528-111">Wenn eine Methode, die der Client oder Dienstanbieter Ruft eine Warnung zurückgeben kann, verwenden Sie das Makro **HR_FAILED** So testen Sie den Rückgabewert statt eine Überprüfung für 0 (null) oder ungleich NULL.</span><span class="sxs-lookup"><span data-stu-id="1b528-111">If a method that your client or service provider calls can return a warning, use the **HR_FAILED** macro to test the return value rather than a check for zero or nonzero.</span></span> <span data-ttu-id="1b528-112">Warnungen, unterscheiden sich zwar ungleich NULL, von Fehlercodes, dass sie nicht das hohe Bit festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="1b528-112">Warnings, although nonzero, differ from error codes in that they do not have the high bit set.</span></span> <span data-ttu-id="1b528-113">Wenn der Client oder Dienstanbieter nicht das Makro verwendet wird, ist es wahrscheinlich, dass eine Warnung für ein Fehler gehalten werden kann.</span><span class="sxs-lookup"><span data-stu-id="1b528-113">If your client or service provider does not use the macro, it is likely that a warning might be mistaken for a failure.</span></span> 
  
<span data-ttu-id="1b528-114">Zwar die meisten Interface-Methoden und Funktionen HRESULT-Werte zurückgeben, Rückgabewerte einige Funktionen, die nicht signierte lang.</span><span class="sxs-lookup"><span data-stu-id="1b528-114">Although most interface methods and functions return HRESULT values, some functions return unsigned long values.</span></span> <span data-ttu-id="1b528-115">Darüber hinaus einige Methoden in der MAPI-Umgebung verwendet stammen aus COM und COM-Fehlerwerte statt MAPI-Fehlerwerte zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="1b528-115">Also, some methods used in the MAPI environment come from COM and return COM error values rather than MAPI error values.</span></span> <span data-ttu-id="1b528-116">Beachten behalten Sie die folgenden Richtlinien beim erachtet bei:</span><span class="sxs-lookup"><span data-stu-id="1b528-116">Keep in mind the following guidelines when making calls:</span></span>
  
- <span data-ttu-id="1b528-117">Niemals, oder verwenden Sie die Rückgabewerte von **IUnknown:: AddRef** oder **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="1b528-117">Never rely on or use the return values from **IUnknown::AddRef** or **IUnknown::Release**.</span></span> <span data-ttu-id="1b528-118">Diese zurückgegebenen Werte sind nur zu Diagnosezwecken.</span><span class="sxs-lookup"><span data-stu-id="1b528-118">These return values are for diagnostic purposes only.</span></span> 
    
- <span data-ttu-id="1b528-119">**QueryInterface** gibt immer generischen COM-Fehler, in dem die Funktion FACILITY_NULL oder FACILITY_RPC wird, statt der MAPI-Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="1b528-119">**IUnknown::QueryInterface** always returns generic COM errors where the facility is FACILITY_NULL or FACILITY_RPC, rather than MAPI errors.</span></span> 
    
- <span data-ttu-id="1b528-120">Alle anderen Schnittstellenmethoden zurückgeben MAPI-Benutzeroberflächenfehler mit einer Funktion des FACILITY_ITF oder FACILITY_RPC oder FACILITY_NULL Fehler.</span><span class="sxs-lookup"><span data-stu-id="1b528-120">All other interface methods return MAPI interface errors with a facility of FACILITY_ITF, or FACILITY_RPC or FACILITY_NULL errors.</span></span>
    
<span data-ttu-id="1b528-121">Wenn eine nicht unterstützte MAPI-Methode aufgerufen wird, kann eine der vier mögliche Fehler zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="1b528-121">When a call is made to an unsupported MAPI method, one of four possible errors can be returned:</span></span> 
  
<span data-ttu-id="1b528-122">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="1b528-122">MAPI_E_NO_SUPPORT</span></span>
  
<span data-ttu-id="1b528-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="1b528-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span>
  
<span data-ttu-id="1b528-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1b528-124">MAPI_E_INVALID_PARAMETER</span></span>
  
<span data-ttu-id="1b528-125">MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="1b528-125">MAPI_E_VERSION.</span></span> 
  

