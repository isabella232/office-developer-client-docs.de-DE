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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331878"
---
# <a name="adding-address-book-entries"></a><span data-ttu-id="a9305-103">Hinzufügen von Adressbucheinträgen</span><span class="sxs-lookup"><span data-stu-id="a9305-103">Adding Address Book Entries</span></span>

  
  
<span data-ttu-id="a9305-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9305-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9305-105">Um einem Container einen Messagingbenutzer oder eine Verteilerliste hinzuzufügen, Ruft ein Client [IAddrBook:: Neuentry](iaddrbook-newentry.md) auf, oder ein Anbieter ruft [IMAPISupport::](imapisupport-newentry.md) neueintrags mit dem Eintragsbezeichner des Zielcontainers im _lpEIDContainer_ -Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="a9305-105">To add a messaging user or distribution list to a container, a client calls [IAddrBook::NewEntry](iaddrbook-newentry.md) or a provider calls [IMAPISupport::NewEntry](imapisupport-newentry.md) with the entry identifier of the target container in the  _lpEIDContainer_ parameter.</span></span> <span data-ttu-id="a9305-106">MAPI ruft wiederum die [IABContainer:: CreateEntry](iabcontainer-createentry.md) -Methode des Containers auf, um den Eintrag mithilfe einer einmaligen Vorlage aus einer einmaligen Tabelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a9305-106">MAPI in turn calls the container's [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the entry using a one-off template from a one-off table.</span></span> <span data-ttu-id="a9305-107">Eine einmalige Vorlage ermöglicht es dem Client, einen neuen Empfänger eines bestimmten Typs zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a9305-107">A one-off template allows the client to create a new recipient of a particular type.</span></span> <span data-ttu-id="a9305-108">Die meisten Felder können bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="a9305-108">Most of the fields are editable.</span></span> <span data-ttu-id="a9305-109">Die Vorlage, auf die durch den _lpEntryID_ -Parameter verwiesen wird, kann möglicherweise von Ihrem Anbieter bereitgestellt werden, oder es kann sich um eine Vorlage eines fremden Anbieters handeln, wenn Ihr Anbieter fremde Vorlagen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a9305-109">The template pointed to by the  _lpEntryID_ parameter might be one that your provider supplies or it might be a template from a foreign provider, if your provider supports foreign templates.</span></span> <span data-ttu-id="a9305-110">Implementierungen \*\*\*\* von CreateEntry für Anbieter, die Empfänger aus einer fremden Vorlage erstellen können, sind immer komplexer als Implementierungen für Anbieter, die nicht.</span><span class="sxs-lookup"><span data-stu-id="a9305-110">Implementations of **CreateEntry** for providers that can create recipients from a foreign template are always more complex than implementations for providers that cannot.</span></span> 
  
 <span data-ttu-id="a9305-111">**So implementieren Sie IABContainer:: createEntry**</span><span class="sxs-lookup"><span data-stu-id="a9305-111">**To implement IABContainer::CreateEntry**</span></span>
  
1. <span data-ttu-id="a9305-112">Bestimmen des vom _lpEntryID_ -Parameter angegebenen Typs der Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="a9305-112">Determine the type of entry identifier specified by the  _lpEntryID_ parameter.</span></span> 
    
2. <span data-ttu-id="a9305-113">Wenn die Eintrags-ID eine Vorlage für einen Messagingbenutzer, eine Verteilerliste oder einen Adressbuchcontainer darstellt, die im Besitz Ihres Anbieters sind:</span><span class="sxs-lookup"><span data-stu-id="a9305-113">If the entry identifier represents a template for a messaging user, distribution list, or address book container owned by your provider:</span></span>
    
1. <span data-ttu-id="a9305-114">Erstellen und initialisieren Sie das entsprechende Objekt.</span><span class="sxs-lookup"><span data-stu-id="a9305-114">Create and initialize the appropriate object.</span></span> <span data-ttu-id="a9305-115">Bei Bedarf kann Ihr Anbieter einige anfängliche Eigenschaften festlegen.</span><span class="sxs-lookup"><span data-stu-id="a9305-115">Your provider can set some initial properties if desired.</span></span> <span data-ttu-id="a9305-116">Diese Eigenschaften hängen vom Typ des zu erstellenden Empfängers ab.</span><span class="sxs-lookup"><span data-stu-id="a9305-116">These properties depend on the type of recipient being created.</span></span> 
    
2. <span data-ttu-id="a9305-117">Zurückgeben eines Zeigers auf die Implementierung des Objekts im Inhalt des _lppMAPIPropEntry_ -Parameters.</span><span class="sxs-lookup"><span data-stu-id="a9305-117">Return a pointer to the object's implementation in the contents of the  _lppMAPIPropEntry_ parameter.</span></span> 
    
3. <span data-ttu-id="a9305-118">Wenn die Eintrags-ID eine Vorlage für einen fremden Anbieter darstellt:</span><span class="sxs-lookup"><span data-stu-id="a9305-118">If the entry identifier represents a template for a foreign provider:</span></span>
    
1. <span data-ttu-id="a9305-119">Rufen Sie [IMAPISupport:: OpenEntry](imapisupport-openentry.md) auf, um das fremdobjekt zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a9305-119">Call [IMAPISupport::OpenEntry](imapisupport-openentry.md) to open the foreign object.</span></span> 
    
2. <span data-ttu-id="a9305-120">Rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des Objekts auf, und übergeben Sie NULL für das Property-Tag-Array, um dessen Eigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a9305-120">Call the object's [IMAPIProp::GetProps](imapiprop-getprops.md) method, passing NULL for the property tag array, to retrieve its properties.</span></span> 
    
3. <span data-ttu-id="a9305-121">Bearbeiten Sie das von getProps \*\*\*\* zurückgegebene Eigenschafts Wertarray, indem Sie das Property-Tag in PR_NULL für alle Eigenschaften ändern, die für das neue Objekt nicht gelten und nicht übertragen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a9305-121">Edit the property value array returned from **GetProps** by changing the property tag to PR_NULL for all properties that will not apply to the new object and should not be transferred.</span></span> 
    
4. <span data-ttu-id="a9305-122">Erstellen Sie eine Eintrags-ID für das neue Objekt.</span><span class="sxs-lookup"><span data-stu-id="a9305-122">Create an entry identifier for the new object.</span></span> 
    
5. <span data-ttu-id="a9305-123">Erstellen Sie ein neues Objekt vom entsprechenden Typ, entweder Messaging-Benutzer oder Verteilerliste.</span><span class="sxs-lookup"><span data-stu-id="a9305-123">Create a new object of the appropriate type, either messaging user or distribution list.</span></span>
    
6. <span data-ttu-id="a9305-124">Initialisieren Sie das neue Objekt, indem Sie die Standardeigenschaften festlegen.</span><span class="sxs-lookup"><span data-stu-id="a9305-124">Initialize the new object by setting default properties.</span></span>
    
7. <span data-ttu-id="a9305-125">Überprüfen Sie, ob das Foreign-Objekt die **PR_TEMPLATEID** ([pidtagtemplateid (](pidtagtemplateid-canonical-property.md))-Eigenschaft unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a9305-125">Check whether or not the foreign object supports the **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) property.</span></span> 
    
8. <span data-ttu-id="a9305-126">Wenn das Foreign-Objekt **PR_TEMPLATEID**unterstützt, rufen Sie [IMAPISupport::](imapisupport-opentemplateid.md) opentemplatecode auf, um eine Property-Objekt Schnittstelle vom fremden Anbieter abzurufen, und legen Sie den Inhalt des _lppMAPIPropEntry_ -Parameters auf die Foreign-Eigenschaft fest. Objekt Implementierung.</span><span class="sxs-lookup"><span data-stu-id="a9305-126">If the foreign object supports **PR_TEMPLATEID**, call [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) to retrieve a property object interface from the foreign provider and set the contents of the  _lppMAPIPropEntry_ parameter to the foreign property object implementation.</span></span> 
    
9. <span data-ttu-id="a9305-127">Wenn das Foreign-Objekt **PR_TEMPLATEID**nicht unterstützt, legen Sie die Inhalte des _lppMAPIPropEntry_ -Parameters auf die Implementierung des neuen Objekts durch den Anbieter fest.</span><span class="sxs-lookup"><span data-stu-id="a9305-127">If the foreign object does not support **PR_TEMPLATEID**, set the contents of the  _lppMAPIPropEntry_ parameter to your provider's implementation of the new object.</span></span> 
    
10. <span data-ttu-id="a9305-128">Rufen Sie die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode des Objekts auf, auf das durch den _lppMAPIPropEntry_ -Parameter verwiesen wird, um die entsprechenden Eigenschaften aus dem Foreign-Objekt festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a9305-128">Call the [IMAPIProp::SetProps](imapiprop-setprops.md) method of the object pointed to by the  _lppMAPIPropEntry_ parameter to set the appropriate properties from the foreign object.</span></span> 
    

