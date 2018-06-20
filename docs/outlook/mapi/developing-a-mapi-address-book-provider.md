---
title: Entwickeln von einem MAPI-Adressbuchanbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 821cc42d-eebb-4327-b2d4-594421a5c22c
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 03f53dbfbe57db76ee8ceefda3f6938301f70da8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791531"
---
# <a name="developing-a-mapi-address-book-provider"></a><span data-ttu-id="b09ea-103">Entwickeln von einem MAPI-Adressbuchanbieter</span><span class="sxs-lookup"><span data-stu-id="b09ea-103">Developing a MAPI Address Book Provider</span></span>

  
  
<span data-ttu-id="b09ea-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b09ea-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b09ea-105">Adressbuch-Dienstanbieter liefert Empfängerinformationen Clientanwendungen Nachrichtenspeicher und transport-Anbieter und MAPI.</span><span class="sxs-lookup"><span data-stu-id="b09ea-105">An address book provider supplies recipient information to client applications, to message store and transport providers, and to MAPI.</span></span> <span data-ttu-id="b09ea-106">Empfängerinformationen ist in Storage Kästchen bekannt als Container hierarchisch organisiert.</span><span class="sxs-lookup"><span data-stu-id="b09ea-106">Recipient information is organized hierarchically into storage compartments known as containers.</span></span> <span data-ttu-id="b09ea-107">Jedes Adressbuch im Profil trägt eine oder mehr auf oberster Ebene oder übergeordneten Inhaltstyps, Bücher zu MAPI-Adressbuch, eine integrierte Ansicht der Empfängerinformationen aus allen Adresse Container Anbieter in einer Sitzung.</span><span class="sxs-lookup"><span data-stu-id="b09ea-107">Every address book in the profile contributes one or more top-level, or parent, containers to the MAPI address book, an integrated view of recipient information from all address book providers in a session.</span></span> <span data-ttu-id="b09ea-108">Es ist über das MAPI-Adressbuch, dass Clients und andere Telefoniedienstanbieter Zugriff auf die Daten der Adressbuch-Dienstanbieter erhalten.</span><span class="sxs-lookup"><span data-stu-id="b09ea-108">It is through the MAPI address book that clients and other service providers gain access to the data of an address book provider.</span></span>
  
<span data-ttu-id="b09ea-109">MAPI-builds integrierte Adressbuch nach:</span><span class="sxs-lookup"><span data-stu-id="b09ea-109">MAPI builds the integrated address book by:</span></span>
  
1. <span data-ttu-id="b09ea-110">Abrufen von Container der obersten Ebene aus jeder Adressbuchanbieter.</span><span class="sxs-lookup"><span data-stu-id="b09ea-110">Retrieving the top-level containers from each address book provider.</span></span>
    
2. <span data-ttu-id="b09ea-111">Abrufen des Containers Hierarchietabelle.</span><span class="sxs-lookup"><span data-stu-id="b09ea-111">Retrieving each container's hierarchy table.</span></span> 
    
3. <span data-ttu-id="b09ea-112">Kopieren jede Hierarchietabelle in eine Hierarchietabelle integrierte.</span><span class="sxs-lookup"><span data-stu-id="b09ea-112">Copying each hierarchy table into an integrated hierarchy table.</span></span> <span data-ttu-id="b09ea-113">Es ist die integrierte Hierarchietabelle, die an den Client verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="b09ea-113">It is the integrated hierarchy table that is exposed to the client.</span></span> 
    
<span data-ttu-id="b09ea-114">MAPI erfordert einige Anforderungen auf Address Book Anbieterwriter.</span><span class="sxs-lookup"><span data-stu-id="b09ea-114">MAPI imposes few requirements on address book provider writers.</span></span> <span data-ttu-id="b09ea-115">Der Bereich der möglichen Features können Sie implementieren, wie ein Address Book Writer verschiedenen und flexible ist.</span><span class="sxs-lookup"><span data-stu-id="b09ea-115">The range of possible features you can implement as an address book writer is varied and flexible.</span></span> <span data-ttu-id="b09ea-116">Beispielsweise konnte Ihres Anbieters mit der Bereitstellung einer nur-Lese-Ansicht eines bestimmten Typs von Empfängerinformationen beschränkt werden oder implementieren eine umfassende Auswahl an Features, vielleicht und-Clients oder Anbieter um vorgenommene Hinzufügungen oder Änderungen an den Daten des Empfängers zu gestalten und zugrunde liegen die Suchkriterien Sie für benutzerdefinierte Ansichten definieren.</span><span class="sxs-lookup"><span data-stu-id="b09ea-116">For example, your provider could be limited to supplying a read-only view of a particular type of recipient information or implement a full set of features, perhaps allowing clients or providers to make additions or modifications to the recipient data and to impose search criteria for defining customized views.</span></span> 
  
<span data-ttu-id="b09ea-117">Daten des Anbieters können lokal in einer Datei oder Datenbank oder auf einem Remoteserver befinden.</span><span class="sxs-lookup"><span data-stu-id="b09ea-117">Your provider's data can reside locally in a file or database or on a remote server.</span></span> <span data-ttu-id="b09ea-118">Einige adressbuchanbietern implementierte sollen arbeiten mit einem bestimmten Messagingsystem eng mit eines Transportdienstes gekoppelt, während andere Benutzer mit messaging-System ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="b09ea-118">Some address book providers are meant to work with a particular messaging system, tightly coupled with a transport provider, while others can operate with any messaging system.</span></span>
  
<span data-ttu-id="b09ea-119">MAPI definiert einen speziellen Adressbuchanbieter ein persönliches Adressbuch oder PAB, die einen einzelnen änderbaren Container implementiert und kann halten, kopiert aus anderen Containern sowie Informationen, die direkt erstellt Empfängerinformationen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b09ea-119">MAPI defines a special type of address book provider called a personal address book, or PAB, that implements a single modifiable container and can hold recipient information copied from other containers as well as information created directly.</span></span> <span data-ttu-id="b09ea-120">Zwar alle Adressbuchanbieter ein PAB implementieren kann und mehrere PABs zu einem Profil hinzugefügt werden können, kann nur eine dieser Anbieter als PAB während einer Sitzung ein Betrieb festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b09ea-120">Although any address book provider can implement a PAB and multiple PABs can be added to a profile, only one of these providers can be designated to operate as the PAB during any one session.</span></span> 
  

