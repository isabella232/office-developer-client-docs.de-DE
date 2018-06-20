---
title: Registrieren von Service Provider eindeutige Bezeichner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 80d2e4fd353f0746349563fd911e0af09a658b35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795360"
---
# <a name="registering-service-provider-unique-identifiers"></a><span data-ttu-id="29218-103">Registrieren von Service Provider eindeutige Bezeichner</span><span class="sxs-lookup"><span data-stu-id="29218-103">Registering Service Provider Unique Identifiers</span></span>

  
  
<span data-ttu-id="29218-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="29218-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="29218-105">Adressbuch, Nachrichtenspeicher und Transportanbieter führen einen eindeutigen Bezeichner, der als ein [MAPIUID](mapiuid.md) bezeichnet, um auf Serviceobjekte der verschiedenen Typen registrieren.</span><span class="sxs-lookup"><span data-stu-id="29218-105">Address book, message store, and transport providers use a unique identifier known as a [MAPIUID](mapiuid.md) to register to service objects of various types.</span></span> <span data-ttu-id="29218-106">Ein **MAPIUID** ist ein 16-Byte-Bezeichner, der eine GUID enthält.</span><span class="sxs-lookup"><span data-stu-id="29218-106">A **MAPIUID** is a 16-byte identifier that contains a GUID.</span></span> <span data-ttu-id="29218-107">Sie können eine **MAPIUID** mithilfe des folgenden Verfahrens erstellen:</span><span class="sxs-lookup"><span data-stu-id="29218-107">You can create a **MAPIUID** by using the following procedure:</span></span> 
  
1. <span data-ttu-id="29218-108">Definieren Sie eine Konstante.</span><span class="sxs-lookup"><span data-stu-id="29218-108">Define a constant.</span></span>
    
2. <span data-ttu-id="29218-109">Rufen Sie die Visual Studio-*GUID erstellen*\* Tool.</span><span class="sxs-lookup"><span data-stu-id="29218-109">Invoke the Visual Studio*Create GUID*\* tool.</span></span> 
    
<span data-ttu-id="29218-110">Adressbuch-Dienstanbieter möglicherweise beispielsweise die folgenden Konstanten in einer Headerdatei zum Definieren einer **MAPIUID**enthalten:</span><span class="sxs-lookup"><span data-stu-id="29218-110">For example, an address book provider might include the following constant in a header file to define a **MAPIUID**:</span></span>
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 <span data-ttu-id="29218-111">**Eine MAPIUID registriert, wenn der Anbieter einen Address Book oder einer Nachricht-Anbieter ist**</span><span class="sxs-lookup"><span data-stu-id="29218-111">**To register a MAPIUID if your provider is an address book or message store provider**</span></span>
  
1. <span data-ttu-id="29218-112">Rufen Sie [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span><span class="sxs-lookup"><span data-stu-id="29218-112">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
    
2. <span data-ttu-id="29218-113">Registrieren einer **MAPIUID** für die einzelnen Anmeldung Objekt zurück, das Sie instanziieren, und Schließen dieses **MAPIUID** in den ersten 16 Byte des Elements **Ab** der jedes Eintrags-ID, die Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="29218-113">Register a **MAPIUID** for each logon object that you instantiate and include this **MAPIUID** in the first 16 bytes of the **ab** member of every entry identifier that you create.</span></span> <span data-ttu-id="29218-114">MAPI verwendet **MAPIUID** Strukturen Dienstanbieter Objekte zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="29218-114">MAPI uses **MAPIUID** structures to associate objects with service providers.</span></span> <span data-ttu-id="29218-115">Wenn ein Client aufruft, dass die [IMAPISession::OpenEntry](imapisession-openentry.md) -Methode zum Öffnen eines Objekts, MAPI den **MAPIUID** Teil des Bezeichners Eintrag untersucht, sollte anschließendem Abgleich mit der registrierten **MAPIUID**, zu bestimmen, welches Objekt Anmeldung öffnen erhalten Anforderung.</span><span class="sxs-lookup"><span data-stu-id="29218-115">When a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open an object, MAPI examines the **MAPIUID** portion of the entry identifier, matching it against the registered **MAPIUID**, to determine which logon object should receive the open request.</span></span>
    
3. <span data-ttu-id="29218-116">Wenn der Anbieter einen Transport ist, registrieren Sie ein oder mehrere **MAPIUID** Strukturen, wenn MAPI Ihrer **IXPLogon::AddressTypes** -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="29218-116">If your provider is a transport, register one or more **MAPIUID** structures when MAPI calls your **IXPLogon::AddressTypes** method.</span></span> <span data-ttu-id="29218-117">MAPI verwendet die vom Transportanbieter für registriert **MAPIUID** Strukturen, die Verantwortung für die Nachrichtenübermittlung zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="29218-117">MAPI uses the **MAPIUID** structures registered by transport providers to assign responsibility for message delivery.</span></span> 
    
<span data-ttu-id="29218-118">Obwohl-Dienstanbieter in der Regel ein einzelnes **MAPIUID**registrieren, können Sie mehrere **MAPIUID** Strukturen registrieren.</span><span class="sxs-lookup"><span data-stu-id="29218-118">Although service providers typically register a single **MAPIUID**, you can register multiple **MAPIUID** structures.</span></span> <span data-ttu-id="29218-119">Wenn Ihr Adressbuch oder die Nachricht vom Anbieter unterstützt mehrere Logon-Objekten, möglicherweise speichern Anwesenheitsebene einen Benutzer mehr als eine Instanz des Anbieters zu deren Profil hinzufügen, möchten Sie möglicherweise eine unterschiedliche **MAPIUID** für jedes Objekt Anmeldung zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="29218-119">If your address book or message store provider supports multiple logon objects, perhaps by permitting a user to add more than one instance of your provider to their profile, you might want to implement a different **MAPIUID** for each logon object.</span></span> <span data-ttu-id="29218-120">Es gibt einige andere Gründe zur Unterstützung von mehr als eine **MAPIUID**:</span><span class="sxs-lookup"><span data-stu-id="29218-120">There are a few other reasons to support more than one **MAPIUID**:</span></span>
  
- <span data-ttu-id="29218-121">Sie müssen mehr als eine Version des Anbieters unterstützen, und die Eintragsbezeichner müssen die entsprechende Version darstellen.</span><span class="sxs-lookup"><span data-stu-id="29218-121">You must support more than one version of your provider and the entry identifiers must represent the appropriate version.</span></span> <span data-ttu-id="29218-122">Zuweisen einer anderen **MAPIUID** für jede Version.</span><span class="sxs-lookup"><span data-stu-id="29218-122">Assign a different **MAPIUID** for each version.</span></span> 
    
- <span data-ttu-id="29218-123">Unterscheiden zwischen den Typen von Objekten, die Sie unterstützen möchten.</span><span class="sxs-lookup"><span data-stu-id="29218-123">You want to distinguish between the types of objects you support.</span></span> <span data-ttu-id="29218-124">Beispielsweise möchten ein Adressbuchanbieter Registrieren einer **MAPIUID** in der Eintragsbezeichner seiner messaging User-Objekte verwenden und eine unterschiedliche **MAPIUID** für Verteilerlisten verwenden.</span><span class="sxs-lookup"><span data-stu-id="29218-124">For example, an address book provider might want to register one **MAPIUID** to use in the entry identifiers of its messaging user objects and a different **MAPIUID** to use for distribution lists.</span></span> 
    
<span data-ttu-id="29218-125">Wenn mehrere Logon-Objekten, die gleichzeitig aktiv sind vorhanden sind, ist es sinnvoll, die jeweils eindeutige **MAPIUID** -Strukturen haben.</span><span class="sxs-lookup"><span data-stu-id="29218-125">When there are multiple logon objects that are concurrently active, it makes sense to have unique **MAPIUID** structures for each one.</span></span> <span data-ttu-id="29218-126">Dadurch wird die Genauigkeit, mit der MAPI entspricht-Eintragsbezeichner Dienstanbietern und erspart einige, erhöht.</span><span class="sxs-lookup"><span data-stu-id="29218-126">This increases the accuracy with which MAPI matches entry identifiers to service providers and saves some work.</span></span> <span data-ttu-id="29218-127">Bei jeder Anmeldung-Objekt eine eigene eindeutige ID besitzt, MAPI kann zu gewährleisten, dass alle anfordern Routen zu einem Anmeldeobjekt können durch dieses Objekt behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="29218-127">When every logon object has its own unique identifier, MAPI can guarantee that any request it routes to a logon object can be handled by that object.</span></span> <span data-ttu-id="29218-128">Wenn Logon-Objekten **MAPIUID** Strukturen freigeben, leitet MAPI die Anforderung auf der ersten Anmeldung-Objekt, das durch die **MAPIUID**identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="29218-128">When logon objects share **MAPIUID** structures, MAPI routes the request to the first logon object that is identified by the **MAPIUID**.</span></span> <span data-ttu-id="29218-129">Wenn eine der Logon-Objekten eine Anforderung, die nicht verarbeitet werden kann empfängt, da die Eintrags-ID nicht bearbeitet werden kann, übergeben Sie die Anforderung an die nächste Anmeldung-Objekt vor der Rückgabe eines Fehlers.</span><span class="sxs-lookup"><span data-stu-id="29218-129">If one of your logon objects receives a request that it cannot process because it does not handle the entry identifier, pass the request on to your next logon object before returning an error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="29218-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29218-130">See also</span></span>



[<span data-ttu-id="29218-131">Implementieren von Service Provider Anmeldung</span><span class="sxs-lookup"><span data-stu-id="29218-131">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

