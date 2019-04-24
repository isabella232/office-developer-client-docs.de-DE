---
title: Registrieren von eindeutigen Bezeichnern des Dienstanbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 964fceb4-8a1c-46c1-98e1-a325c9259f8b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9f4acbb06f85a88a6c057da263ae95e09f72e0bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328399"
---
# <a name="registering-service-provider-unique-identifiers"></a><span data-ttu-id="8dd42-103">Registrieren von eindeutigen Bezeichnern des Dienstanbieters</span><span class="sxs-lookup"><span data-stu-id="8dd42-103">Registering Service Provider Unique Identifiers</span></span>

  
  
<span data-ttu-id="8dd42-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8dd42-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8dd42-105">Adressbuch, Nachrichtenspeicher und Transportanbieter verwenden einen eindeutigen Bezeichner, der als [MAPIUID](mapiuid.md) bezeichnet wird, um Dienstobjekte unterschiedlicher Typen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="8dd42-105">Address book, message store, and transport providers use a unique identifier known as a [MAPIUID](mapiuid.md) to register to service objects of various types.</span></span> <span data-ttu-id="8dd42-106">Ein **MAPIUID** ist ein 16-Byte-Bezeichner, der eine GUID enthält.</span><span class="sxs-lookup"><span data-stu-id="8dd42-106">A **MAPIUID** is a 16-byte identifier that contains a GUID.</span></span> <span data-ttu-id="8dd42-107">Mithilfe des folgenden Verfahrens können Sie eine **MAPIUID** erstellen:</span><span class="sxs-lookup"><span data-stu-id="8dd42-107">You can create a **MAPIUID** by using the following procedure:</span></span> 
  
1. <span data-ttu-id="8dd42-108">Definieren Sie eine Konstante.</span><span class="sxs-lookup"><span data-stu-id="8dd42-108">Define a constant.</span></span>
    
2. <span data-ttu-id="8dd42-109">Rufen Sie das Visual Studio*Create GUID*\* Tool auf.</span><span class="sxs-lookup"><span data-stu-id="8dd42-109">Invoke the Visual Studio*Create GUID*\* tool.</span></span> 
    
<span data-ttu-id="8dd42-110">Ein Adressbuchanbieter kann beispielsweise die folgende Konstante in eine Headerdatei aufnehmen, um eine **MAPIUID**zu definieren:</span><span class="sxs-lookup"><span data-stu-id="8dd42-110">For example, an address book provider might include the following constant in a header file to define a **MAPIUID**:</span></span>
  
 `#define AB_UID_PROVIDER { 0Xe3, 0x3c, 0x67, 0xa0, \ 0xc8, 0x1f, 0x11, 0xce, \ 0xb2, 0xe4, 0x0, 0xaa, \ 0x0, 0x51, 0xe, 0x3b }`
  
 <span data-ttu-id="8dd42-111">**So registrieren Sie eine MAPIUID, wenn es sich bei Ihrem Anbieter um ein Adressbuch oder einen Nachrichtenspeicher Anbieter handelt**</span><span class="sxs-lookup"><span data-stu-id="8dd42-111">**To register a MAPIUID if your provider is an address book or message store provider**</span></span>
  
1. <span data-ttu-id="8dd42-112">Rufen Sie [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md)auf.</span><span class="sxs-lookup"><span data-stu-id="8dd42-112">Call [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md).</span></span>
    
2. <span data-ttu-id="8dd42-113">Registrieren Sie ein **MAPIUID** für jedes Anmeldeobjekt, das Sie instanziieren, und fügen Sie dieses **MAPIUID** in die ersten 16 Bytes des **ab** -Elements jeder Eintrags-ID ein, die Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="8dd42-113">Register a **MAPIUID** for each logon object that you instantiate and include this **MAPIUID** in the first 16 bytes of the **ab** member of every entry identifier that you create.</span></span> <span data-ttu-id="8dd42-114">MAPI verwendet **MAPIUID** -Strukturen zum Zuordnen von Objekten zu Dienstanbietern.</span><span class="sxs-lookup"><span data-stu-id="8dd42-114">MAPI uses **MAPIUID** structures to associate objects with service providers.</span></span> <span data-ttu-id="8dd42-115">Wenn ein Client die [IMAPISession:: OpenEntry](imapisession-openentry.md) -Methode aufruft, um ein Objekt zu öffnen, untersucht MAPI den **MAPIUID** -Teil des Eintrags Bezeichners, der mit dem registrierten **MAPIUID**übereinstimmt, um zu bestimmen, welches Anmeldeobjekt das öffnen soll. Anfrage.</span><span class="sxs-lookup"><span data-stu-id="8dd42-115">When a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method to open an object, MAPI examines the **MAPIUID** portion of the entry identifier, matching it against the registered **MAPIUID**, to determine which logon object should receive the open request.</span></span>
    
3. <span data-ttu-id="8dd42-116">Wenn es sich bei Ihrem Anbieter um einen Transport handelt, registrieren Sie eine oder mehrere **MAPIUID** -Strukturen, wenn MAPI Ihre **IXPLogon:: AddressTypes** -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="8dd42-116">If your provider is a transport, register one or more **MAPIUID** structures when MAPI calls your **IXPLogon::AddressTypes** method.</span></span> <span data-ttu-id="8dd42-117">MAPI verwendet die von Transportanbietern registrierten **MAPIUID** -Strukturen, um die Zuständigkeit für die Nachrichtenübermittlung zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="8dd42-117">MAPI uses the **MAPIUID** structures registered by transport providers to assign responsibility for message delivery.</span></span> 
    
<span data-ttu-id="8dd42-118">Obwohl Dienstanbieter in der Regel ein einzelnes **MAPIUID**registrieren, können Sie mehrere **MAPIUID** -Strukturen registrieren.</span><span class="sxs-lookup"><span data-stu-id="8dd42-118">Although service providers typically register a single **MAPIUID**, you can register multiple **MAPIUID** structures.</span></span> <span data-ttu-id="8dd42-119">Wenn Ihr Adressbuch oder der Nachrichtenspeicher Anbieter mehrere Anmeldeobjekte unterstützt, können Sie möglicherweise ein anderes **MAPIUID** für jedes Logon-Objekt implementieren, indem Sie einem Benutzer erlauben, mehrere Instanzen Ihres Anbieters zu Ihrem Profil hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="8dd42-119">If your address book or message store provider supports multiple logon objects, perhaps by permitting a user to add more than one instance of your provider to their profile, you might want to implement a different **MAPIUID** for each logon object.</span></span> <span data-ttu-id="8dd42-120">Es gibt einige weitere Gründe, mehr als eine **MAPIUID**zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="8dd42-120">There are a few other reasons to support more than one **MAPIUID**:</span></span>
  
- <span data-ttu-id="8dd42-121">Sie müssen mehr als eine Version Ihres Anbieters unterstützen, und die Eintrags-IDs müssen die entsprechende Version darstellen.</span><span class="sxs-lookup"><span data-stu-id="8dd42-121">You must support more than one version of your provider and the entry identifiers must represent the appropriate version.</span></span> <span data-ttu-id="8dd42-122">Weisen Sie für jede Version einen anderen **MAPIUID** zu.</span><span class="sxs-lookup"><span data-stu-id="8dd42-122">Assign a different **MAPIUID** for each version.</span></span> 
    
- <span data-ttu-id="8dd42-123">Sie möchten zwischen den von Ihnen unterstützten Objekttypen unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="8dd42-123">You want to distinguish between the types of objects you support.</span></span> <span data-ttu-id="8dd42-124">Ein Adressbuchanbieter kann beispielsweise ein **MAPIUID** registrieren, um es in den Eintrags Bezeichnern seiner Messaging-Benutzerobjekte zu verwenden, und ein anderes **MAPIUID** für Verteilerlisten verwenden.</span><span class="sxs-lookup"><span data-stu-id="8dd42-124">For example, an address book provider might want to register one **MAPIUID** to use in the entry identifiers of its messaging user objects and a different **MAPIUID** to use for distribution lists.</span></span> 
    
<span data-ttu-id="8dd42-125">Wenn mehrere Anmeldeobjekte gleichzeitig aktiv sind, ist es sinnvoll, für jeden eine eindeutige **MAPIUID** -Struktur zu besitzen.</span><span class="sxs-lookup"><span data-stu-id="8dd42-125">When there are multiple logon objects that are concurrently active, it makes sense to have unique **MAPIUID** structures for each one.</span></span> <span data-ttu-id="8dd42-126">Dadurch wird die Genauigkeit erhöht, mit der MAPI Eingabe-IDs mit Dienstanbietern vergleicht und einige Arbeitsvorgänge spart.</span><span class="sxs-lookup"><span data-stu-id="8dd42-126">This increases the accuracy with which MAPI matches entry identifiers to service providers and saves some work.</span></span> <span data-ttu-id="8dd42-127">Wenn jedes Logon-Objekt seinen eigenen eindeutigen Bezeichner hat, kann MAPI sicherstellen, dass jede Anforderung, die an ein LOGON-Objekt weitergeleitet wird, von diesem Objekt verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8dd42-127">When every logon object has its own unique identifier, MAPI can guarantee that any request it routes to a logon object can be handled by that object.</span></span> <span data-ttu-id="8dd42-128">Wenn Anmeldeobjekte **MAPIUID** -Strukturen freigeben, leitet MAPI die Anforderung an das erste Anmeldeobjekt weiter, das von der **MAPIUID**identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="8dd42-128">When logon objects share **MAPIUID** structures, MAPI routes the request to the first logon object that is identified by the **MAPIUID**.</span></span> <span data-ttu-id="8dd42-129">Wenn eines Ihrer Anmeldeobjekte eine Anforderung erhält, dass es nicht verarbeitet werden kann, da es die Eintrags-ID nicht verarbeitet, leiten Sie die Anforderung an das nächste Anmeldeobjekt weiter, bevor Sie einen Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8dd42-129">If one of your logon objects receives a request that it cannot process because it does not handle the entry identifier, pass the request on to your next logon object before returning an error.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8dd42-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8dd42-130">See also</span></span>



[<span data-ttu-id="8dd42-131">Implementieren der Dienstanbieter Anmeldung</span><span class="sxs-lookup"><span data-stu-id="8dd42-131">Implementing Service Provider Logon</span></span>](implementing-service-provider-logon.md)

