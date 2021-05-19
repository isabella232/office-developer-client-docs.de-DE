---
title: Hinzufügen von Adressbucheinträgen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63444a65-d56a-4dbd-9aa6-e60f18ba8104
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8dc82a99ee088d42c076ca9a3a75eac6553f7d35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421340"
---
# <a name="adding-address-book-entries"></a><span data-ttu-id="88c37-103">Hinzufügen von Adressbucheinträgen</span><span class="sxs-lookup"><span data-stu-id="88c37-103">Adding Address Book Entries</span></span>

  
  
<span data-ttu-id="88c37-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88c37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88c37-105">Zum Hinzufügen eines Messagingbenutzers oder einer Verteilerliste zu einem Container ruft ein Client [IAddrBook::NewEntry](iaddrbook-newentry.md) auf, oder ein Anbieter ruft [IMAPISupport::NewEntry](imapisupport-newentry.md) mit der Eintrags-ID des Zielcontainers im  _lpEIDContainer-Parameter_ auf.</span><span class="sxs-lookup"><span data-stu-id="88c37-105">To add a messaging user or distribution list to a container, a client calls [IAddrBook::NewEntry](iaddrbook-newentry.md) or a provider calls [IMAPISupport::NewEntry](imapisupport-newentry.md) with the entry identifier of the target container in the  _lpEIDContainer_ parameter.</span></span> <span data-ttu-id="88c37-106">MAPI ruft wiederum die [IABContainer::CreateEntry-Methode](iabcontainer-createentry.md) des Containers auf, um den Eintrag mithilfe einer einmal erstellten Vorlage aus einer einmal erstellten Tabelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="88c37-106">MAPI in turn calls the container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the entry using a one-off template from a one-off table.</span></span> <span data-ttu-id="88c37-107">Mit einer einmal erstellten Vorlage kann der Client einen neuen Empfänger eines bestimmten Typs erstellen.</span><span class="sxs-lookup"><span data-stu-id="88c37-107">A one-off template allows the client to create a new recipient of a particular type.</span></span> <span data-ttu-id="88c37-108">Die meisten Felder können bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="88c37-108">Most of the fields are editable.</span></span> <span data-ttu-id="88c37-109">Die Vorlage, auf die der  _lpEntryID-Parameter_ verweist, kann eine Vorlage sein, die ihr Anbieter liefert, oder es kann sich um eine Vorlage eines fremden Anbieters, wenn Ihr Anbieter fremde Vorlagen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88c37-109">The template pointed to by the  _lpEntryID_ parameter might be one that your provider supplies or it might be a template from a foreign provider, if your provider supports foreign templates.</span></span> <span data-ttu-id="88c37-110">Implementierungen von **CreateEntry** für Anbieter, die Empfänger aus einer fremden Vorlage erstellen können, sind immer komplexer als Implementierungen für Anbieter, die dies nicht können.</span><span class="sxs-lookup"><span data-stu-id="88c37-110">Implementations of **CreateEntry** for providers that can create recipients from a foreign template are always more complex than implementations for providers that cannot.</span></span> 
  
 <span data-ttu-id="88c37-111">**So implementieren Sie IABContainer::CreateEntry**</span><span class="sxs-lookup"><span data-stu-id="88c37-111">**To implement IABContainer::CreateEntry**</span></span>
  
1. <span data-ttu-id="88c37-112">Bestimmen Sie den Typ des Eintragsbezeichners, der durch den  _lpEntryID-Parameter angegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="88c37-112">Determine the type of entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
2. <span data-ttu-id="88c37-113">Wenn der Eintragsbezeichner eine Vorlage für einen Messagingbenutzer, eine Verteilerliste oder einen Adressbuchcontainer darstellt, die sich im Besitz Ihres Anbieters befinden:</span><span class="sxs-lookup"><span data-stu-id="88c37-113">If the entry identifier represents a template for a messaging user, distribution list, or address book container owned by your provider:</span></span>
    
1. <span data-ttu-id="88c37-114">Erstellen und initialisieren Sie das entsprechende Objekt.</span><span class="sxs-lookup"><span data-stu-id="88c37-114">Create and initialize the appropriate object.</span></span> <span data-ttu-id="88c37-115">Ihr Anbieter kann bei Bedarf einige anfängliche Eigenschaften festlegen.</span><span class="sxs-lookup"><span data-stu-id="88c37-115">Your provider can set some initial properties if desired.</span></span> <span data-ttu-id="88c37-116">Diese Eigenschaften hängen vom Typ des zu erstellenden Empfängers ab.</span><span class="sxs-lookup"><span data-stu-id="88c37-116">These properties depend on the type of recipient being created.</span></span> 
    
2. <span data-ttu-id="88c37-117">Gibt einen Zeiger auf die Implementierung des Objekts im Inhalt des  _lppMAPIPropEntry-Parameters_ zurück.</span><span class="sxs-lookup"><span data-stu-id="88c37-117">Return a pointer to the object's implementation in the contents of the  _lppMAPIPropEntry_ parameter.</span></span> 
    
3. <span data-ttu-id="88c37-118">Wenn der Eintragsbezeichner eine Vorlage für einen fremden Anbieter darstellt:</span><span class="sxs-lookup"><span data-stu-id="88c37-118">If the entry identifier represents a template for a foreign provider:</span></span>
    
1. <span data-ttu-id="88c37-119">Rufen [Sie IMAPISupport::OpenEntry auf,](imapisupport-openentry.md) um das fremde Objekt zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="88c37-119">Call [IMAPISupport::OpenEntry](imapisupport-openentry.md) to open the foreign object.</span></span> 
    
2. <span data-ttu-id="88c37-120">Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Objekts auf, übergeben Sie NULL für das Eigenschaftentagarray, um seine Eigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="88c37-120">Call the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method, passing NULL for the property tag array, to retrieve its properties.</span></span> 
    
3. <span data-ttu-id="88c37-121">Bearbeiten Sie das von **GetProps** zurückgegebene Eigenschaftswertarray, indem Sie das Eigenschaftstag in PR_NULL für alle Eigenschaften ändern, die nicht auf das neue Objekt angewendet werden und nicht übertragen werden sollten.</span><span class="sxs-lookup"><span data-stu-id="88c37-121">Edit the property value array returned from **GetProps** by changing the property tag to PR_NULL for all properties that will not apply to the new object and should not be transferred.</span></span> 
    
4. <span data-ttu-id="88c37-122">Erstellen Sie einen Eintragsbezeichner für das neue Objekt.</span><span class="sxs-lookup"><span data-stu-id="88c37-122">Create an entry identifier for the new object.</span></span> 
    
5. <span data-ttu-id="88c37-123">Erstellen Sie ein neues Objekt des entsprechenden Typs, entweder Messagingbenutzer oder Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="88c37-123">Create a new object of the appropriate type, either messaging user or distribution list.</span></span>
    
6. <span data-ttu-id="88c37-124">Initialisieren Sie das neue Objekt, indem Sie Standardeigenschaften festlegen.</span><span class="sxs-lookup"><span data-stu-id="88c37-124">Initialize the new object by setting default properties.</span></span>
    
7. <span data-ttu-id="88c37-125">Überprüfen Sie, ob das fremde Objekt die **eigenschaft PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88c37-125">Check whether or not the foreign object supports the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> 
    
8. <span data-ttu-id="88c37-126">Wenn das fremde Objekt **PR_TEMPLATEID** unterstützt, rufen Sie [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) auf, um eine Eigenschaftsobjektschnittstelle vom fremden Anbieter abzurufen und den Inhalt des  _lppMAPIPropEntry-Parameters_ auf die Implementierung des fremden Eigenschaftsobjekts zu setzen.</span><span class="sxs-lookup"><span data-stu-id="88c37-126">If the foreign object supports **PR_TEMPLATEID**, call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to retrieve a property object interface from the foreign provider and set the contents of the  _lppMAPIPropEntry_ parameter to the foreign property object implementation.</span></span> 
    
9. <span data-ttu-id="88c37-127">Wenn das fremde Objekt keine **PR_TEMPLATEID,** legen Sie den Inhalt des  _lppMAPIPropEntry-Parameters_ auf die Implementierung des neuen Objekts durch Ihren Anbieter.</span><span class="sxs-lookup"><span data-stu-id="88c37-127">If the foreign object does not support **PR_TEMPLATEID**, set the contents of the  _lppMAPIPropEntry_ parameter to your provider's implementation of the new object.</span></span> 
    
10. <span data-ttu-id="88c37-128">Rufen Sie [die IMAPIProp::SetProps-Methode](imapiprop-setprops.md) des Objekts auf, auf das der  _lppMAPIPropEntry-Parameter_ verweist, um die entsprechenden Eigenschaften aus dem fremden Objekt zu legen.</span><span class="sxs-lookup"><span data-stu-id="88c37-128">Call the [IMAPIProp::SetProps](imapiprop-setprops.md) method of the object pointed to by the  _lppMAPIPropEntry_ parameter to set the appropriate properties from the foreign object.</span></span> 
    

