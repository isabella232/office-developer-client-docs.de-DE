---
title: Registrieren eindeutiger Bezeichner des Dienstanbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9f4acbb06f85a88a6c057da263ae95e09f72e0bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410175"
---
# <a name="registering-service-provider-unique-identifiers"></a><span data-ttu-id="97caf-103">Registrieren eindeutiger Bezeichner des Dienstanbieters</span><span class="sxs-lookup"><span data-stu-id="97caf-103">Registering Service Provider Unique Identifiers</span></span>

  
  
<span data-ttu-id="97caf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="97caf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="97caf-105">Adressbuch-, Nachrichtenspeicher- und Transportanbieter verwenden einen eindeutigen Bezeichner, der [als MAPIUID](mapiuid.md) bezeichnet wird, um sich bei Dienstobjekten verschiedener Typen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="97caf-105">Address book, message store, and transport providers use a unique identifier known as a [MAPIUID](mapiuid.md) to register to service objects of various types.</span></span> <span data-ttu-id="97caf-106">Eine **MAPIUID** ist eine 16-Byte-ID, die eine GUID enthält.</span><span class="sxs-lookup"><span data-stu-id="97caf-106">A **MAPIUID** is a 16-byte identifier that contains a GUID.</span></span> <span data-ttu-id="97caf-107">Sie können eine **MAPIUID mithilfe** des folgenden Verfahrens erstellen:</span><span class="sxs-lookup"><span data-stu-id="97caf-107">You can create a **MAPIUID** by using the following procedure:</span></span> 
  
1. <span data-ttu-id="97caf-108">Definieren Sie eine Konstante.</span><span class="sxs-lookup"><span data-stu-id="97caf-108">Define a constant.</span></span>
    
2. <span data-ttu-id="97caf-109">Rufen Sie das Visual Studio *GUID*\* erstellen auf.</span><span class="sxs-lookup"><span data-stu-id="97caf-109">Invoke the Visual Studio *Create GUID*\* tool.</span></span> 
    
<span data-ttu-id="97caf-110">Ein Adressbuchanbieter kann z. B. die folgende Konstante in einer Headerdatei enthalten, um eine **MAPIUID zu definieren:**</span><span class="sxs-lookup"><span data-stu-id="97caf-110">For example, an address book provider might include the following constant in a header file to define a **MAPIUID**:</span></span>
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 <span data-ttu-id="97caf-111">**So registrieren Sie eine MAPIUID, wenn Ihr Anbieter ein Adressbuch- oder Nachrichtenspeicheranbieter ist**</span><span class="sxs-lookup"><span data-stu-id="97caf-111">**To register a MAPIUID if your provider is an address book or message store provider**</span></span>
  
1. <span data-ttu-id="97caf-112">Rufen [Sie IMAPISupport::SetProviderUID auf.](imapisupport-setprovideruid.md)</span><span class="sxs-lookup"><span data-stu-id="97caf-112">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
    
2. <span data-ttu-id="97caf-113">Registrieren Sie **eine MAPIUID** für jedes Anmeldeobjekt, das Sie instanziieren, und fügen Sie diese **MAPIUID** in die ersten 16 Byte des **ab-Mitglieds** jedes Eintragsbezeichners ein, den Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="97caf-113">Register a **MAPIUID** for each logon object that you instantiate and include this **MAPIUID** in the first 16 bytes of the **ab** member of every entry identifier that you create.</span></span> <span data-ttu-id="97caf-114">MAPI verwendet **MAPIUID-Strukturen,** um Objekte Dienstanbietern zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="97caf-114">MAPI uses **MAPIUID** structures to associate objects with service providers.</span></span> <span data-ttu-id="97caf-115">Wenn ein Client die [IMAPISession::OpenEntry-Methode](imapisession-openentry.md) aufruft, um ein Objekt zu öffnen, untersucht MAPI den **MAPIUID-Teil** des Eintragsbezeichners und vergleicht ihn mit der registrierten **MAPIUID**, um zu bestimmen, welches Anmeldeobjekt die offene Anforderung empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="97caf-115">When a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open an object, MAPI examines the **MAPIUID** portion of the entry identifier, matching it against the registered **MAPIUID**, to determine which logon object should receive the open request.</span></span>
    
3. <span data-ttu-id="97caf-116">Wenn Ihr Anbieter ein Transport ist, registrieren Sie mindestens eine **MAPIUID-Struktur,** wenn MAPI Ihre **IXPLogon::AddressTypes-Methode** aufruft.</span><span class="sxs-lookup"><span data-stu-id="97caf-116">If your provider is a transport, register one or more **MAPIUID** structures when MAPI calls your **IXPLogon::AddressTypes** method.</span></span> <span data-ttu-id="97caf-117">MAPI verwendet die von Transportanbietern registrierten **MAPIUID-Strukturen,** um die Verantwortung für die Nachrichtenzustellung zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="97caf-117">MAPI uses the **MAPIUID** structures registered by transport providers to assign responsibility for message delivery.</span></span> 
    
<span data-ttu-id="97caf-118">Obwohl Dienstanbieter in der Regel eine einzelne **MAPIUID registrieren,** können Sie mehrere **MAPIUID-Strukturen** registrieren.</span><span class="sxs-lookup"><span data-stu-id="97caf-118">Although service providers typically register a single **MAPIUID**, you can register multiple **MAPIUID** structures.</span></span> <span data-ttu-id="97caf-119">Wenn Ihr Adressbuch- oder Nachrichtenspeicheranbieter mehrere Anmeldeobjekte unterstützt, z. B. indem ein Benutzer mehrere Instanzen Ihres Anbieters zu seinem Profil hinzufügen kann, sollten Sie für jedes Anmeldeobjekt eine andere **MAPIUID** implementieren.</span><span class="sxs-lookup"><span data-stu-id="97caf-119">If your address book or message store provider supports multiple logon objects, perhaps by permitting a user to add more than one instance of your provider to their profile, you might want to implement a different **MAPIUID** for each logon object.</span></span> <span data-ttu-id="97caf-120">Es gibt einige andere Gründe für die Unterstützung von mehr als einem **MAPIUID:**</span><span class="sxs-lookup"><span data-stu-id="97caf-120">There are a few other reasons to support more than one **MAPIUID**:</span></span>
  
- <span data-ttu-id="97caf-121">Sie müssen mehr als eine Version Ihres Anbieters unterstützen, und die Eintragsbezeichner müssen die entsprechende Version darstellen.</span><span class="sxs-lookup"><span data-stu-id="97caf-121">You must support more than one version of your provider and the entry identifiers must represent the appropriate version.</span></span> <span data-ttu-id="97caf-122">Weisen Sie für jede Version eine andere **MAPIUID** zu.</span><span class="sxs-lookup"><span data-stu-id="97caf-122">Assign a different **MAPIUID** for each version.</span></span> 
    
- <span data-ttu-id="97caf-123">Sie möchten zwischen den unterstützten Objekttypen unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="97caf-123">You want to distinguish between the types of objects you support.</span></span> <span data-ttu-id="97caf-124">Beispielsweise kann ein Adressbuchanbieter eine **MAPIUID** registrieren, die in den Eintragsbezeichnern seiner Messagingbenutzerobjekte verwendet werden soll, und eine andere **MAPIUID,** die für Verteilerlisten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="97caf-124">For example, an address book provider might want to register one **MAPIUID** to use in the entry identifiers of its messaging user objects and a different **MAPIUID** to use for distribution lists.</span></span> 
    
<span data-ttu-id="97caf-125">Wenn mehrere Anmeldeobjekte gleichzeitig aktiv sind, ist es sinnvoll, für jedes Objekt eindeutige **MAPIUID-Strukturen** zu haben.</span><span class="sxs-lookup"><span data-stu-id="97caf-125">When there are multiple logon objects that are concurrently active, it makes sense to have unique **MAPIUID** structures for each one.</span></span> <span data-ttu-id="97caf-126">Dadurch wird die Genauigkeit erhöht, mit der MAPI Eintragsbezeichnern zu Dienstanbietern entspricht, und es wird etwas Arbeit gespart.</span><span class="sxs-lookup"><span data-stu-id="97caf-126">This increases the accuracy with which MAPI matches entry identifiers to service providers and saves some work.</span></span> <span data-ttu-id="97caf-127">Wenn jedes Anmeldeobjekt über einen eigenen eindeutigen Bezeichner verfügt, kann MAPI garantieren, dass jede Anforderung, die es an ein Anmeldeobjekt weiter leitet, von diesem Objekt verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="97caf-127">When every logon object has its own unique identifier, MAPI can guarantee that any request it routes to a logon object can be handled by that object.</span></span> <span data-ttu-id="97caf-128">Wenn Anmeldeobjekte **MAPIUID-Strukturen** gemeinsam verwenden, leitet MAPI die Anforderung an das erste Anmeldeobjekt weiter, das durch die **MAPIUID identifiziert wird.**</span><span class="sxs-lookup"><span data-stu-id="97caf-128">When logon objects share **MAPIUID** structures, MAPI routes the request to the first logon object that is identified by the **MAPIUID**.</span></span> <span data-ttu-id="97caf-129">Wenn eines der Anmeldeobjekte eine Anforderung empfängt, die nicht verarbeiten kann, da die Eintrags-ID nicht verwendet wird, übergeben Sie die Anforderung an das nächste Anmeldeobjekt, bevor sie einen Fehler zurücksennen.</span><span class="sxs-lookup"><span data-stu-id="97caf-129">If one of your logon objects receives a request that it cannot process because it does not handle the entry identifier, pass the request on to your next logon object before returning an error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="97caf-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97caf-130">See also</span></span>



[<span data-ttu-id="97caf-131">Implementieren der Dienstanbieteranmeldung</span><span class="sxs-lookup"><span data-stu-id="97caf-131">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

