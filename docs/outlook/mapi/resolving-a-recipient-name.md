---
title: Auflösen eines Empfängernamens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2baed391-85bd-4e88-8800-c19bc2d2d54a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a3faed3dda2461cab749c824fc97c2074e62375f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328672"
---
# <a name="resolving-a-recipient-name"></a><span data-ttu-id="3d51e-103">Auflösen eines Empfängernamens</span><span class="sxs-lookup"><span data-stu-id="3d51e-103">Resolving a Recipient Name</span></span>

  
  
<span data-ttu-id="3d51e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d51e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d51e-105">Wenn eine Nachricht adressiert wird, wird eine Empfängerliste mit Eigenschaften für jeden Empfänger erstellt.</span><span class="sxs-lookup"><span data-stu-id="3d51e-105">When a message is addressed, a recipient list is built with properties relating to each recipient.</span></span> <span data-ttu-id="3d51e-106">Zu dem Zeitpunkt, zu dem die Nachricht gesendet wird, muss eine dieser Eigenschaften der langfristige Eintragsbezeichner des Empfängers sein.</span><span class="sxs-lookup"><span data-stu-id="3d51e-106">By the time the message is sent, one of those properties must be the recipient's long-term entry identifier.</span></span> <span data-ttu-id="3d51e-107">Um sicherzustellen, dass jeder Empfänger die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft enthält, übergeben Sie die [ADRLIST](adrlist.md) -Struktur, die ihre Empfängerliste in den Inhalten des _lpAdrList_ -Parameters beschreibt, in einem Aufruf von [IAddrBook:: ](iaddrbook-resolvename.md)ResolveName.</span><span class="sxs-lookup"><span data-stu-id="3d51e-107">To ensure that each recipient includes the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, pass the [ADRLIST](adrlist.md) structure describing your recipient list in the contents of the  _lpAdrList_ parameter in a call to [IAddrBook::ResolveName](iaddrbook-resolvename.md).</span></span>
  
 <span data-ttu-id="3d51e-108">\*\*\*\* ResolveName beginnt mit der Verarbeitung, indem die Einträge in der **ADRLIST** -Struktur, die bereits aufgelöst wurden, ignoriert werden, wie durch das vorhanden sein eines Eintrags Bezeichners in der **SPropValue** der zugehörigen [Miet](adrentry.md) Struktur angegeben. Array.</span><span class="sxs-lookup"><span data-stu-id="3d51e-108">**ResolveName** begins processing by ignoring the entries in the **ADRLIST** structure that have already been resolved, as indicated by the presence of an entry identifier in the corresponding [ADRENTRY](adrentry.md) structure's **SPropValue** array.</span></span> <span data-ttu-id="3d51e-109">Als nächstes \*\*\*\* weist ResolveName zwei Typen von Empfängern automatisch einmalige Eintrags-IDs zu:</span><span class="sxs-lookup"><span data-stu-id="3d51e-109">Next, **ResolveName** automatically assigns one-off entry identifiers to two types of recipients:</span></span> 
  
- <span data-ttu-id="3d51e-110">Empfänger mit einer als Internet Adresse formatierten Adresse</span><span class="sxs-lookup"><span data-stu-id="3d51e-110">Recipients with an address formatted as an Internet address</span></span>
    
- <span data-ttu-id="3d51e-111">Empfänger mit einer Adresse, die wie folgt formatiert ist:</span><span class="sxs-lookup"><span data-stu-id="3d51e-111">Recipients with an address formatted as follows:</span></span>
    
     `displayname[address type:email address]`
    
<span data-ttu-id="3d51e-112">Für alle verbleibenden \*\*\*\* Einträge durchsucht ResolveName das Adressbuch nach einer genauen Übereinstimmung mit dem Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="3d51e-112">For all remaining entries, **ResolveName** searches the address book for an exact match on the display name.</span></span> <span data-ttu-id="3d51e-113">\*\*\*\* ResolveName verwendet die **PR_AB_SEARCH_PATH** ([pidtagabsearchpath (](pidtagabsearchpath-canonical-property.md))-Eigenschaft, um den zu durchsuchenden Container Satz und die Suchreihenfolge zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="3d51e-113">**ResolveName** uses the **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)) property to determine the set of containers to search and the search order.</span></span> <span data-ttu-id="3d51e-114">MAPI Ruft die [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) -Methode jedes Containers auf, um alle Namen aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="3d51e-114">MAPI calls the [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method of every container to attempt to resolve all of the names.</span></span> <span data-ttu-id="3d51e-115">Da einige Container **ResolveNames**nicht unterstützen, wendet MAPI eine **PR_ANR** ([pidtaganr (](pidtaganr-canonical-property.md))-Eigenschaftseinschränkung für die Inhaltstabelle an, wenn der Container MAPI_E_NO_SUPPORT zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3d51e-115">Because some containers do not support **ResolveNames**, if the container returns MAPI_E_NO_SUPPORT, MAPI applies a **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) property restriction against its contents table.</span></span> <span data-ttu-id="3d51e-116">Alle Adressbuchcontainer sind erforderlich, um die Namensauflösung mit dieser Einschränkung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3d51e-116">All address book containers are required to support name resolution with this restriction.</span></span> <span data-ttu-id="3d51e-117">Nachdem alle Namen aufgelöst wurden, werden keine weiteren Container Aufrufe durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="3d51e-117">Once all the names are resolved, no further container calls are made.</span></span> <span data-ttu-id="3d51e-118">Wenn alle Container aufgerufen wurden, aber mehrdeutige oder nicht aufgelöste Namen bleiben, zeigt MAPI ein Dialogfeld an, wenn möglich, um den Benutzer aufzufordern, die verbleibenden Namen aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="3d51e-118">If all the containers have been called, but ambiguous or unresolved names remain, MAPI displays a dialog box if possible to prompt the user to resolve the remaining names.</span></span>
  
<span data-ttu-id="3d51e-119">Die **PR_ANR** -Einschränkung entspricht dem Wert der **PR_ANR** -Eigenschaft mit dem Anzeigenamen in der **ADRLIST** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="3d51e-119">The **PR_ANR** restriction matches the value of the **PR_ANR** property against the display name in the **ADRLIST** structure.</span></span> <span data-ttu-id="3d51e-120">Durch Einschränken der Ansicht der Inhaltstabelle eines Containers mit der **PR_ANR** -Eigenschaftseinschränkung führt der Adressbuchanbieter einen "bestmöglichen" Suchtyp aus, der mit der für den Anbieter sinnvollsten Eigenschaft verglichen wird.</span><span class="sxs-lookup"><span data-stu-id="3d51e-120">Limiting the view of a container's contents table with the **PR_ANR** property restriction causes the address book provider to perform a "best guess" type of search, matching against the property that makes sense for the provider.</span></span> <span data-ttu-id="3d51e-121">Beispielsweise kann ein Adressbuchanbieter immer die Namen in der Empfängerliste mit **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) vergleichen, während eine andere Person es einem Administrator ermöglicht, die Eigenschaft auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="3d51e-121">For example, one address book provider might always match names in the recipient list against **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) while another might allow an administrator to select the property.</span></span>
  
 <span data-ttu-id="3d51e-122">**So legen Sie eine PR_ANR-Eigenschaftseinschränkung für die Inhaltstabelle eines Adressbuch Containers fest**</span><span class="sxs-lookup"><span data-stu-id="3d51e-122">**To set a PR_ANR property restriction on an address book container's contents table**</span></span>
  
1. <span data-ttu-id="3d51e-123">Erstellen Sie eine [SRestriction](srestriction.md) -Struktur, wie im folgenden Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="3d51e-123">Create an [SRestriction](srestriction.md) structure as shown in the following code:</span></span> 
    
  ```cpp
  SRestriction SRestrict;
  SRestrict.rt = RES_PROPERTY;
  SRestrict.res.resProperty.relop = RELOP_EQ;
  SRestrict.res.resProperty.ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->ulPropTag = PR_ANR;
  SRestrict.res.resProperty.lpProp->Value.LPSZ = lpszName;
   
  ```

2. <span data-ttu-id="3d51e-124">Rufen Sie die [IMAPITable:: Restrict](imapitable-restrict.md) -Methode der Inhaltstabelle auf, und übergeben Sie die **SRestriction** -Struktur als _lpRestriction_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="3d51e-124">Call the contents table's [IMAPITable::Restrict](imapitable-restrict.md) method, passing the **SRestriction** structure as the  _lpRestriction_ parameter.</span></span> 
    

