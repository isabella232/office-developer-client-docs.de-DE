---
title: Zum Gateway zuzuordnende Eigenschaften
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6f1a399cac2adbae66dabf9383540bb089424d17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430476"
---
# <a name="gateway-mappable-properties"></a><span data-ttu-id="08c68-103">Zum Gateway zuzuordnende Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="08c68-103">Gateway mappable properties</span></span>

<span data-ttu-id="08c68-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08c68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08c68-105">Gateway-mappable-Eigenschaften sind Eigenschaften, die eine Übersetzung erfordern, wenn sie von einer Messagingdomäne in eine andere gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="08c68-105">Gateway-mappable properties are properties that may require translation when sent from one messaging domain to another.</span></span> <span data-ttu-id="08c68-106">Die Gateway-Mappable-Eigenschaften von MAPI ermöglichen es Nachrichten, Informationen zu enthalten, für die ein Gateway erforderlich ist, um sicherzustellen, dass das Zielnachrichtensystem es ordnungsgemäß verwendet.</span><span class="sxs-lookup"><span data-stu-id="08c68-106">MAPI's gateway-mappable properties enable messages to include information that requires a gateway to ensure the destination messaging system uses it properly.</span></span> <span data-ttu-id="08c68-107">Obwohl Gatewayentwickler diese Übersetzungsfunktion nicht bereitstellen müssen, sollten sie Gateway-mappable-Eigenschaften als Möglichkeit zur Verbesserung der Behandlung von Nachrichteninhalten betrachten.</span><span class="sxs-lookup"><span data-stu-id="08c68-107">Although gateway developers are not required to provide this translation capability, they should consider gateway-mappable properties as an opportunity to improve handling of message content.</span></span>
  
<span data-ttu-id="08c68-108">MAPI gibt fünf Typen von Gateway-mappable-Eigenschaften an:</span><span class="sxs-lookup"><span data-stu-id="08c68-108">MAPI specifies five types of gateway-mappable properties:</span></span>
  
- <span data-ttu-id="08c68-109">Distinguished Name (DN)</span><span class="sxs-lookup"><span data-stu-id="08c68-109">Display name</span></span>
    
- <span data-ttu-id="08c68-110">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="08c68-110">Email address</span></span>
    
- <span data-ttu-id="08c68-111">E-Mail-Typ</span><span class="sxs-lookup"><span data-stu-id="08c68-111">Email type</span></span>
    
- <span data-ttu-id="08c68-112">Eintrags-ID</span><span class="sxs-lookup"><span data-stu-id="08c68-112">Entry identifier</span></span>
    
- <span data-ttu-id="08c68-113">Suchtaste</span><span class="sxs-lookup"><span data-stu-id="08c68-113">Search key</span></span>
    
<span data-ttu-id="08c68-114">Dies ist der Satz von Adressierungseigenschaften, die Empfängern, Absendern, Berichtsempfängern und delegierten Absendern und Empfängern zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="08c68-114">This is the set of addressing properties that are associated with recipients, senders, report recipients, and delegated senders and recipients.</span></span> <span data-ttu-id="08c68-115">Damit Der Client diese Eigenschaften so definieren kann, dass sie von einem Gateway speziell behandelt werden, gibt MAPI eine Benennungskonvention mit benannten Eigenschaften und Eigenschaftensätzen an.</span><span class="sxs-lookup"><span data-stu-id="08c68-115">To help your client define these properties so that a gateway handles them specially, MAPI specifies a naming convention using named properties and property sets.</span></span> <span data-ttu-id="08c68-116">Es sind fünf Eigenschaftensätze vorhanden, die benannte Eigenschaften enthalten, die Adressierungseigenschaften, die eine Zuordnung erfordern.</span><span class="sxs-lookup"><span data-stu-id="08c68-116">Five property sets exist to hold named properties, the addressing properties that require mapping.</span></span> <span data-ttu-id="08c68-117">Für jeden Typ von mappable-Eigenschaft ist eine Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="08c68-117">There is one property set for each type of mappable property.</span></span> <span data-ttu-id="08c68-118">Die Eigenschaftensätze, die diese benannten Adressierungseigenschaften enthalten, sind wie folgt.</span><span class="sxs-lookup"><span data-stu-id="08c68-118">The property sets that will hold these named addressing properties are as follows.</span></span>
  
|<span data-ttu-id="08c68-119">**Eigenschaftensatz**</span><span class="sxs-lookup"><span data-stu-id="08c68-119">**Property set**</span></span>|<span data-ttu-id="08c68-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="08c68-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="08c68-121">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="08c68-121">PS_ROUTING_DISPLAY_NAME</span></span>  <br/> |<span data-ttu-id="08c68-122">Enthält Zeichenfolgeneigenschaften, die als Anzeigenamen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08c68-122">Contains string properties used as display names.</span></span>  <br/> |
|<span data-ttu-id="08c68-123">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="08c68-123">PS_ROUTING_EMAIL_ADDRESSES</span></span>  <br/> |<span data-ttu-id="08c68-124">Enthält Zeichenfolgeneigenschaften, die als E-Mail-Adressen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08c68-124">Contains string properties used as email addresses.</span></span>  <br/> |
|<span data-ttu-id="08c68-125">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="08c68-125">PS_ROUTING_ADDRTYPE</span></span>  <br/> |<span data-ttu-id="08c68-126">Enthält Zeichenfolgeneigenschaften, die als E-Mail-Adresstypen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08c68-126">Contains string properties used as email address types.</span></span>  <br/> |
|<span data-ttu-id="08c68-127">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="08c68-127">PS_ROUTING_ENTRYID</span></span>  <br/> |<span data-ttu-id="08c68-128">Enthält binäre Eigenschaften, die als langfristige Eintragsbezeichner verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08c68-128">Contains binary properties used as long-term entry identifiers.</span></span>  <br/> |
|<span data-ttu-id="08c68-129">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="08c68-129">PS_ROUTING_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="08c68-130">Enthält binäre Eigenschaften, die als Suchschlüssel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08c68-130">Contains binary properties used as search keys.</span></span>  <br/> |
   

