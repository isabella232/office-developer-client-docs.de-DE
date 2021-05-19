---
title: Entwickeln eines MAPI-Adressbuchanbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 821cc42d-eebb-4327-b2d4-594421a5c22c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1db3ce53a1da60d946e52a03369c10547676277f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409370"
---
# <a name="developing-a-mapi-address-book-provider"></a><span data-ttu-id="06035-103">Entwickeln eines MAPI-Adressbuchanbieters</span><span class="sxs-lookup"><span data-stu-id="06035-103">Developing a MAPI Address Book Provider</span></span>

  
  
<span data-ttu-id="06035-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06035-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06035-105">Ein Adressbuchanbieter stellt Empfängerinformationen für Clientanwendungen, für Nachrichtenspeicher- und Transportanbieter sowie für MAPI zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="06035-105">An address book provider supplies recipient information to client applications, to message store and transport providers, and to MAPI.</span></span> <span data-ttu-id="06035-106">Empfängerinformationen sind hierarchisch in Speicherfächern organisiert, die als Container bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="06035-106">Recipient information is organized hierarchically into storage compartments known as containers.</span></span> <span data-ttu-id="06035-107">Jedes Adressbuch im Profil trägt einen oder mehrere übergeordnete Container der obersten Ebene zum MAPI-Adressbuch bei, eine integrierte Ansicht von Empfängerinformationen von allen Adressbuchanbietern in einer Sitzung.</span><span class="sxs-lookup"><span data-stu-id="06035-107">Every address book in the profile contributes one or more top-level, or parent, containers to the MAPI address book, an integrated view of recipient information from all address book providers in a session.</span></span> <span data-ttu-id="06035-108">Über das MAPI-Adressbuch erhalten Clients und andere Dienstanbieter Zugriff auf die Daten eines Adressbuchanbieters.</span><span class="sxs-lookup"><span data-stu-id="06035-108">It is through the MAPI address book that clients and other service providers gain access to the data of an address book provider.</span></span>
  
<span data-ttu-id="06035-109">MAPI erstellt das integrierte Adressbuch durch:</span><span class="sxs-lookup"><span data-stu-id="06035-109">MAPI builds the integrated address book by:</span></span>
  
1. <span data-ttu-id="06035-110">Abrufen der Container auf oberster Ebene von jedem Adressbuchanbieter.</span><span class="sxs-lookup"><span data-stu-id="06035-110">Retrieving the top-level containers from each address book provider.</span></span>
    
2. <span data-ttu-id="06035-111">Abrufen der Hierarchietabelle jedes Containers.</span><span class="sxs-lookup"><span data-stu-id="06035-111">Retrieving each container's hierarchy table.</span></span> 
    
3. <span data-ttu-id="06035-112">Kopieren jeder Hierarchietabelle in eine integrierte Hierarchietabelle.</span><span class="sxs-lookup"><span data-stu-id="06035-112">Copying each hierarchy table into an integrated hierarchy table.</span></span> <span data-ttu-id="06035-113">Es ist die integrierte Hierarchietabelle, die für den Client verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="06035-113">It is the integrated hierarchy table that is exposed to the client.</span></span> 
    
<span data-ttu-id="06035-114">MapI stellt nur wenige Anforderungen für Adressbuchanbieterautoren.</span><span class="sxs-lookup"><span data-stu-id="06035-114">MAPI imposes few requirements on address book provider writers.</span></span> <span data-ttu-id="06035-115">Die Palette der möglichen Features, die Sie als Adressbuchautor implementieren können, ist vielfältig und flexibel.</span><span class="sxs-lookup"><span data-stu-id="06035-115">The range of possible features you can implement as an address book writer is varied and flexible.</span></span> <span data-ttu-id="06035-116">Ihr Anbieter kann beispielsweise auf die Bereitstellung einer schreibgeschützten Ansicht einer bestimmten Art von Empfängerinformationen oder die Implementierung eines vollständigen Features beschränkt sein, sodass Clients oder Anbieter möglicherweise Ergänzungen oder Änderungen an den Empfängerdaten und Suchkriterien zum Definieren angepasster Ansichten festlegen können.</span><span class="sxs-lookup"><span data-stu-id="06035-116">For example, your provider could be limited to supplying a read-only view of a particular type of recipient information or implement a full set of features, perhaps allowing clients or providers to make additions or modifications to the recipient data and to impose search criteria for defining customized views.</span></span> 
  
<span data-ttu-id="06035-117">Die Daten Ihres Anbieters können sich lokal in einer Datei oder Datenbank oder auf einem Remoteserver befinden.</span><span class="sxs-lookup"><span data-stu-id="06035-117">Your provider's data can reside locally in a file or database or on a remote server.</span></span> <span data-ttu-id="06035-118">Einige Adressbuchanbieter sind für die Zusammenarbeit mit einem bestimmten Messagingsystem gedacht, das eng mit einem Transportanbieter gekoppelt ist, während andere mit einem beliebigen Messagingsystem arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="06035-118">Some address book providers are meant to work with a particular messaging system, tightly coupled with a transport provider, while others can operate with any messaging system.</span></span>
  
<span data-ttu-id="06035-119">MAPI definiert einen speziellen Typ von Adressbuchanbietern, das als persönliches Adressbuch oder PAB bezeichnet wird, das einen einzelnen veränderbaren Container implementiert und Empfängerinformationen, die aus anderen Containern kopiert wurden, sowie direkt erstellte Informationen enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="06035-119">MAPI defines a special type of address book provider called a personal address book, or PAB, that implements a single modifiable container and can hold recipient information copied from other containers as well as information created directly.</span></span> <span data-ttu-id="06035-120">Obwohl jeder Adressbuchanbieter ein PAB implementieren kann und einem Profil mehrere PABs hinzugefügt werden können, kann nur einer dieser Anbieter während einer sitzung als PAB bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="06035-120">Although any address book provider can implement a PAB and multiple PABs can be added to a profile, only one of these providers can be designated to operate as the PAB during any one session.</span></span> 
  

