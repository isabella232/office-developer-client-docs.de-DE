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
ms.openlocfilehash: 6ebd6009700742e9b1159bc95ff0496c423e512c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422159"
---
# <a name="opening-address-book-entries"></a><span data-ttu-id="c708a-103">Öffnen von Adressbucheinträgen</span><span class="sxs-lookup"><span data-stu-id="c708a-103">Opening address book entries</span></span>

<span data-ttu-id="c708a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c708a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c708a-105">Wenn ein Client oder Anbieter das Öffnen eines Ihrer Objekte angefordert hat, ruft MAPI die [IABLogon::OpenEntry-Methode](iablogon-openentry.md) Ihres Anbieters auf.</span><span class="sxs-lookup"><span data-stu-id="c708a-105">When a client or provider has requested that one of your objects be opened, MAPI calls your provider's [IABLogon::OpenEntry](iablogon-openentry.md) method.</span></span> <span data-ttu-id="c708a-106">MAPI bestimmt, dass der Eintragsbezeichner, der das Zielobjekt darstellt, zu Ihrem Anbieter gehört, indem sie den [MAPIUID-Teil](mapiuid.md) der Eintrags-ID untersucht und mit der **MAPIUID** abgleicht, die Ihr Anbieter im Aufruf von **IMAPISupport::SetProviderUID** registriert hat.</span><span class="sxs-lookup"><span data-stu-id="c708a-106">MAPI determines that the entry identifier representing the target object belongs to your provider by examining the [MAPIUID](mapiuid.md) portion of the entry identifier and matching it to the **MAPIUID** that your provider registered in the call to **IMAPISupport::SetProviderUID**.</span></span> <span data-ttu-id="c708a-107">MAPI ruft dann Ihre **OpenEntry-Methode** auf.</span><span class="sxs-lookup"><span data-stu-id="c708a-107">MAPI then calls your **OpenEntry** method.</span></span> <span data-ttu-id="c708a-108">Ihr Anbieter muss antworten, indem er das entsprechende Objekt abruft – einen Container, eine Verteilerliste oder einen Messagingbenutzer.</span><span class="sxs-lookup"><span data-stu-id="c708a-108">Your provider must respond by retrieving the corresponding object — a container, distribution list, or messaging user.</span></span> 
  
<span data-ttu-id="c708a-109">Ein NULL-Eintragsbezeichner gibt eine Anforderung zum Öffnen des Stammcontainers des Adressbuchanbieters an.</span><span class="sxs-lookup"><span data-stu-id="c708a-109">A NULL entry identifier indicates a request to open the address book provider's root container.</span></span> <span data-ttu-id="c708a-110">Clients öffnen den Stammcontainer, um auf seine Hierarchietabelle und ihre Empfänger zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="c708a-110">Clients open the root container to access its hierarchy table and its recipients.</span></span> <span data-ttu-id="c708a-111">Adressbuchanbieter, die nur Vorlagen zum Erstellen von Einmalempfängern angeben, unterstützen den **OpenEntry-Aufruf** für den Stammcontainer nicht.</span><span class="sxs-lookup"><span data-stu-id="c708a-111">Address book providers that only supply templates for creating one-off recipients do not support the **OpenEntry** call for the root container.</span></span> 
  
### <a name="to-implement-iablogonopenentry"></a><span data-ttu-id="c708a-112">So implementieren Sie IABLogon::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="c708a-112">To implement IABLogon::OpenEntry</span></span>
  
1. <span data-ttu-id="c708a-113">Überprüfen Sie, ob es sich bei der Eintrags-ID um einen gültigen Bezeichner handelt, den Ihr Anbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c708a-113">Check that the entry identifier is a valid identifier that your provider supports.</span></span> <span data-ttu-id="c708a-114">Wenn es sich nicht um einen gültigen Eintragsbezeichner handelt, geben Sie MAPI_E_INVALID_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="c708a-114">If it is not a valid entry identifier, return MAPI_E_INVALID_ENTRYID.</span></span> 
    
2. <span data-ttu-id="c708a-115">Überprüfen Sie das Flag, das mit dem  _ulFlags-Parameter übergeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="c708a-115">Check the flag that is passed in with the  _ulFlags_ parameter.</span></span> <span data-ttu-id="c708a-116">Wenn MAPI die MAPI_MODIFY übergeben hat und Ihr Anbieter die Änderung der Objekte nicht zusent lässt, führen Sie einen Fehler aus, und geben Sie den MAPI_E_ACCESS_DENIED zurück.</span><span class="sxs-lookup"><span data-stu-id="c708a-116">If MAPI has passed in MAPI_MODIFY and your provider does not allow its objects to be modified, fail and return the MAPI_E_ACCESS_DENIED error value.</span></span> 
    
3. <span data-ttu-id="c708a-117">Überprüfen Sie, ob die im  _lpInterface-Parameter_ angeforderte Schnittstelle für den Objekttyp gültig ist, den Ihr Anbieter öffnen soll.</span><span class="sxs-lookup"><span data-stu-id="c708a-117">Check that the interface requested in the  _lpInterface_ parameter is valid for the type of object your provider has been asked to open.</span></span> <span data-ttu-id="c708a-118">Wenn ein ungültiger Parameter übergeben wurde, führen Sie einen Fehler aus, und geben Sie den MAPI_E_INTERFACE_NOT_SUPPORTED zurück.</span><span class="sxs-lookup"><span data-stu-id="c708a-118">If an invalid parameter has been passed in, fail and return the MAPI_E_INTERFACE_NOT_SUPPORTED error value.</span></span> 
    
4. <span data-ttu-id="c708a-119">Wenn der  _cbEntryID-Parameter_ null ist, ist dies eine Anforderung zum Öffnen des Stammcontainers Ihres Anbieters.</span><span class="sxs-lookup"><span data-stu-id="c708a-119">If the  _cbEntryID_ parameter is zero, this is a request to open your provider's root container.</span></span> <span data-ttu-id="c708a-120">Erstellen Sie den Stammcontainer, und geben Sie einen Zeiger auf die **IABContainer-Schnittstellenimplementierung** zurück.</span><span class="sxs-lookup"><span data-stu-id="c708a-120">Create the root container and return a pointer to its **IABContainer** interface implementation.</span></span> 
    
5. <span data-ttu-id="c708a-121">Wenn Ihr Anbieter mehrere Anmeldeobjekte implementiert, die jeweils über eine eigene registrierte **MAPIUID** verfügen, ordnen Sie die im Eintragsbezeichner enthaltene **MAPIUID** dem entsprechenden Anmeldeobjekt zu.</span><span class="sxs-lookup"><span data-stu-id="c708a-121">If your provider implements several logon objects, each with its own registered **MAPIUID**, map the **MAPIUID** contained in the entry identifier with the appropriate logon object.</span></span> 
    
6. <span data-ttu-id="c708a-122">Bestimmen Sie, welcher Objekttyp der Eintragsbezeichner darstellt: ein Messagingbenutzer, eine Verteilerliste oder ein Container, der zu Ihrem Anbieter gehört, oder einen one-off-Messagingbenutzer oder eine Verteilerliste, damit der entsprechende Wert für den  _lpulObjectType-Parameter_ festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c708a-122">Determine which type of object the entry identifier represents: a messaging user, distribution list, or container belonging to your provider or a one-off messaging user or distribution list so that the appropriate value can be set for the  _lpulObjectType_ parameter.</span></span> 
    
7. <span data-ttu-id="c708a-123">Erstellen Sie das Objekt des entsprechenden Typs, und legen Sie die folgenden grundlegenden Eigenschaften ein:</span><span class="sxs-lookup"><span data-stu-id="c708a-123">Create the object of the appropriate type and set the following basic properties:</span></span>
    
    - <span data-ttu-id="c708a-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c708a-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    - <span data-ttu-id="c708a-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c708a-125">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    - <span data-ttu-id="c708a-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c708a-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    - <span data-ttu-id="c708a-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c708a-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
8. <span data-ttu-id="c708a-128">Berechnen **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) und **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) aus Informationen in der Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="c708a-128">Calculate **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) and **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) from information in the entry identifier.</span></span>
    
9. <span data-ttu-id="c708a-129">Gibt einen Zeiger auf die Schnittstellenimplementierung für das Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="c708a-129">Return a pointer to the interface implementation for the object.</span></span> 
    

