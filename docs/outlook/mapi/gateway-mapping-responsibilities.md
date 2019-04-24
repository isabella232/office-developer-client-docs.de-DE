---
title: Aufgaben bei der Gateway-Zuordnung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac67bb83-e4f3-4c82-995b-c11a2a195e90
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 214d24bb0b0af525d5e2588c556c37cf720364a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342798"
---
# <a name="gateway-mapping-responsibilities"></a><span data-ttu-id="b07aa-103">Aufgaben bei der Gateway-Zuordnung</span><span class="sxs-lookup"><span data-stu-id="b07aa-103">Gateway mapping responsibilities</span></span>

<span data-ttu-id="b07aa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b07aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b07aa-105">Wenn ein MAPI-fähiges Gateway eine Nachricht mit benannten Eigenschaften in einem der speziellen Eigenschaftssätze empfängt, die zuzuordnende-Eigenschaften enthalten, sollte das Gateway alle Eigenschaften dem Protokoll des Zielmessagingsystems zuordnen.</span><span class="sxs-lookup"><span data-stu-id="b07aa-105">When a MAPI-aware gateway receives a message containing named properties in one of the special property sets designated to contain gateway-mappable properties, the gateway should map all of the properties to the protocol of the destination messaging system.</span></span> <span data-ttu-id="b07aa-106">Obgleich MAPI empfiehlt, dass Gateways alle benannten Eigenschaften in den speziellen Eigenschaftssätzen behandeln, wird davon ausgegangen, dass Gateways nur zwei behandeln: e-Mail-Adresse und Adresstyp.</span><span class="sxs-lookup"><span data-stu-id="b07aa-106">Although MAPI recommends that gateways handle all named properties in the special property sets, gateways are expected to handle only two: email address and address type.</span></span> <span data-ttu-id="b07aa-107">Da sich die Eigenschaften von e-Mail-Adresse und Adresstyp direkt auf die Nachrichtenübertragung auswirken, ist es wichtig, dass Gateways die Zuordnung dieser beiden Eigenschaften unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b07aa-107">Because the email address and address type properties directly affect message transmission, it is critical that gateways support the mapping of these two properties.</span></span> <span data-ttu-id="b07aa-108">Da Suchschlüssel den Adresstyp und die Adresse eines Benutzers enthalten, sollten Sie auch übersetzt werden, falls dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="b07aa-108">Because search keys consist of a user's address type and address, they should also be translated if at all possible.</span></span>
  
<span data-ttu-id="b07aa-109">Eintragsbezeichner werden nicht häufig behandelt.</span><span class="sxs-lookup"><span data-stu-id="b07aa-109">Entry identifiers are not expected to be handled frequently.</span></span> <span data-ttu-id="b07aa-110">Um die Zuordnung eines Eintrags Bezeichners, der sich in einem Messagingsystem ausgibt, zu einer Eintrags-ID zu ermöglichen, die von einem anderen Messagingsystem verwendet werden kann, muss das Gateway in der Lage sein, das Format beider Systeme zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b07aa-110">To enable mapping of an entry identifier that originates in one messaging system to an entry identifier that is usable by another messaging system, the gateway must be able to use the format of both systems.</span></span> <span data-ttu-id="b07aa-111">Da die meisten Gateways die Eingabe-ID-Formate nicht erkennen, ist die Übersetzung von Eintrags Bezeichnern selten.</span><span class="sxs-lookup"><span data-stu-id="b07aa-111">Because most gateways are not aware of entry identifier formats, the translation of entry identifiers is rare.</span></span>
  
<span data-ttu-id="b07aa-112">Eine weitere zuzuordnende-Eigenschaft, die nicht häufig übersetzt werden sollte, ist der Anzeigename.</span><span class="sxs-lookup"><span data-stu-id="b07aa-112">Another mappable property that is not expected to be translated frequently is the display name.</span></span> <span data-ttu-id="b07aa-113">Gateways sollten Anzeige Namen speichern und übertragen, aber nicht notwendigerweise übersetzen.</span><span class="sxs-lookup"><span data-stu-id="b07aa-113">Gateways should store display names and transmit them, but not necessarily translate them.</span></span> 
  

