---
title: Öffnen von Adressbucheinträgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c36c70eacffcb4a41af0e73eea85143ab737867f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793318"
---
# <a name="opening-address-book-entries"></a><span data-ttu-id="f3fc9-103">Öffnen von Adressbucheinträgen</span><span class="sxs-lookup"><span data-stu-id="f3fc9-103">Opening address book entries</span></span>

<span data-ttu-id="f3fc9-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f3fc9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f3fc9-105">MAPI Ihres Anbieters [IABLogon::OpenEntry](iablogon-openentry.md) Methode aufgerufen, wenn ein Client oder Anbieter angefordert hat, dass eines Ihrer Objekte geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-105">When a client or provider has requested that one of your objects be opened, MAPI calls your provider's [IABLogon::OpenEntry](iablogon-openentry.md) method.</span></span> <span data-ttu-id="f3fc9-106">MAPI bestimmt, dass die Eintrags-ID, das Zielobjekt darstellt, die an Ihren Anbieter durch Untersuchen des [MAPIUID](mapiuid.md) Teils die Eintrags-ID und an die **MAPIUID** , die vom Dienstanbieter im Aufruf **registriert übereinstimmende gehört IMAPISupport::SetProviderUID**.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-106">MAPI determines that the entry identifier representing the target object belongs to your provider by examining the [MAPIUID](mapiuid.md) portion of the entry identifier and matching it to the **MAPIUID** that your provider registered in the call to **IMAPISupport::SetProviderUID**.</span></span> <span data-ttu-id="f3fc9-107">MAPI ruft dann die **OpenEntry** -Methode.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-107">MAPI then calls your **OpenEntry** method.</span></span> <span data-ttu-id="f3fc9-108">Vom Dienstanbieter muss durch Abrufen des entsprechenden-Objekts reagieren – eine Container, Verteilerliste oder messaging-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-108">Your provider must respond by retrieving the corresponding object — a container, distribution list, or messaging user.</span></span> 
  
<span data-ttu-id="f3fc9-109">Eine NULL-Eintrags-ID gibt eine Anforderung zum Öffnen der Adressbuchanbieter Stammcontainer.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-109">A NULL entry identifier indicates a request to open the address book provider's root container.</span></span> <span data-ttu-id="f3fc9-110">Clients öffnen Sie im Stamm der Hierarchietabelle und deren Empfänger für den Zugriff.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-110">Clients open the root container to access its hierarchy table and its recipients.</span></span> <span data-ttu-id="f3fc9-111">Von adressbuchanbietern implementierte, die nur Vorlagen zum Erstellen von einmaligen Empfänger angeben unterstützt den Anruf **OpenEntry** nicht für den Container Root.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-111">Address book providers that only supply templates for creating one-off recipients do not support the **OpenEntry** call for the root container.</span></span> 
  
### <a name="to-implement-iablogonopenentry"></a><span data-ttu-id="f3fc9-112">Implementieren von IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="f3fc9-112">To implement IABLogon::OpenEntry</span></span>
  
1. <span data-ttu-id="f3fc9-113">Überprüfen Sie, dass die Eintrags-ID ein gültiger Bezeichner ist, den vom Anbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-113">Check that the entry identifier is a valid identifier that your provider supports.</span></span> <span data-ttu-id="f3fc9-114">Wenn es sich nicht um eine gültige Eintrags-ID ist, geben Sie MAPI_E_INVALID_ENTRYID zurück.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-114">If it is not a valid entry identifier, return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="f3fc9-115">Überprüfen Sie die Kennzeichen, die sich mit der _UlFlags_ -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-115">Check the flag that is passed in with the  _ulFlags_ parameter.</span></span> <span data-ttu-id="f3fc9-116">Wenn MAPI in MAPI_MODIFY verstrichen ist und vom Dienstanbieter lässt sich nicht auf seine Objekte geändert werden soll, ein Fehler auftritt, und geben Sie den Fehlerwert MAPI_E_ACCESS_DENIED zurück.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-116">If MAPI has passed in MAPI_MODIFY and your provider does not allow its objects to be modified, fail and return the MAPI_E_ACCESS_DENIED error value.</span></span> 
    
3. <span data-ttu-id="f3fc9-117">Überprüfen Sie, dass die im Parameter _LpInterface_ angeforderte Schnittstelle für den Typ des Objekts gültig ist, die zum Öffnen des Anbieters aufgefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-117">Check that the interface requested in the  _lpInterface_ parameter is valid for the type of object your provider has been asked to open.</span></span> <span data-ttu-id="f3fc9-118">Wenn in ein ungültiger Parameter übergeben wurde, wird ein Fehler auftritt, und geben Sie den Fehlerwert MAPI_E_INTERFACE_NOT_SUPPORTED zurück.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-118">If an invalid parameter has been passed in, fail and return the MAPI_E_INTERFACE_NOT_SUPPORTED error value.</span></span> 
    
4. <span data-ttu-id="f3fc9-119">Wenn der Parameter _CbEntryID_ gleich NULL ist, ist dies eine Anforderung zum Öffnen des Anbieters Stammcontainer.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-119">If the  _cbEntryID_ parameter is zero, this is a request to open your provider's root container.</span></span> <span data-ttu-id="f3fc9-120">Erstellen Sie den Stammcontainer, und zurückgegeben Sie ein Zeiger auf die Implementierung eines **IABContainer** .</span><span class="sxs-lookup"><span data-stu-id="f3fc9-120">Create the root container and return a pointer to its **IABContainer** interface implementation.</span></span> 
    
5. <span data-ttu-id="f3fc9-121">Wenn der Anbieter mehrere Logon-Objekten implementiert, registriert jeweils mit eigenem **MAPIUID**, Zuordnung, in der **MAPIUID** die Eintrags-ID mit dem entsprechenden Anmeldung-Objekt enthalten.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-121">If your provider implements several logon objects, each with its own registered **MAPIUID**, map the **MAPIUID** contained in the entry identifier with the appropriate logon object.</span></span> 
    
6. <span data-ttu-id="f3fc9-122">Bestimmen, welche Art des Objekts darstellt, die Eintrags-ID: messaging Benutzer, Verteilerliste oder Container, die auf Ihrem Anbieter oder eine einmalige messaging Benutzer oder eine Verteilergruppe gehören, damit Sie der entsprechende Wert für die _LpulObjectType_ festgelegt werden kann der Parameter.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-122">Determine which type of object the entry identifier represents: a messaging user, distribution list, or container belonging to your provider or a one-off messaging user or distribution list so that the appropriate value can be set for the  _lpulObjectType_ parameter.</span></span> 
    
7. <span data-ttu-id="f3fc9-123">Erstellen Sie das Objekt des entsprechenden Typs, und legen Sie die folgenden grundlegenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f3fc9-123">Create the object of the appropriate type and set the following basic properties:</span></span>
    
    - <span data-ttu-id="f3fc9-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f3fc9-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    - <span data-ttu-id="f3fc9-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f3fc9-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    - <span data-ttu-id="f3fc9-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f3fc9-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    - <span data-ttu-id="f3fc9-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f3fc9-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
8. <span data-ttu-id="f3fc9-128">Berechnen Sie anhand der Informationen in die Eintrags-ID **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) und **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="f3fc9-128">Calculate **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) and **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from information in the entry identifier.</span></span>
    
9. <span data-ttu-id="f3fc9-129">Ein Zeiger auf die schnittstellenimplementierung für das Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f3fc9-129">Return a pointer to the interface implementation for the object.</span></span> 
    

