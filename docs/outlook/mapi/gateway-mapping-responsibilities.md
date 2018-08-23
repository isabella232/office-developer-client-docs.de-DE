---
title: Gateway Zuordnung Zuständigkeiten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac67bb83-e4f3-4c82-995b-c11a2a195e90
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 91c1d9293108b96fde43b769c97ec673f82a8cb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563030"
---
# <a name="gateway-mapping-responsibilities"></a><span data-ttu-id="c29aa-103">Gateway Zuordnung Zuständigkeiten</span><span class="sxs-lookup"><span data-stu-id="c29aa-103">Gateway mapping responsibilities</span></span>

<span data-ttu-id="c29aa-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c29aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c29aa-105">Wenn ein MAPI-fähigen Gateway eine Nachricht mit benannten Eigenschaften in einem der die spezielle Eigenschaftensätze festgelegte Gateway sämtliche Eigenschaften enthält empfängt, sollte das Gateway alle Eigenschaften des Protokolls des Ziels Messagingsystem zuordnen.</span><span class="sxs-lookup"><span data-stu-id="c29aa-105">When a MAPI-aware gateway receives a message containing named properties in one of the special property sets designated to contain gateway-mappable properties, the gateway should map all of the properties to the protocol of the destination messaging system.</span></span> <span data-ttu-id="c29aa-106">Obwohl MAPI empfiehlt, dass Gateways alle benannte Eigenschaften in die spezielle Eigenschaftensätze zu behandeln, Gateways werden erwartet, dass nur zwei behandeln: e-Mail-Adresse und Adresstyp.</span><span class="sxs-lookup"><span data-stu-id="c29aa-106">Although MAPI recommends that gateways handle all named properties in the special property sets, gateways are expected to handle only two: email address and address type.</span></span> <span data-ttu-id="c29aa-107">Da der e-Mail-Adresse und den Typ Adresseigenschaften direkt die Nachrichtenübermittlung beeinträchtigen, ist es wichtig, Gateways die Zuordnung dieser beiden Eigenschaften unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c29aa-107">Because the email address and address type properties directly affect message transmission, it is critical that gateways support the mapping of these two properties.</span></span> <span data-ttu-id="c29aa-108">Da Search Schlüssel Adresstyp und Adresse eines Benutzers bestehen, sollten sie auch nach Möglichkeit übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="c29aa-108">Because search keys consist of a user's address type and address, they should also be translated if at all possible.</span></span>
  
<span data-ttu-id="c29aa-109">Eintragsbezeichner voraussichtlich nicht häufig behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="c29aa-109">Entry identifiers are not expected to be handled frequently.</span></span> <span data-ttu-id="c29aa-110">Um Zuordnung von Eintrags-ID zu aktivieren, die in einem messaging-System auf einen Eintrag Bezeichner stammt, die von einem anderen Messagingsystem verwendet werden kann, muss das Gateway das Format der beiden Systemen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="c29aa-110">To enable mapping of an entry identifier that originates in one messaging system to an entry identifier that is usable by another messaging system, the gateway must be able to use the format of both systems.</span></span> <span data-ttu-id="c29aa-111">Da die meisten Gateways keine Eintrags-ID Formate kennen, ist die Übersetzung von Eintragsbezeichner selten.</span><span class="sxs-lookup"><span data-stu-id="c29aa-111">Because most gateways are not aware of entry identifier formats, the translation of entry identifiers is rare.</span></span>
  
<span data-ttu-id="c29aa-112">Eine andere sämtliche-Eigenschaft, die nicht häufig übersetzt werden erwartet wird, ist der Anzeigename.</span><span class="sxs-lookup"><span data-stu-id="c29aa-112">Another mappable property that is not expected to be translated frequently is the display name.</span></span> <span data-ttu-id="c29aa-113">Gateways sollte Anzeigenamen speichern und senden, aber nicht unbedingt zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="c29aa-113">Gateways should store display names and transmit them, but not necessarily translate them.</span></span> 
  

