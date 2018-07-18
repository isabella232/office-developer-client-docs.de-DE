---
title: Auflösen eines Empfängernamens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 256412f6ccbe66da067411bf9f66ad0478cf5ca2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795384"
---
# <a name="resolving-a-recipient-name"></a><span data-ttu-id="44106-103">Auflösen eines Empfängernamens</span><span class="sxs-lookup"><span data-stu-id="44106-103">Resolving a Recipient Name</span></span>

  
  
<span data-ttu-id="44106-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="44106-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="44106-105">Wenn eine Nachricht adressiert ist, wird eine Empfängerliste mit Eigenschaften für jeden Empfänger erstellt.</span><span class="sxs-lookup"><span data-stu-id="44106-105">When a message is addressed, a recipient list is built with properties relating to each recipient.</span></span> <span data-ttu-id="44106-106">Durch die Zeit, den die Nachricht gesendet wird, muss eine der Eigenschaften des Empfängers langfristige Eintrags-ID sein:</span><span class="sxs-lookup"><span data-stu-id="44106-106">By the time the message is sent, one of those properties must be the recipient's long-term entry identifier.</span></span> <span data-ttu-id="44106-107">Um sicherzustellen, dass für jeden Empfänger die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft enthält, die [ADRLIST](adrlist.md) -Struktur, die zur Beschreibung der Empfängerliste in den Inhalt des Parameters _LpAdrList_ in einem Aufruf von [IAddrBook übergeben:: ResolveName](iaddrbook-resolvename.md).</span><span class="sxs-lookup"><span data-stu-id="44106-107">To ensure that each recipient includes the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, pass the [ADRLIST](adrlist.md) structure describing your recipient list in the contents of the  _lpAdrList_ parameter in a call to [IAddrBook::ResolveName](iaddrbook-resolvename.md).</span></span>
  
 <span data-ttu-id="44106-108">**ResolveName** beginnt die Verarbeitung durch die Einträge in der **ADRLIST** -Struktur, die bereits behoben wurden, ignorieren, wie das Vorhandensein eines Bezeichners Eintrag in die entsprechenden [ADRENTRY](adrentry.md) Struktur **SPropValue** angegeben Array.</span><span class="sxs-lookup"><span data-stu-id="44106-108">**ResolveName** begins processing by ignoring the entries in the **ADRLIST** structure that have already been resolved, as indicated by the presence of an entry identifier in the corresponding [ADRENTRY](adrentry.md) structure's **SPropValue** array.</span></span> <span data-ttu-id="44106-109">Im nächsten Schritt weist **ResolveName** einmaligen-Eintragsbezeichner automatisch auf zwei Arten von Empfängern:</span><span class="sxs-lookup"><span data-stu-id="44106-109">Next, **ResolveName** automatically assigns one-off entry identifiers to two types of recipients:</span></span> 
  
- <span data-ttu-id="44106-110">Empfänger mit einer Adresse, formatiert als eine IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="44106-110">Recipients with an address formatted as an Internet address</span></span>
    
- <span data-ttu-id="44106-111">Empfänger mit einer Adresse formatiert wie folgt:</span><span class="sxs-lookup"><span data-stu-id="44106-111">Recipients with an address formatted as follows:</span></span>
    
     `displayname[address type:email address]`
    
<span data-ttu-id="44106-112">Für alle verbleibenden Einträge sucht **ResolveName** im Adressbuch nach einer genauen Übereinstimmung für den Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="44106-112">For all remaining entries, **ResolveName** searches the address book for an exact match on the display name.</span></span> <span data-ttu-id="44106-113">**ResolveName** verwendet die **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))-Eigenschaft, um die von Containern, Suche und die Suche Reihenfolge zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="44106-113">**ResolveName** uses the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property to determine the set of containers to search and the search order.</span></span> <span data-ttu-id="44106-114">MAPI-Aufrufen die [IABContainer](iabcontainer-resolvenames.md) -Methode des jedes Container so versuchen Sie, alle Namen aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="44106-114">MAPI calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method of every container to attempt to resolve all of the names.</span></span> <span data-ttu-id="44106-115">Da einige Container nicht **ResolveNames**, unterstützt werden, wenn der Container MAPI_E_NO_SUPPORT zurückgibt, gilt MAPI eine eigenschaftseinschränkung **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) mit der Inhaltstabelle.</span><span class="sxs-lookup"><span data-stu-id="44106-115">Because some containers do not support **ResolveNames**, if the container returns MAPI_E_NO_SUPPORT, MAPI applies a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction against its contents table.</span></span> <span data-ttu-id="44106-116">Alle Address Book Container sind zur Unterstützung von namensauflösung mit diese Einschränkung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="44106-116">All address book containers are required to support name resolution with this restriction.</span></span> <span data-ttu-id="44106-117">Nachdem alle Namen aufgelöst werden, werden keine weiteren Container Aufrufe ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="44106-117">Once all the names are resolved, no further container calls are made.</span></span> <span data-ttu-id="44106-118">Wenn alle Container aufgerufen wurde, aber nicht eindeutige oder nicht aufgelöste Namen bleiben, zeigt MAPI ein Dialogfeld Wenn möglich, den Benutzer zum Auflösen der verbleibenden Names an.</span><span class="sxs-lookup"><span data-stu-id="44106-118">If all the containers have been called, but ambiguous or unresolved names remain, MAPI displays a dialog box if possible to prompt the user to resolve the remaining names.</span></span>
  
<span data-ttu-id="44106-119">Die Einschränkung **PR_ANR** entspricht dem Wert der **PR_ANR** -Eigenschaft auf den Anzeigenamen der **ADRLIST** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="44106-119">The **PR_ANR** restriction matches the value of the **PR_ANR** property against the display name in the **ADRLIST** structure.</span></span> <span data-ttu-id="44106-120">Beschränken die Ansicht des Containers Inhalt Tabelle mit der **PR_ANR** eigenschaftseinschränkung bewirkt, dass die Adressbuchanbieter zum Ausführen eines "am besten erraten" Typs der Übereinstimmung mit der Eigenschaft, die für den Anbieter sinnvoll-Suche.</span><span class="sxs-lookup"><span data-stu-id="44106-120">Limiting the view of a container's contents table with the **PR_ANR** property restriction causes the address book provider to perform a "best guess" type of search, matching against the property that makes sense for the provider.</span></span> <span data-ttu-id="44106-121">Beispielsweise könnte eine Adressbuchanbieter immer übereinstimmen Namen in der Empfängerliste gegen **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) während einer anderen Administrator, um die Eigenschaft auswählen kann möglicherweise.</span><span class="sxs-lookup"><span data-stu-id="44106-121">For example, one address book provider might always match names in the recipient list against **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) while another might allow an administrator to select the property.</span></span>
  
 <span data-ttu-id="44106-122">**Um eine Beschränkung der PR_ANR-Eigenschaft für ein Adressbuchcontainer Inhaltstabelle festzulegen**</span><span class="sxs-lookup"><span data-stu-id="44106-122">**To set a PR_ANR property restriction on an address book container's contents table**</span></span>
  
1. <span data-ttu-id="44106-123">Erstellen Sie eine [SRestriction](srestriction.md) -Struktur, wie im folgenden Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="44106-123">Create an [SRestriction](srestriction.md) structure as shown in the following code:</span></span> 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. <span data-ttu-id="44106-124">Rufen Sie den Inhalt der Tabelle [Methode IMAPITable:: Restrict](imapitable-restrict.md) -Methode, die **SRestriction** -Struktur als des _LpRestriction_ -Parameters übergeben.</span><span class="sxs-lookup"><span data-stu-id="44106-124">Call the contents table's [IMAPITable::Restrict](imapitable-restrict.md) method, passing the **SRestriction** structure as the  _lpRestriction_ parameter.</span></span> 
    

