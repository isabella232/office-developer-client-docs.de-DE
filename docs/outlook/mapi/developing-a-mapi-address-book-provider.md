---
title: Entwickeln eines MAPI-Adressbuch Anbieters
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
# <a name="developing-a-mapi-address-book-provider"></a><span data-ttu-id="93e66-103">Entwickeln eines MAPI-Adressbuch Anbieters</span><span class="sxs-lookup"><span data-stu-id="93e66-103">Developing a MAPI Address Book Provider</span></span>

  
  
<span data-ttu-id="93e66-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93e66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93e66-105">Ein Adressbuchanbieter liefert Empfängerinformationen für Clientanwendungen, für Nachrichtenspeicher-und Transportanbieter sowie für MAPI.</span><span class="sxs-lookup"><span data-stu-id="93e66-105">An address book provider supplies recipient information to client applications, to message store and transport providers, and to MAPI.</span></span> <span data-ttu-id="93e66-106">Empfängerinformationen werden hierarchisch in Speicher Fächern, die als Container bezeichnet werden, organisiert.</span><span class="sxs-lookup"><span data-stu-id="93e66-106">Recipient information is organized hierarchically into storage compartments known as containers.</span></span> <span data-ttu-id="93e66-107">Jedes Adressbuch im Profil trägt einen oder mehrere Container der obersten Ebene oder eines übergeordneten Elements zum MAPI-Adressbuch bei, eine integrierte Ansicht von Empfängerinformationen aller Adressbuchanbieter in einer Sitzung.</span><span class="sxs-lookup"><span data-stu-id="93e66-107">Every address book in the profile contributes one or more top-level, or parent, containers to the MAPI address book, an integrated view of recipient information from all address book providers in a session.</span></span> <span data-ttu-id="93e66-108">Über das MAPI-Adressbuch erhalten Clients und andere Dienstanbieter Zugriff auf die Daten eines Adressbuch Anbieters.</span><span class="sxs-lookup"><span data-stu-id="93e66-108">It is through the MAPI address book that clients and other service providers gain access to the data of an address book provider.</span></span>
  
<span data-ttu-id="93e66-109">MAPI erstellt das integrierte Adressbuch nach folgendem:</span><span class="sxs-lookup"><span data-stu-id="93e66-109">MAPI builds the integrated address book by:</span></span>
  
1. <span data-ttu-id="93e66-110">Abrufen der Container der obersten Ebene aus jedem Adressbuchanbieter.</span><span class="sxs-lookup"><span data-stu-id="93e66-110">Retrieving the top-level containers from each address book provider.</span></span>
    
2. <span data-ttu-id="93e66-111">Abrufen der Hierarchietabelle der einzelnen Container.</span><span class="sxs-lookup"><span data-stu-id="93e66-111">Retrieving each container's hierarchy table.</span></span> 
    
3. <span data-ttu-id="93e66-112">Kopieren jeder Hierarchietabelle in eine integrierte Hierarchietabelle.</span><span class="sxs-lookup"><span data-stu-id="93e66-112">Copying each hierarchy table into an integrated hierarchy table.</span></span> <span data-ttu-id="93e66-113">Es ist die integrierte Hierarchietabelle, die für den Client verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="93e66-113">It is the integrated hierarchy table that is exposed to the client.</span></span> 
    
<span data-ttu-id="93e66-114">MAPI stellt wenige Anforderungen an Writer für Adressbuchanbieter.</span><span class="sxs-lookup"><span data-stu-id="93e66-114">MAPI imposes few requirements on address book provider writers.</span></span> <span data-ttu-id="93e66-115">Die Möglichkeiten, die Sie als Adressbuch Autor implementieren können, sind vielfältig und flexibel.</span><span class="sxs-lookup"><span data-stu-id="93e66-115">The range of possible features you can implement as an address book writer is varied and flexible.</span></span> <span data-ttu-id="93e66-116">Beispielsweise könnte Ihr Anbieter auf die Bereitstellung einer schreibgeschützten Ansicht eines bestimmten Typs von Empfängerinformationen beschränken oder einen vollständigen Satz von Features implementieren, sodass Clients oder Anbieter möglicherweise Ergänzungen oder Änderungen an den Empfängerdaten vornehmen und Suchkriterien für die Definition angepasster Ansichten.</span><span class="sxs-lookup"><span data-stu-id="93e66-116">For example, your provider could be limited to supplying a read-only view of a particular type of recipient information or implement a full set of features, perhaps allowing clients or providers to make additions or modifications to the recipient data and to impose search criteria for defining customized views.</span></span> 
  
<span data-ttu-id="93e66-117">Die Daten Ihres Anbieters können sich lokal in einer Datei oder Datenbank oder auf einem Remoteserver befinden.</span><span class="sxs-lookup"><span data-stu-id="93e66-117">Your provider's data can reside locally in a file or database or on a remote server.</span></span> <span data-ttu-id="93e66-118">Einige Adressbuchanbieter sollen mit einem bestimmten Messagingsystem zusammenarbeiten, eng mit einem Transportanbieter gekoppelt, während andere mit einem beliebigen Messagingsystem arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="93e66-118">Some address book providers are meant to work with a particular messaging system, tightly coupled with a transport provider, while others can operate with any messaging system.</span></span>
  
<span data-ttu-id="93e66-119">MAPI definiert einen speziellen Adressbuchanbieter, der als persönliches Adressbuch bezeichnet wird, oder ein PAB, das einen einzelnen änderbaren Container implementiert und Empfängerinformationen aus anderen Containern sowie direkt erstellte Informationen enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="93e66-119">MAPI defines a special type of address book provider called a personal address book, or PAB, that implements a single modifiable container and can hold recipient information copied from other containers as well as information created directly.</span></span> <span data-ttu-id="93e66-120">Auch wenn ein Adressbuchanbieter ein PAB implementieren kann und mehrere PABs zu einem Profil hinzugefügt werden können, kann nur einer dieser Anbieter als PAB während einer Sitzung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="93e66-120">Although any address book provider can implement a PAB and multiple PABs can be added to a profile, only one of these providers can be designated to operate as the PAB during any one session.</span></span> 
  

