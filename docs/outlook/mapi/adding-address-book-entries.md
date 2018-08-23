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
ms.openlocfilehash: d5b2aa2830e2721b9f895b22df12c9d712188625
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590134"
---
# <a name="adding-address-book-entries"></a><span data-ttu-id="5436b-103">Hinzufügen von Adressbucheinträgen</span><span class="sxs-lookup"><span data-stu-id="5436b-103">Adding Address Book Entries</span></span>

  
  
<span data-ttu-id="5436b-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5436b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5436b-105">Aufrufe [IMAPISupport::NewEntry](imapisupport-newentry.md) mit der Eintrags-ID des Zielcontainers in der _LpEIDContainer_ -Parameter einen Container, eine Client-Anrufe [IAddrBook::NewEntry](iaddrbook-newentry.md) oder einen Anbieter einen messaging Benutzer oder eine Verteilerliste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5436b-105">To add a messaging user or distribution list to a container, a client calls [IAddrBook::NewEntry](iaddrbook-newentry.md) or a provider calls [IMAPISupport::NewEntry](imapisupport-newentry.md) with the entry identifier of the target container in the  _lpEIDContainer_ parameter.</span></span> <span data-ttu-id="5436b-106">MAPI-Aufrufen wiederum den Container [IABContainer::CreateEntry](iabcontainer-createentry.md) -Methode, um den Eintrag mithilfe einer einmaligen Vorlage aus einer einmaligen Tabelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5436b-106">MAPI in turn calls the container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the entry using a one-off template from a one-off table.</span></span> <span data-ttu-id="5436b-107">Eine einmalige Vorlage ermöglicht dem Client einen neuen Empfänger eines bestimmten Typs zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5436b-107">A one-off template allows the client to create a new recipient of a particular type.</span></span> <span data-ttu-id="5436b-108">Die meisten Felder können bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="5436b-108">Most of the fields are editable.</span></span> <span data-ttu-id="5436b-109">Die Vorlage, auf das durch den Parameter _LpEntryID_ möglicherweise eine, die vom Dienstanbieter bereitstellt oder einer Vorlage von einem fremden Anbieter, wäre, wenn der Anbieter fremde Vorlagen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5436b-109">The template pointed to by the  _lpEntryID_ parameter might be one that your provider supplies or it might be a template from a foreign provider, if your provider supports foreign templates.</span></span> <span data-ttu-id="5436b-110">Die Implementierung von **CreateEntry** für Anbieter, die Empfänger aus einer fremden Vorlage erstellen können sind immer komplexer als Implementierungen für Anbieter, die nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="5436b-110">Implementations of **CreateEntry** for providers that can create recipients from a foreign template are always more complex than implementations for providers that cannot.</span></span> 
  
 <span data-ttu-id="5436b-111">**Implementieren von IABContainer::CreateEntry**</span><span class="sxs-lookup"><span data-stu-id="5436b-111">**To implement IABContainer::CreateEntry**</span></span>
  
1. <span data-ttu-id="5436b-112">Bestimmen Sie den Typ des Eintrags-ID, die durch den Parameter _LpEntryID_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="5436b-112">Determine the type of entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
2. <span data-ttu-id="5436b-113">Wenn die Eintrags-ID eine Vorlage für eine messaging-Benutzer, Verteilerliste oder im Besitz des Anbieters Adressbuchcontainer darstellt:</span><span class="sxs-lookup"><span data-stu-id="5436b-113">If the entry identifier represents a template for a messaging user, distribution list, or address book container owned by your provider:</span></span>
    
1. <span data-ttu-id="5436b-114">Erstellen Sie und initialisieren Sie das entsprechende Objekt.</span><span class="sxs-lookup"><span data-stu-id="5436b-114">Create and initialize the appropriate object.</span></span> <span data-ttu-id="5436b-115">Vom Dienstanbieter kann einige anfänglichen Eigenschaften festlegen, falls gewünscht.</span><span class="sxs-lookup"><span data-stu-id="5436b-115">Your provider can set some initial properties if desired.</span></span> <span data-ttu-id="5436b-116">Diese Eigenschaften richten sich nach den Typ des zu erstellenden Empfänger.</span><span class="sxs-lookup"><span data-stu-id="5436b-116">These properties depend on the type of recipient being created.</span></span> 
    
2. <span data-ttu-id="5436b-117">Ein Zeiger auf das Objekt Implementierung in den Inhalt des Parameters _LppMAPIPropEntry_ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5436b-117">Return a pointer to the object's implementation in the contents of the  _lppMAPIPropEntry_ parameter.</span></span> 
    
3. <span data-ttu-id="5436b-118">Wenn die Eintrags-ID eine Vorlage für einen fremden Anbieter darstellt:</span><span class="sxs-lookup"><span data-stu-id="5436b-118">If the entry identifier represents a template for a foreign provider:</span></span>
    
1. <span data-ttu-id="5436b-119">Rufen Sie [IMAPISupport::OpenEntry](imapisupport-openentry.md) zum Öffnen des fremden Objekts.</span><span class="sxs-lookup"><span data-stu-id="5436b-119">Call [IMAPISupport::OpenEntry](imapisupport-openentry.md) to open the foreign object.</span></span> 
    
2. <span data-ttu-id="5436b-120">Rufen Sie das Objekt [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode übergeben NULL für die Arrays Tag-Eigenschaft, um seine Eigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5436b-120">Call the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method, passing NULL for the property tag array, to retrieve its properties.</span></span> 
    
3. <span data-ttu-id="5436b-121">Bearbeiten des Eigenschaft Wertearrays von **GetProps** zurückgegeben, indem Sie das Eigenschafts-Tag auf PR_NULL für alle Eigenschaften, die nicht auf das neue Objekt angewendet und sollte nicht übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="5436b-121">Edit the property value array returned from **GetProps** by changing the property tag to PR_NULL for all properties that will not apply to the new object and should not be transferred.</span></span> 
    
4. <span data-ttu-id="5436b-122">Erstellen Sie einen Eintrag Bezeichner für das neue Objekt.</span><span class="sxs-lookup"><span data-stu-id="5436b-122">Create an entry identifier for the new object.</span></span> 
    
5. <span data-ttu-id="5436b-123">Erstellen Sie ein neues Objekt der entsprechenden eingeben, entweder messaging Benutzer oder Verteilerliste aus.</span><span class="sxs-lookup"><span data-stu-id="5436b-123">Create a new object of the appropriate type, either messaging user or distribution list.</span></span>
    
6. <span data-ttu-id="5436b-124">Initialisieren Sie das neue Objekt durch Festlegen der Standardeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5436b-124">Initialize the new object by setting default properties.</span></span>
    
7. <span data-ttu-id="5436b-125">Überprüfen Sie, ob die fremden Objekts die Eigenschaft **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5436b-125">Check whether or not the foreign object supports the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> 
    
8. <span data-ttu-id="5436b-126">Wenn die fremden Objekts **PR_TEMPLATEID**unterstützt, rufen Sie [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) zum Abrufen einer Eigenschaft Objektschnittstelle aus der fremden Anbieter und Festlegen von den Inhalt des Parameters _LppMAPIPropEntry_ für die foreign-Eigenschaft objektimplementierung.</span><span class="sxs-lookup"><span data-stu-id="5436b-126">If the foreign object supports **PR_TEMPLATEID**, call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to retrieve a property object interface from the foreign provider and set the contents of the  _lppMAPIPropEntry_ parameter to the foreign property object implementation.</span></span> 
    
9. <span data-ttu-id="5436b-127">Wenn die fremden Objekts **PR_TEMPLATEID**nicht unterstützt, legen Sie den Inhalt des Parameters _LppMAPIPropEntry_ an Ihren Anbieter die Implementierung des neuen Objekts.</span><span class="sxs-lookup"><span data-stu-id="5436b-127">If the foreign object does not support **PR_TEMPLATEID**, set the contents of the  _lppMAPIPropEntry_ parameter to your provider's implementation of the new object.</span></span> 
    
10. <span data-ttu-id="5436b-128">Rufen Sie die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode des Objekts auf das durch den Parameter _LppMAPIPropEntry_ , um die entsprechenden Eigenschaften aus der fremden Objekts festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5436b-128">Call the [IMAPIProp::SetProps](imapiprop-setprops.md) method of the object pointed to by the  _lppMAPIPropEntry_ parameter to set the appropriate properties from the foreign object.</span></span> 
    

