---
title: Empfängereigenschaften für alle Nachrichten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18c96796-f38d-4058-9c51-9c5a14990846
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3c5764d74039249ccac47d449f0ebd4042893434
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439716"
---
# <a name="recipient-properties-for-all-messages"></a><span data-ttu-id="5d031-103">Empfängereigenschaften für alle Nachrichten</span><span class="sxs-lookup"><span data-stu-id="5d031-103">Recipient Properties for All Messages</span></span>

  
  
<span data-ttu-id="5d031-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d031-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d031-105">Die folgenden Eigenschaften sind in der Regel für alle Nachrichtenempfänger vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5d031-105">The following properties are typically present for all message recipients.</span></span> <span data-ttu-id="5d031-106">**PR_EMAIL_ADDRESS** und **PR_SEARCH_KEY** sind optional. alle anderen Eigenschaften sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5d031-106">**PR_EMAIL_ADDRESS** and **PR_SEARCH_KEY** are optional; all of the other properties are required.</span></span> 
  
<span data-ttu-id="5d031-107">**Tabellentitel**</span><span class="sxs-lookup"><span data-stu-id="5d031-107">**Table Title**</span></span>

|<span data-ttu-id="5d031-108">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="5d031-108">**Property**</span></span>|<span data-ttu-id="5d031-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5d031-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5d031-110">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5d031-110">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5d031-111">Enthält den E-Mail-Adresstyp des Messagingbenutzers, z. B. SMTP.</span><span class="sxs-lookup"><span data-stu-id="5d031-111">Contains the messaging user's email address type, such as SMTP.</span></span>  <br/> |
|<span data-ttu-id="5d031-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5d031-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5d031-113">Enthält den Anzeigenamen für ein bestimmtes MAPI-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5d031-113">Contains the display name for a given MAPI object.</span></span>  <br/> |
|<span data-ttu-id="5d031-114">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5d031-114">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5d031-115">Enthält einen Wert, der zum Zuordnen eines Symbols zu einer bestimmten Zeile einer Tabelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5d031-115">Contains a value used to associate an icon with a particular row of a table.</span></span>  <br/> |
|<span data-ttu-id="5d031-116">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5d031-116">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5d031-117">Enthält die E-Mail-Adresse des Messagingbenutzers.</span><span class="sxs-lookup"><span data-stu-id="5d031-117">Contains the messaging user's email address.</span></span>  <br/> |
|<span data-ttu-id="5d031-118">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5d031-118">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5d031-119">Enthält einen MAPI-Eintragsbezeichner, der zum Öffnen und Bearbeiten von Eigenschaften eines bestimmten MAPI-Objekts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5d031-119">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span>  <br/> |
|<span data-ttu-id="5d031-120">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5d031-120">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5d031-121">Enthält den Typ eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="5d031-121">Contains the type of an object.</span></span>  <br/> |
|<span data-ttu-id="5d031-122">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="5d031-122">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="5d031-123">Enthält einen binär-vergleichbaren Schlüssel, der korrelierte Objekte für eine Suche identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5d031-123">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>  <br/> |
   

