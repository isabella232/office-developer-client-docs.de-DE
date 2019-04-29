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
# <a name="gateway-mappable-properties"></a><span data-ttu-id="9dabe-103">Zum Gateway zuzuordnende Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9dabe-103">Gateway mappable properties</span></span>

<span data-ttu-id="9dabe-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9dabe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9dabe-105">Gateway-zuzuordnende-Eigenschaften sind Eigenschaften, die beim Senden von einer Messaging Domäne an eine andere Übersetzung erfordern.</span><span class="sxs-lookup"><span data-stu-id="9dabe-105">Gateway-mappable properties are properties that may require translation when sent from one messaging domain to another.</span></span> <span data-ttu-id="9dabe-106">Die MAPI-zuzuordnende-Eigenschaften ermöglichen es, dass Nachrichten Informationen enthält, die ein Gateway erfordern, um sicherzustellen, dass das Ziel Messagingsystem Sie ordnungsgemäß verwendet.</span><span class="sxs-lookup"><span data-stu-id="9dabe-106">MAPI's gateway-mappable properties enable messages to include information that requires a gateway to ensure the destination messaging system uses it properly.</span></span> <span data-ttu-id="9dabe-107">Obwohl Gateway-Entwickler diese Übersetzungsfunktion nicht bereitstellen müssen, sollten Sie die zuzuordnende-Eigenschaften als Gelegenheit zur Verbesserung der Verarbeitung von Nachrichteninhalten berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="9dabe-107">Although gateway developers are not required to provide this translation capability, they should consider gateway-mappable properties as an opportunity to improve handling of message content.</span></span>
  
<span data-ttu-id="9dabe-108">MAPI gibt fünf Typen von Gateway-zuzuordnende-Eigenschaften an:</span><span class="sxs-lookup"><span data-stu-id="9dabe-108">MAPI specifies five types of gateway-mappable properties:</span></span>
  
- <span data-ttu-id="9dabe-109">Distinguished Name (DN)</span><span class="sxs-lookup"><span data-stu-id="9dabe-109">Display name</span></span>
    
- <span data-ttu-id="9dabe-110">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="9dabe-110">Email address</span></span>
    
- <span data-ttu-id="9dabe-111">E-Mail-Typ</span><span class="sxs-lookup"><span data-stu-id="9dabe-111">Email type</span></span>
    
- <span data-ttu-id="9dabe-112">Eintrags-ID</span><span class="sxs-lookup"><span data-stu-id="9dabe-112">Entry identifier</span></span>
    
- <span data-ttu-id="9dabe-113">Suchschlüssel</span><span class="sxs-lookup"><span data-stu-id="9dabe-113">Search key</span></span>
    
<span data-ttu-id="9dabe-114">Hierbei handelt es sich um den Satz von Adressierungs Eigenschaften, die Empfängern, Absendern, Berichts Empfängern und Delegierten Absendern und Empfängern zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9dabe-114">This is the set of addressing properties that are associated with recipients, senders, report recipients, and delegated senders and recipients.</span></span> <span data-ttu-id="9dabe-115">Um dem Client zu helfen, diese Eigenschaften so zu definieren, dass er Sie speziell behandelt, gibt MAPI eine Benennungskonvention mit benannten Eigenschaften und Eigenschaftensätzen an.</span><span class="sxs-lookup"><span data-stu-id="9dabe-115">To help your client define these properties so that a gateway handles them specially, MAPI specifies a naming convention using named properties and property sets.</span></span> <span data-ttu-id="9dabe-116">Es sind fünf Eigenschaftensätze vorhanden, die benannte Eigenschaften enthalten, die Adressierungs Eigenschaften, die zugeordnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="9dabe-116">Five property sets exist to hold named properties, the addressing properties that require mapping.</span></span> <span data-ttu-id="9dabe-117">Für jeden zuzuordnende-Eigenschafts ist ein Eigenschaftensatz vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9dabe-117">There is one property set for each type of mappable property.</span></span> <span data-ttu-id="9dabe-118">Die Eigenschaftensätze, in denen diese benannten Adressierungs Einstellungen gespeichert werden, lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="9dabe-118">The property sets that will hold these named addressing properties are as follows.</span></span>
  
|<span data-ttu-id="9dabe-119">**Eigenschaftensatz**</span><span class="sxs-lookup"><span data-stu-id="9dabe-119">**Property set**</span></span>|<span data-ttu-id="9dabe-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9dabe-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9dabe-121">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="9dabe-121">PS_ROUTING_DISPLAY_NAME</span></span>  <br/> |<span data-ttu-id="9dabe-122">Enthält Zeichenfolgeneigenschaften, die als Anzeigenamen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9dabe-122">Contains string properties used as display names.</span></span>  <br/> |
|<span data-ttu-id="9dabe-123">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="9dabe-123">PS_ROUTING_EMAIL_ADDRESSES</span></span>  <br/> |<span data-ttu-id="9dabe-124">Enthält Zeichenfolgeneigenschaften, die als e-Mail-Adressen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9dabe-124">Contains string properties used as email addresses.</span></span>  <br/> |
|<span data-ttu-id="9dabe-125">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="9dabe-125">PS_ROUTING_ADDRTYPE</span></span>  <br/> |<span data-ttu-id="9dabe-126">Enthält Zeichenfolgeneigenschaften, die als e-Mail-Adresstypen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9dabe-126">Contains string properties used as email address types.</span></span>  <br/> |
|<span data-ttu-id="9dabe-127">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="9dabe-127">PS_ROUTING_ENTRYID</span></span>  <br/> |<span data-ttu-id="9dabe-128">Enthält binäre Eigenschaften, die als langfristige Eintragsbezeichner verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9dabe-128">Contains binary properties used as long-term entry identifiers.</span></span>  <br/> |
|<span data-ttu-id="9dabe-129">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="9dabe-129">PS_ROUTING_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="9dabe-130">Enthält binäre Eigenschaften, die als Suchschlüssel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9dabe-130">Contains binary properties used as search keys.</span></span>  <br/> |
   

