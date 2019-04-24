---
title: Strategien für die Fehlerbehandlung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9e76ae3f292d8348b9dc64cb54bffae96b96e871
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327216"
---
# <a name="strategies-for-error-handling"></a><span data-ttu-id="20ec0-103">Strategien für die Fehlerbehandlung</span><span class="sxs-lookup"><span data-stu-id="20ec0-103">Strategies for Error Handling</span></span>

  
  
<span data-ttu-id="20ec0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20ec0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20ec0-105">Da Schnittstellenmethoden virtuell sind, ist es nicht möglich, als Anrufer den vollständigen Satz von Werten zu kennen, die von einem beliebigen Aufruf zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="20ec0-105">Because interface methods are virtual, it is not possible to know, as a caller, the full set of values that can be returned from any one call.</span></span> <span data-ttu-id="20ec0-106">Eine Implementierung einer Methode kann fünf Werte zurückgeben. eine andere kann acht zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="20ec0-106">One implementation of a method might return five values; another might return eight.</span></span> <span data-ttu-id="20ec0-107">In den Referenz Einträgen in der MAPI-Dokumentation werden einige Werte aufgeführt, die für jede Methode zurückgegeben werden können. Dies sind die Werte, die Ihr Client oder Dienstanbieter überprüfen und behandeln kann, da diese eine besondere Bedeutung haben.</span><span class="sxs-lookup"><span data-stu-id="20ec0-107">The reference entries in the MAPI documentation list a few values that can be returned for each method; these are the values that your client or service provider can check for and handle because they have special meanings.</span></span> <span data-ttu-id="20ec0-108">Andere Werte können zurückgegeben werden, da Sie jedoch keine Bedeutung haben, ist kein spezieller Code erforderlich, um diese zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="20ec0-108">Other values can be returned, but because they are not meaningful, special code to handle those is not necessary.</span></span> <span data-ttu-id="20ec0-109">Eine einfache Überprüfung auf Erfolg oder Misserfolg ist ausreichend.</span><span class="sxs-lookup"><span data-stu-id="20ec0-109">A simple check for success or failure is adequate.</span></span>
  
<span data-ttu-id="20ec0-110">Einige der Schnittstellenmethoden geben Warnungen zurück.</span><span class="sxs-lookup"><span data-stu-id="20ec0-110">A few of the interface methods return warnings.</span></span> <span data-ttu-id="20ec0-111">Wenn eine vom Client oder Dienstanbieter aufgerufene Methode eine Warnung zurückgeben kann, verwenden Sie das **HR_FAILED** -Makro, um den Rückgabewert zu testen, statt eine Überprüfung auf 0 (null) oder ungleich NULL.</span><span class="sxs-lookup"><span data-stu-id="20ec0-111">If a method that your client or service provider calls can return a warning, use the **HR_FAILED** macro to test the return value rather than a check for zero or nonzero.</span></span> <span data-ttu-id="20ec0-112">Warnungen, obwohl ungleich NULL, unterscheiden sich von Fehlercodes dadurch, dass Sie nicht das hohe Bit festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="20ec0-112">Warnings, although nonzero, differ from error codes in that they do not have the high bit set.</span></span> <span data-ttu-id="20ec0-113">Wenn Ihr Client oder Dienstanbieter das Makro nicht verwendet, ist es wahrscheinlich, dass für einen Fehler eine Warnung verwechselt wird.</span><span class="sxs-lookup"><span data-stu-id="20ec0-113">If your client or service provider does not use the macro, it is likely that a warning might be mistaken for a failure.</span></span> 
  
<span data-ttu-id="20ec0-114">Obwohl die meisten Schnittstellenmethoden und-Funktionen HRESULT-Werte zurückgeben, geben einige Funktionen unsigned long-Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="20ec0-114">Although most interface methods and functions return HRESULT values, some functions return unsigned long values.</span></span> <span data-ttu-id="20ec0-115">Außerdem stammen einige Methoden, die in der MAPI-Umgebung verwendet werden, aus COM und geben COM-Fehlerwerte anstelle von MAPI-Fehlerwerten zurück.</span><span class="sxs-lookup"><span data-stu-id="20ec0-115">Also, some methods used in the MAPI environment come from COM and return COM error values rather than MAPI error values.</span></span> <span data-ttu-id="20ec0-116">Beachten Sie beim tätigen von Anrufen die folgenden Richtlinien:</span><span class="sxs-lookup"><span data-stu-id="20ec0-116">Keep in mind the following guidelines when making calls:</span></span>
  
- <span data-ttu-id="20ec0-117">Verlassen Sie sich nie auf die Rückgabewerte von **IUnknown:: AddRef** oder **IUnknown:: Release**.</span><span class="sxs-lookup"><span data-stu-id="20ec0-117">Never rely on or use the return values from **IUnknown::AddRef** or **IUnknown::Release**.</span></span> <span data-ttu-id="20ec0-118">Diese Rückgabewerte dienen nur zu Diagnosezwecken.</span><span class="sxs-lookup"><span data-stu-id="20ec0-118">These return values are for diagnostic purposes only.</span></span> 
    
- <span data-ttu-id="20ec0-119">**IUnknown:: QueryInterface** gibt immer generische com-Fehler zurück, bei denen die FACILITY_NULL-oder FACILITY_RPC statt MAPI-Fehler aufweist.</span><span class="sxs-lookup"><span data-stu-id="20ec0-119">**IUnknown::QueryInterface** always returns generic COM errors where the facility is FACILITY_NULL or FACILITY_RPC, rather than MAPI errors.</span></span> 
    
- <span data-ttu-id="20ec0-120">Alle anderen Schnittstellenmethoden geben MAPI-Schnittstellenfehler mit einer FACILITY_ITF-oder FACILITY_RPC-oder FACILITY_NULL-Fehlermeldung zurück.</span><span class="sxs-lookup"><span data-stu-id="20ec0-120">All other interface methods return MAPI interface errors with a facility of FACILITY_ITF, or FACILITY_RPC or FACILITY_NULL errors.</span></span>
    
<span data-ttu-id="20ec0-121">Wenn ein Aufruf an eine nicht unterstützte MAPI-Methode erfolgt, kann einer von vier möglichen Fehlern zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="20ec0-121">When a call is made to an unsupported MAPI method, one of four possible errors can be returned:</span></span> 
  
<span data-ttu-id="20ec0-122">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="20ec0-122">MAPI_E_NO_SUPPORT</span></span>
  
<span data-ttu-id="20ec0-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="20ec0-123">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span>
  
<span data-ttu-id="20ec0-124">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="20ec0-124">MAPI_E_INVALID_PARAMETER</span></span>
  
<span data-ttu-id="20ec0-125">MAPI_E_VERSION.</span><span class="sxs-lookup"><span data-stu-id="20ec0-125">MAPI_E_VERSION.</span></span> 
  

