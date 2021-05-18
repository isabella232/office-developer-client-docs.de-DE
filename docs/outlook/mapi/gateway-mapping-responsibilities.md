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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422754"
---
# <a name="gateway-mapping-responsibilities"></a><span data-ttu-id="117d1-103">Aufgaben bei der Gateway-Zuordnung</span><span class="sxs-lookup"><span data-stu-id="117d1-103">Gateway mapping responsibilities</span></span>

<span data-ttu-id="117d1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="117d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="117d1-105">Wenn ein MAPI-fähiges Gateway eine Nachricht empfängt, die benannte Eigenschaften in einem der speziellen Eigenschaftensätze enthält, die gatewaymappbare Eigenschaften enthalten sollen, sollte das Gateway alle Eigenschaften dem Protokoll des Zielnachrichtensystems zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="117d1-105">When a MAPI-aware gateway receives a message containing named properties in one of the special property sets designated to contain gateway-mappable properties, the gateway should map all of the properties to the protocol of the destination messaging system.</span></span> <span data-ttu-id="117d1-106">Obwohl MAPI empfiehlt, dass Gateways alle benannten Eigenschaften in den speziellen Eigenschaftensätzen behandeln, werden gateways voraussichtlich nur zwei behandeln: E-Mail-Adresse und Adresstyp.</span><span class="sxs-lookup"><span data-stu-id="117d1-106">Although MAPI recommends that gateways handle all named properties in the special property sets, gateways are expected to handle only two: email address and address type.</span></span> <span data-ttu-id="117d1-107">Da sich die Eigenschaften E-Mail-Adresse und Adresstyp direkt auf die Nachrichtenübermittlung auswirken, ist es wichtig, dass Gateways die Zuordnung dieser beiden Eigenschaften unterstützen.</span><span class="sxs-lookup"><span data-stu-id="117d1-107">Because the email address and address type properties directly affect message transmission, it is critical that gateways support the mapping of these two properties.</span></span> <span data-ttu-id="117d1-108">Da Suchschlüssel aus dem Adresstyp und der Adresse eines Benutzers bestehen, sollten sie nach Möglichkeit auch übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="117d1-108">Because search keys consist of a user's address type and address, they should also be translated if at all possible.</span></span>
  
<span data-ttu-id="117d1-109">Es wird nicht erwartet, dass Eintragsbezeichner häufig verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="117d1-109">Entry identifiers are not expected to be handled frequently.</span></span> <span data-ttu-id="117d1-110">Zum Aktivieren der Zuordnung eines Eintragsbezeichners, der aus einem Messagingsystem stammt, zu einer Eintrags-ID, die von einem anderen Messagingsystem verwendet werden kann, muss das Gateway das Format beider Systeme verwenden können.</span><span class="sxs-lookup"><span data-stu-id="117d1-110">To enable mapping of an entry identifier that originates in one messaging system to an entry identifier that is usable by another messaging system, the gateway must be able to use the format of both systems.</span></span> <span data-ttu-id="117d1-111">Da die meisten Gateways keine Eingabebezeichnerformate kennen, ist die Übersetzung von Eintragsbezeichnern selten.</span><span class="sxs-lookup"><span data-stu-id="117d1-111">Because most gateways are not aware of entry identifier formats, the translation of entry identifiers is rare.</span></span>
  
<span data-ttu-id="117d1-112">Eine weitere mappable Eigenschaft, die nicht häufig übersetzt werden soll, ist der Anzeigename.</span><span class="sxs-lookup"><span data-stu-id="117d1-112">Another mappable property that is not expected to be translated frequently is the display name.</span></span> <span data-ttu-id="117d1-113">Gateways sollten Anzeigenamen speichern und übertragen, aber nicht unbedingt übersetzen.</span><span class="sxs-lookup"><span data-stu-id="117d1-113">Gateways should store display names and transmit them, but not necessarily translate them.</span></span> 
  

