---
title: Anzeigen der Tabellen Implementierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6990e32445083c3465693df2c1a3d40b980853c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435264"
---
# <a name="display-table-implementation"></a><span data-ttu-id="71bc8-103">Anzeigen der Tabellen Implementierung</span><span class="sxs-lookup"><span data-stu-id="71bc8-103">Display Table Implementation</span></span>

  
  
<span data-ttu-id="71bc8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="71bc8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="71bc8-105">Eine Anzeigetabelle wird verwendet, um ein Eigenschaftenfenster anzuzeigen, ein spezielles Dialogfeld, das aus einem oder mehreren Registerkarten-Eigenschaftenseiten besteht, die für das Anzeigen und möglicherweise Bearbeiten einer oder mehrerer Eigenschaften reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="71bc8-105">A display table is used to show a property sheet, a special dialog box that is composed of one or more tabbed property pages dedicated to displaying and possibly editing one or more properties.</span></span> <span data-ttu-id="71bc8-106">Jeder Anzeigetabelle ist eine [IAttach: IMAPIProp](iattachimapiprop.md) -Schnittstellenimplementierung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="71bc8-106">Associated with every display table is an [IAttach : IMAPIProp](iattachimapiprop.md) interface implementation.</span></span> <span data-ttu-id="71bc8-107">Die [IMAPIProp](imapipropiunknown.md) -Implementierung verwaltet die Eigenschaftendaten, die im Eigenschaftenfenster angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="71bc8-107">The [IMAPIProp](imapipropiunknown.md) implementation maintains the property data that is presented in the property sheet.</span></span> 
  
<span data-ttu-id="71bc8-108">Die Zeilen in einer Anzeigetabelle stellen die Steuerelemente im Eigenschaftenfenster dar.</span><span class="sxs-lookup"><span data-stu-id="71bc8-108">The rows in a display table represent the controls in the property sheet.</span></span> <span data-ttu-id="71bc8-109">Die meisten Steuerelemente können Eigenschaften zugeordnet werden, die mit der **IMAPIProp** -Implementierung verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="71bc8-109">Most controls can be associated with properties maintained with the **IMAPIProp** implementation.</span></span> <span data-ttu-id="71bc8-110">Wenn ein Benutzer den Wert eines änderbaren Steuerelements ändert, wird die entsprechende Eigenschaft aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="71bc8-110">When a user changes the value of a modifiable control, the corresponding property is updated.</span></span> 
  
<span data-ttu-id="71bc8-111">Die Spalten in einer Anzeigetabelle stellen die Eigenschaften des Steuerelements dar, beispielsweise seine Position im Eigenschaftenfenster, dessen Typ, zugehörige Struktur und Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="71bc8-111">The columns in a display table represent properties of the control, such as its position in the property sheet, its type, associated structure, and identifier.</span></span> <span data-ttu-id="71bc8-112">Eine vollständige Liste der erforderlichen Anzeige Tabellenspalten finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="71bc8-112">For a complete list of required display table columns, see [Display Tables](display-tables.md).</span></span>
  
<span data-ttu-id="71bc8-113">MAPI zeigt dem Benutzer einer Clientanwendung ein Eigenschaftenblatt, indem es Eigenschaftswerte aus der **IMAPIProp** -Implementierung liest, die der Anzeigetabelle oder der Anzeigetabelle direkt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="71bc8-113">MAPI displays a property sheet to the user of a client application by reading property values from the **IMAPIProp** implementation associated with the display table or from the display table directly.</span></span> <span data-ttu-id="71bc8-114">Während der Benutzer mit dem Eigenschaftenfenster arbeitet und Werte in den Steuerelementen ändert, ruft MAPI [IMAPIProp::](imapiprop-setprops.md) SetProps auf, um ein geändertes Steuerelement zu speichern, wenn das DT_SET_IMMEDIATE-Flag des Steuerelements festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="71bc8-114">As the user works with the property sheet, changing values in the controls, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to save a changed control if the control's DT_SET_IMMEDIATE flag is set.</span></span> <span data-ttu-id="71bc8-115">Bei Steuerelementen ohne DT_SET_IMMEDIATE werden Änderungen an Eigenschaften gespeichert, wenn der Benutzer das Dialogfeld abschließt, indem er auf die Schaltfläche **OK** oder **jetzt anwenden** klickt.</span><span class="sxs-lookup"><span data-stu-id="71bc8-115">For controls without the DT_SET_IMMEDIATE flag set, changes to properties are saved when the user dismisses the dialog box by clicking the **OK** or **Apply Now** button.</span></span> <span data-ttu-id="71bc8-116">Wenn eine dieser Schaltflächen oder die Schaltfläche **Abbrechen** geklickt wird, entfernt MAPI das Eigenschaftenblatt aus der Ansicht.</span><span class="sxs-lookup"><span data-stu-id="71bc8-116">When either of these buttons or the **Cancel** button is clicked, MAPI removes the property sheet from view.</span></span> 
  
<span data-ttu-id="71bc8-117">MAPI erhält Zugriff auf Ihre Anzeigetabelle, indem Sie die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode in der **IMAPIProp** -Implementierung aufrufen und die **PR_DETAILS_TABLE** ([pidtagdetailstable (](pidtagdetailstable-canonical-property.md))-Eigenschaft anfordert oder in einer Anruf, den Sie an MAPI vorgenommen haben, beispielsweise [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md).</span><span class="sxs-lookup"><span data-stu-id="71bc8-117">MAPI gains access to your display table either by calling the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method in the **IMAPIProp** implementation and requesting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property or by inheriting it in a call that you have made to MAPI, such as [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md).</span></span>
  
<span data-ttu-id="71bc8-118">Die erste Zugriffs Technik wird verwendet, wenn Adressbuchanbieter aufgefordert werden, Details zu Messaging Benutzern oder Verteilerlisten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="71bc8-118">The first access technique is used when address book providers are asked to show details about messaging users or distribution lists.</span></span> <span data-ttu-id="71bc8-119">Die folgende Verarbeitung erfolgt:</span><span class="sxs-lookup"><span data-stu-id="71bc8-119">The following processing occurs:</span></span>
  
1. <span data-ttu-id="71bc8-120">Ein Client ruft die [IAddrBook::D ails](iaddrbook-details.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="71bc8-120">A client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
    
2. <span data-ttu-id="71bc8-121">MAPI Ruft die [IABLogon:: OpenEntry](iablogon-openentry.md) -Methode des Adressbuch Anbieters auf, um auf den Messagingbenutzer zuzugreifen, der den ausgewählten Eintrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="71bc8-121">MAPI calls the address book provider's [IABLogon::OpenEntry](iablogon-openentry.md) method to access the messaging user that represents the selected entry.</span></span> 
    
3. <span data-ttu-id="71bc8-122">MAPI Ruft die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode des Messaging Benutzers auf, um die **PR_DETAILS_TABLE** -Eigenschaft, die Anzeigetabelle für das Dialogfeld Details, abzurufen.</span><span class="sxs-lookup"><span data-stu-id="71bc8-122">MAPI calls the messaging user's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to retrieve the **PR_DETAILS_TABLE** property, the display table for the details dialog box.</span></span> 
    
4. <span data-ttu-id="71bc8-123">MAPI zeigt das Dialogfeld an, verarbeitet die Interaktion des Benutzers mit den Informationen und entfernt es, wenn der Benutzer fertig ist.</span><span class="sxs-lookup"><span data-stu-id="71bc8-123">MAPI displays the dialog box, handling the user's interaction with the information, and removes it when the user has finished.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="71bc8-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71bc8-124">See also</span></span>



[<span data-ttu-id="71bc8-125">MAPI-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="71bc8-125">MAPI Service Providers</span></span>](mapi-service-providers.md)

