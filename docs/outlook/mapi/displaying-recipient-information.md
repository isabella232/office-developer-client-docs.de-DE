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
ms.openlocfilehash: e1c31e5edf702dd8f172f67e7055a96ae4cfff1c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412954"
---
# <a name="displaying-recipient-information"></a><span data-ttu-id="256bb-103">Anzeigen von Empfängerinformationen</span><span class="sxs-lookup"><span data-stu-id="256bb-103">Displaying recipient information</span></span>

<span data-ttu-id="256bb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="256bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="256bb-105">MAPI bietet ein allgemeines Dialogfeld zum Anzeigen von Empfängerdetails.</span><span class="sxs-lookup"><span data-stu-id="256bb-105">MAPI provides a common dialog box for showing recipient details.</span></span> <span data-ttu-id="256bb-106">Das Dialogfeld Details wird aus einer Anzeigetabelle und einer **IMAPIProp-Implementierung** erstellt.</span><span class="sxs-lookup"><span data-stu-id="256bb-106">The details dialog box is created from a display table and an **IMAPIProp** implementation.</span></span> <span data-ttu-id="256bb-107">In der Anzeigetabelle wird die Darstellung der Detailanzeige beschrieben, und die **IMAPIProp-Implementierung** steuert die Daten für den Empfänger.</span><span class="sxs-lookup"><span data-stu-id="256bb-107">The display table describes the appearance of the details display and the **IMAPIProp** implementation controls the data for the recipient.</span></span> <span data-ttu-id="256bb-108">Ihr Anbieter ist für die Bereitstellung der Anzeigetabelle und der **IMAPIProp-Implementierung** für jeden Empfänger verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="256bb-108">Your provider is responsible for supplying the display table and the **IMAPIProp** implementation for each recipient.</span></span> 
  
<span data-ttu-id="256bb-109">Die einfachste Möglichkeit zum Erstellen der Anzeigetabelle besteht in der Definition einer [DTPAGE-Struktur](dtpage.md) und dem Aufrufen [von BuildDisplayTable](builddisplaytable.md).</span><span class="sxs-lookup"><span data-stu-id="256bb-109">The easiest way to create the display table is to define a [DTPAGE](dtpage.md) structure and call [BuildDisplayTable](builddisplaytable.md).</span></span> <span data-ttu-id="256bb-110">Einige Anbieter, insbesondere schreibgeschützte Anbieter, die die Erstellung von einmalempfängern zulassen, verwenden **jedoch IPropData**.</span><span class="sxs-lookup"><span data-stu-id="256bb-110">However, some providers, specifically read-only providers that allow the creation of one-off recipients, use **IPropData**.</span></span> <span data-ttu-id="256bb-111">Die **IMAPIProp-Implementierung** kann ein beliebiger Typ von Eigenschaftsobjekt sein.</span><span class="sxs-lookup"><span data-stu-id="256bb-111">The **IMAPIProp** implementation can be any type of property object.</span></span> 
  
<span data-ttu-id="256bb-112">Es gibt zwei Methoden zum Aufrufen dieses Dialogfelds: [IAddrBook::D etails](iaddrbook-details.md) und [IMAPISupport::D etails](imapisupport-details.md).</span><span class="sxs-lookup"><span data-stu-id="256bb-112">There are two methods for invoking this dialog box: [IAddrBook::Details](iaddrbook-details.md) and [IMAPISupport::Details](imapisupport-details.md).</span></span> <span data-ttu-id="256bb-113">Wenn Ihr Anbieter eine dieser Methoden aufruft, um Details für einen Empfänger an fordern, öffnet MAPI zuerst den Empfänger, indem die [IMAPIContainer::OpenEntry-Methode](imapicontainer-openentry.md) des Containers aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="256bb-113">When your provider calls one of these methods to request details for a recipient, MAPI first opens the recipient by calling its container's [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method.</span></span> <span data-ttu-id="256bb-114">Als Nächstes ruft sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) des **Empfängers** auf, um die PR_DETAILS_TABLE ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) -Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="256bb-114">Next it calls the recipient's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to request the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="256bb-115">**PR_DETAILS_TABLE** ist die Eigenschaft, die die Detailanzeigetabelle eines Empfängers darstellt.</span><span class="sxs-lookup"><span data-stu-id="256bb-115">**PR_DETAILS_TABLE** is the property that represents a recipient's details display table.</span></span> 
  
<span data-ttu-id="256bb-116">Die [IPropData : IMAPIProp-Schnittstelle](ipropdataimapiprop.md) kann zum Überwachen von Änderungen an Steuerelementen für Anzeigetabelle verwendet werden, wie im folgenden Verfahren beschrieben.</span><span class="sxs-lookup"><span data-stu-id="256bb-116">The [IPropData : IMAPIProp](ipropdataimapiprop.md) interface can be used to monitor changes on display table controls as described in the following procedure.</span></span> 
  
## <a name="monitor-changes-to-a-control"></a><span data-ttu-id="256bb-117">Überwachen von Änderungen an einem Steuerelement</span><span class="sxs-lookup"><span data-stu-id="256bb-117">Monitor changes to a control</span></span>
  
1. <span data-ttu-id="256bb-118">Bevor der Benutzer Zugriff auf das Steuerelement erhält, rufen Sie [IPropData::HrSetObjAccess auf,](ipropdata-hrsetobjaccess.md) um den Zugriff des Steuerelements auf IPROP_CLEAN.</span><span class="sxs-lookup"><span data-stu-id="256bb-118">Before the user gains access to the control, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) to set the control's access to IPROP_CLEAN.</span></span> 
    
2. <span data-ttu-id="256bb-119">Zulassen, dass der Benutzer mit dem Dialogfeld arbeitet.</span><span class="sxs-lookup"><span data-stu-id="256bb-119">Allow the user to work with the dialog box.</span></span> 
    
3. <span data-ttu-id="256bb-120">Rufen Sie nach Abschluss des Benutzers [IPropData::HrGetPropAccess auf,](ipropdata-hrgetpropaccess.md) um die aktuelle Zugriffsebene des Steuerelements abzurufen.</span><span class="sxs-lookup"><span data-stu-id="256bb-120">When the user has finished, call [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) to retrieve the current access level of the control.</span></span> 
    
4. <span data-ttu-id="256bb-121">Wenn die Zugriffsebene IPROP_DIRTY ist, hat der Benutzer das Steuerelement geändert.</span><span class="sxs-lookup"><span data-stu-id="256bb-121">If the access level is IPROP_DIRTY, the user has modified the control.</span></span> <span data-ttu-id="256bb-122">Ihr Anbieter sollte:</span><span class="sxs-lookup"><span data-stu-id="256bb-122">Your provider should:</span></span>
    
   - <span data-ttu-id="256bb-123">Rufen [Sie IPropData::HrSetPropAccess auf,](ipropdata-hrsetpropaccess.md) um die Zugriffsebene wieder auf IPROP_CLEAN.</span><span class="sxs-lookup"><span data-stu-id="256bb-123">Call [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) to set the access level back to IPROP_CLEAN.</span></span> 
    
   - <span data-ttu-id="256bb-124">Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Eigenschaftendatenobjekts auf, um die geänderte Eigenschaft abzurufen und durch Aufrufen von [IMAPIProp::SetProps zu aktualisieren.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="256bb-124">Call the property data object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the changed property and update it by calling [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span>
    
5. <span data-ttu-id="256bb-125">Wenn die Zugriffsebene weiterhin IPROP_CLEAN ist, wurde das Steuerelement nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="256bb-125">If the access level is still IPROP_CLEAN, the control has not been modified.</span></span> 
    
<span data-ttu-id="256bb-126">Weitere Informationen zum Erstellen von Anzeigetabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="256bb-126">For more information about creating display tables, see [Display Tables](display-tables.md).</span></span>
  

