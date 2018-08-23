---
title: Anzeigen von Empfängerinformationen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4610d9e643541e39144f2af86a2d64928b8e9ca7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591289"
---
# <a name="displaying-recipient-information"></a><span data-ttu-id="18789-103">Anzeigen von Empfängerinformationen</span><span class="sxs-lookup"><span data-stu-id="18789-103">Displaying recipient information</span></span>

<span data-ttu-id="18789-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18789-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18789-105">MAPI bietet ein Standarddialogfeld für Empfänger-Details anzeigen.</span><span class="sxs-lookup"><span data-stu-id="18789-105">MAPI provides a common dialog box for showing recipient details.</span></span> <span data-ttu-id="18789-106">Im Dialogfeld Details der wird aus einer Tabelle anzeigen und eine Implementierung **IMAPIProp** erstellt.</span><span class="sxs-lookup"><span data-stu-id="18789-106">The details dialog box is created from a display table and an **IMAPIProp** implementation.</span></span> <span data-ttu-id="18789-107">Zeigt die Tabelle erläutert, wie unter "Details" und die Implementierung **IMAPIProp** steuert die Daten für den Empfänger.</span><span class="sxs-lookup"><span data-stu-id="18789-107">The display table describes the appearance of the details display and the **IMAPIProp** implementation controls the data for the recipient.</span></span> <span data-ttu-id="18789-108">Der Anbieter ist verantwortlich für die Angabe der Tabelle anzeigen und die Implementierung **IMAPIProp** für jeden Empfänger.</span><span class="sxs-lookup"><span data-stu-id="18789-108">Your provider is responsible for supplying the display table and the **IMAPIProp** implementation for each recipient.</span></span> 
  
<span data-ttu-id="18789-109">Die einfachste Möglichkeit zum Erstellen der Anzeige-Tabelle ist eine Struktur [DTPAGE](dtpage.md) definieren und Aufrufen von [BuildDisplayTable](builddisplaytable.md).</span><span class="sxs-lookup"><span data-stu-id="18789-109">The easiest way to create the display table is to define a [DTPAGE](dtpage.md) structure and call [BuildDisplayTable](builddisplaytable.md).</span></span> <span data-ttu-id="18789-110">Verwenden Sie einige Anbieter, insbesondere schreibgeschützte Anbieter, mit denen die Erstellung von einmaligen Empfängern können jedoch **IPropData**.</span><span class="sxs-lookup"><span data-stu-id="18789-110">However, some providers, specifically read-only providers that allow the creation of one-off recipients, use **IPropData**.</span></span> <span data-ttu-id="18789-111">Die Implementierung **IMAPIProp** kann jede Art von Property-Objekt sein.</span><span class="sxs-lookup"><span data-stu-id="18789-111">The **IMAPIProp** implementation can be any type of property object.</span></span> 
  
<span data-ttu-id="18789-112">Es gibt zwei Methoden zum Aufrufen dieses Dialogfeld: [IAddrBook::Details](iaddrbook-details.md) und [IMAPISupport::Details](imapisupport-details.md).</span><span class="sxs-lookup"><span data-stu-id="18789-112">There are two methods for invoking this dialog box: [IAddrBook::Details](iaddrbook-details.md) and [IMAPISupport::Details](imapisupport-details.md).</span></span> <span data-ttu-id="18789-113">Wenn der Anbieter eine der folgenden Methoden zum Anfordern von Informationen für einen Empfänger aufruft, öffnet MAPI zuerst den Empfänger durch Aufrufen des Containers [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="18789-113">When your provider calls one of these methods to request details for a recipient, MAPI first opens the recipient by calling its container's [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method.</span></span> <span data-ttu-id="18789-114">Danach wird der Aufgabenliste des Empfängers [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode, um anzufordern, die **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="18789-114">Next it calls the recipient's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to request the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="18789-115">**PR_DETAILS_TABLE** ist die Eigenschaft, die einen Empfänger Details zeigt die Tabelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="18789-115">**PR_DETAILS_TABLE** is the property that represents a recipient's details display table.</span></span> 
  
<span data-ttu-id="18789-116">Die [IPropData: IMAPIProp](ipropdataimapiprop.md) -Schnittstelle verwendet werden, um Änderungen auf die Tabellensteuerelemente anzeigen zu überwachen, wie im folgenden Verfahren beschrieben.</span><span class="sxs-lookup"><span data-stu-id="18789-116">The [IPropData : IMAPIProp](ipropdataimapiprop.md) interface can be used to monitor changes on display table controls as described in the following procedure.</span></span> 
  
## <a name="monitor-changes-to-a-control"></a><span data-ttu-id="18789-117">Überwachen von Änderungen an ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="18789-117">Monitor changes to a control</span></span>
  
1. <span data-ttu-id="18789-118">Bevor der Benutzer Zugriff auf das Steuerelement erhält, rufen Sie [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) , um die Steuerung des Zugriffs auf IPROP_CLEAN festzulegen auf.</span><span class="sxs-lookup"><span data-stu-id="18789-118">Before the user gains access to the control, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) to set the control's access to IPROP_CLEAN.</span></span> 
    
2. <span data-ttu-id="18789-119">Ermöglicht es dem Benutzer das Dialogfeld entwickelt.</span><span class="sxs-lookup"><span data-stu-id="18789-119">Allow the user to work with the dialog box.</span></span> 
    
3. <span data-ttu-id="18789-120">Wenn der Benutzer beendet wurde, rufen Sie [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) zum Abrufen der aktuellen Zugriffsebene des Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="18789-120">When the user has finished, call [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) to retrieve the current access level of the control.</span></span> 
    
4. <span data-ttu-id="18789-121">Wenn die Zugriffsebene IPROP_DIRTY ist, hat der Benutzer das Steuerelement geändert.</span><span class="sxs-lookup"><span data-stu-id="18789-121">If the access level is IPROP_DIRTY, the user has modified the control.</span></span> <span data-ttu-id="18789-122">Der Anbieter sollte:</span><span class="sxs-lookup"><span data-stu-id="18789-122">Your provider should:</span></span>
    
   - <span data-ttu-id="18789-123">Rufen Sie wieder auf IPROP_CLEAN [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) , um den Zugriff festzulegen.</span><span class="sxs-lookup"><span data-stu-id="18789-123">Call [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) to set the access level back to IPROP_CLEAN.</span></span> 
    
   - <span data-ttu-id="18789-124">Rufen Sie die Eigenschaft Datenobjekt [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode, um die geänderte Eigenschaft abgerufen und durch Aufrufen von [IMAPIProp::SetProps](imapiprop-setprops.md)zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="18789-124">Call the property data object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the changed property and update it by calling [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span>
    
5. <span data-ttu-id="18789-125">Wenn die Zugriffsebene noch IPROP_CLEAN ist, wurde das Steuerelement nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="18789-125">If the access level is still IPROP_CLEAN, the control has not been modified.</span></span> 
    
<span data-ttu-id="18789-126">Weitere Informationen zum Erstellen von Tabellen anzeigen finden Sie unter [Tabellen angezeigt](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="18789-126">For more information about creating display tables, see [Display Tables](display-tables.md).</span></span>
  

