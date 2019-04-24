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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337037"
---
# <a name="displaying-recipient-information"></a><span data-ttu-id="50a86-103">Anzeigen von Empfängerinformationen</span><span class="sxs-lookup"><span data-stu-id="50a86-103">Displaying recipient information</span></span>

<span data-ttu-id="50a86-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50a86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50a86-105">MAPI bietet ein allgemeines Dialogfeld zum Anzeigen von Empfängerdetails.</span><span class="sxs-lookup"><span data-stu-id="50a86-105">MAPI provides a common dialog box for showing recipient details.</span></span> <span data-ttu-id="50a86-106">Das Dialogfeld Details wird aus einer Anzeigetabelle und einer **IMAPIProp** -Implementierung erstellt.</span><span class="sxs-lookup"><span data-stu-id="50a86-106">The details dialog box is created from a display table and an **IMAPIProp** implementation.</span></span> <span data-ttu-id="50a86-107">In der Anzeigetabelle wird die Darstellung der Details angezeigt, und die **IMAPIProp** -Implementierung steuert die Daten für den Empfänger.</span><span class="sxs-lookup"><span data-stu-id="50a86-107">The display table describes the appearance of the details display and the **IMAPIProp** implementation controls the data for the recipient.</span></span> <span data-ttu-id="50a86-108">Ihr Anbieter ist für die Bereitstellung der Anzeigetabelle und der **IMAPIProp** -Implementierung für jeden Empfänger verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="50a86-108">Your provider is responsible for supplying the display table and the **IMAPIProp** implementation for each recipient.</span></span> 
  
<span data-ttu-id="50a86-109">Am einfachsten können Sie die Anzeigetabelle erstellen, indem Sie eine [DTPAGE](dtpage.md) -Struktur definieren und [BuildDisplayTable](builddisplaytable.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="50a86-109">The easiest way to create the display table is to define a [DTPAGE](dtpage.md) structure and call [BuildDisplayTable](builddisplaytable.md).</span></span> <span data-ttu-id="50a86-110">Einige Anbieter, insbesondere schreibgeschützte Anbieter, die das Erstellen von einmaligen Empfängern zulassen, verwenden jedoch **IPropData**.</span><span class="sxs-lookup"><span data-stu-id="50a86-110">However, some providers, specifically read-only providers that allow the creation of one-off recipients, use **IPropData**.</span></span> <span data-ttu-id="50a86-111">Bei der **IMAPIProp** -Implementierung kann es sich um einen beliebigen Typ von Property-Objekt handeln.</span><span class="sxs-lookup"><span data-stu-id="50a86-111">The **IMAPIProp** implementation can be any type of property object.</span></span> 
  
<span data-ttu-id="50a86-112">Es gibt zwei Methoden zum Aufrufen dieses Dialogfelds: [IAddrBook::D ails](iaddrbook-details.md) und [IMAPISupport::D ails](imapisupport-details.md).</span><span class="sxs-lookup"><span data-stu-id="50a86-112">There are two methods for invoking this dialog box: [IAddrBook::Details](iaddrbook-details.md) and [IMAPISupport::Details](imapisupport-details.md).</span></span> <span data-ttu-id="50a86-113">Wenn der Anbieter eine dieser Methoden zum Anfordern von Details für einen Empfänger aufruft, wird der Empfänger von MAPI zunächst durch Aufrufen der [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md) -Methode des Containers geöffnet.</span><span class="sxs-lookup"><span data-stu-id="50a86-113">When your provider calls one of these methods to request details for a recipient, MAPI first opens the recipient by calling its container's [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method.</span></span> <span data-ttu-id="50a86-114">Als nächstes wird die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode des Empfängers aufgerufen, um die **PR_DETAILS_TABLE** ([pidtagdetailstable (](pidtagdetailstable-canonical-property.md))-Eigenschaft anzufordern.</span><span class="sxs-lookup"><span data-stu-id="50a86-114">Next it calls the recipient's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to request the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="50a86-115">**PR_DETAILS_TABLE** ist die Eigenschaft, die die Details der Anzeigetabelle eines Empfängers darstellt.</span><span class="sxs-lookup"><span data-stu-id="50a86-115">**PR_DETAILS_TABLE** is the property that represents a recipient's details display table.</span></span> 
  
<span data-ttu-id="50a86-116">Die [IPropData: IMAPIProp](ipropdataimapiprop.md) -Schnittstelle kann verwendet werden, um Änderungen an Anzeige Tabellensteuerelemente zu überwachen, wie im folgenden Verfahren beschrieben.</span><span class="sxs-lookup"><span data-stu-id="50a86-116">The [IPropData : IMAPIProp](ipropdataimapiprop.md) interface can be used to monitor changes on display table controls as described in the following procedure.</span></span> 
  
## <a name="monitor-changes-to-a-control"></a><span data-ttu-id="50a86-117">Überwachen von Änderungen an einem Steuerelement</span><span class="sxs-lookup"><span data-stu-id="50a86-117">Monitor changes to a control</span></span>
  
1. <span data-ttu-id="50a86-118">Bevor der Benutzer Zugriff auf das Steuerelement erhält, rufen Sie [IPropData:: HrSetObjAccess](ipropdata-hrsetobjaccess.md) auf, um den Zugriff auf IPROP_CLEAN für den Steuerelement festzulegen.</span><span class="sxs-lookup"><span data-stu-id="50a86-118">Before the user gains access to the control, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) to set the control's access to IPROP_CLEAN.</span></span> 
    
2. <span data-ttu-id="50a86-119">Ermöglicht dem Benutzer das Arbeiten mit dem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="50a86-119">Allow the user to work with the dialog box.</span></span> 
    
3. <span data-ttu-id="50a86-120">Wenn der Benutzer fertig ist, rufen Sie [IPropData:: HrGetPropAccess](ipropdata-hrgetpropaccess.md) auf, um die aktuelle Zugriffsebene des Steuerelements abzurufen.</span><span class="sxs-lookup"><span data-stu-id="50a86-120">When the user has finished, call [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) to retrieve the current access level of the control.</span></span> 
    
4. <span data-ttu-id="50a86-121">Wenn die Zugriffsebene IPROP_DIRTY ist, hat der Benutzer das Steuerelement geändert.</span><span class="sxs-lookup"><span data-stu-id="50a86-121">If the access level is IPROP_DIRTY, the user has modified the control.</span></span> <span data-ttu-id="50a86-122">Ihr Anbieter sollte:</span><span class="sxs-lookup"><span data-stu-id="50a86-122">Your provider should:</span></span>
    
   - <span data-ttu-id="50a86-123">Rufen Sie [IPropData:: HrSetPropAccess](ipropdata-hrsetpropaccess.md) auf, um die Zugriffsebene auf IPROP_CLEAN zurückzustellen.</span><span class="sxs-lookup"><span data-stu-id="50a86-123">Call [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) to set the access level back to IPROP_CLEAN.</span></span> 
    
   - <span data-ttu-id="50a86-124">Rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des Property-Datenobjekts auf, um die geänderte Eigenschaft abzurufen und durch Aufrufen von [IMAPIProp::](imapiprop-setprops.md)SetProps zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="50a86-124">Call the property data object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the changed property and update it by calling [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span>
    
5. <span data-ttu-id="50a86-125">Wenn die Zugriffsebene immer noch IPROP_CLEAN ist, wurde das Steuerelement nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="50a86-125">If the access level is still IPROP_CLEAN, the control has not been modified.</span></span> 
    
<span data-ttu-id="50a86-126">Weitere Informationen zum Erstellen von Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="50a86-126">For more information about creating display tables, see [Display Tables](display-tables.md).</span></span>
  

