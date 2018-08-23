---
title: Anzeigen der Tabellenimplementierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3e31dd7b25b3abf333505c8bde57f61be7a10901
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580607"
---
# <a name="display-table-implementation"></a><span data-ttu-id="c6d01-103">Anzeigen der Tabellenimplementierung</span><span class="sxs-lookup"><span data-stu-id="c6d01-103">Display Table Implementation</span></span>

  
  
<span data-ttu-id="c6d01-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6d01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6d01-105">Zeigt die Tabelle wird verwendet, um ein Eigenschaftenblatt spezielle ein Dialogfeld, das aus der einen oder mehrere im Registerkartenformat Eigenschaftenseiten zum Anzeigen und Bearbeiten von möglicherweise eine oder mehrere Eigenschaften anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c6d01-105">A display table is used to show a property sheet, a special dialog box that is composed of one or more tabbed property pages dedicated to displaying and possibly editing one or more properties.</span></span> <span data-ttu-id="c6d01-106">Verknüpft ist mit jedem Display-Tabelle ist eine [IAttach: IMAPIProp](iattachimapiprop.md) Schnittstelle Implementierung.</span><span class="sxs-lookup"><span data-stu-id="c6d01-106">Associated with every display table is an [IAttach : IMAPIProp](iattachimapiprop.md) interface implementation.</span></span> <span data-ttu-id="c6d01-107">Die Implementierung [IMAPIProp](imapipropiunknown.md) verwaltet die Daten, die im Eigenschaftenfenster angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c6d01-107">The [IMAPIProp](imapipropiunknown.md) implementation maintains the property data that is presented in the property sheet.</span></span> 
  
<span data-ttu-id="c6d01-108">Die Zeilen in einer Tabelle anzeigen darstellen der Steuerelemente im Eigenschaftenfenster.</span><span class="sxs-lookup"><span data-stu-id="c6d01-108">The rows in a display table represent the controls in the property sheet.</span></span> <span data-ttu-id="c6d01-109">Die meisten Steuerelemente können mit der Implementierung **IMAPIProp** verwaltet Eigenschaften zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="c6d01-109">Most controls can be associated with properties maintained with the **IMAPIProp** implementation.</span></span> <span data-ttu-id="c6d01-110">Wenn ein Benutzer den Wert eines Steuerelements änderbare ändert, wird die entsprechende Eigenschaft aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c6d01-110">When a user changes the value of a modifiable control, the corresponding property is updated.</span></span> 
  
<span data-ttu-id="c6d01-111">Die Spalten in einer Tabelle anzeigen dargestellt Eigenschaften des Steuerelements, wie ihre Position im Eigenschaftenfenster, dessen Typ, zugeordnete-Struktur und Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="c6d01-111">The columns in a display table represent properties of the control, such as its position in the property sheet, its type, associated structure, and identifier.</span></span> <span data-ttu-id="c6d01-112">Eine vollständige Liste der erforderlichen Anzeige Tabellenspalten finden Sie unter [Tabellen angezeigt](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c6d01-112">For a complete list of required display table columns, see [Display Tables](display-tables.md).</span></span>
  
<span data-ttu-id="c6d01-113">MAPI wird dem Benutzer von einer Clientanwendung aus einem Eigenschaftenfenster Eigenschaftswerte aus der **IMAPIProp** Implementierung der Anzeige-Tabelle zugeordnet oder aus der Tabelle anzeigen direktem lesen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c6d01-113">MAPI displays a property sheet to the user of a client application by reading property values from the **IMAPIProp** implementation associated with the display table or from the display table directly.</span></span> <span data-ttu-id="c6d01-114">Der Benutzer mit dem Eigenschaftenfenster arbeitet, ruft Ändern der Werte in den Steuerelementen MAPI [IMAPIProp::SetProps](imapiprop-setprops.md) zum Speichern eines geänderten Steuerelements, wenn das Steuerelement DT_SET_IMMEDIATE Flag festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c6d01-114">As the user works with the property sheet, changing values in the controls, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to save a changed control if the control's DT_SET_IMMEDIATE flag is set.</span></span> <span data-ttu-id="c6d01-115">Für Steuerelemente ohne das DT_SET_IMMEDIATE-Flag festgelegt werden Änderungen an Eigenschaften gespeichert, wenn der Benutzer das Dialogfeld schließt, indem Sie auf die Schaltfläche **OK** oder **Übernehmen** .</span><span class="sxs-lookup"><span data-stu-id="c6d01-115">For controls without the DT_SET_IMMEDIATE flag set, changes to properties are saved when the user dismisses the dialog box by clicking the **OK** or **Apply Now** button.</span></span> <span data-ttu-id="c6d01-116">Wenn eine der folgenden Schaltflächen oder die Schaltfläche **Abbrechen** geklickt wird, werden MAPI Eigenschaftenfenster aus der Ansicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="c6d01-116">When either of these buttons or the **Cancel** button is clicked, MAPI removes the property sheet from view.</span></span> 
  
<span data-ttu-id="c6d01-117">MAPI erhält Zugriff auf Ihre zeigt die Tabelle aus, entweder durch Aufrufen der [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode in der Implementierung **IMAPIProp** und die Eigenschaft **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) anfordern oder durch erben ihn in einen Rufen Sie, dass Sie MAPI, wie etwa [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md)vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="c6d01-117">MAPI gains access to your display table either by calling the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method in the **IMAPIProp** implementation and requesting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property or by inheriting it in a call that you have made to MAPI, such as [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md).</span></span>
  
<span data-ttu-id="c6d01-118">Die erste Access Technik wird verwendet, wenn von adressbuchanbietern implementierte zum Anzeigen von Details zu messaging Benutzer oder Verteilerlisten aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="c6d01-118">The first access technique is used when address book providers are asked to show details about messaging users or distribution lists.</span></span> <span data-ttu-id="c6d01-119">Die folgende Vorgänge ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="c6d01-119">The following processing occurs:</span></span>
  
1. <span data-ttu-id="c6d01-120">Ein Client Ruft die [IAddrBook::Details](iaddrbook-details.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c6d01-120">A client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
    
2. <span data-ttu-id="c6d01-121">MAPI-Aufrufen der Adressbuchanbieter [IABLogon::OpenEntry](iablogon-openentry.md) -Methode, um die messaging-Benutzer zugreifen, der den ausgewählten Eintrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="c6d01-121">MAPI calls the address book provider's [IABLogon::OpenEntry](iablogon-openentry.md) method to access the messaging user that represents the selected entry.</span></span> 
    
3. <span data-ttu-id="c6d01-122">MAPI-Aufrufen [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode zum Abrufen der **PR_DETAILS_TABLE** -Eigenschaft der Tabelle anzeigen im Dialogfeld Details der messaging-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="c6d01-122">MAPI calls the messaging user's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to retrieve the **PR_DETAILS_TABLE** property, the display table for the details dialog box.</span></span> 
    
4. <span data-ttu-id="c6d01-123">MAPI zeigt das Dialogfeld behandeln Interaktion mit den Informationen des Benutzers und entfernt sie, wenn der Benutzer abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="c6d01-123">MAPI displays the dialog box, handling the user's interaction with the information, and removes it when the user has finished.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c6d01-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6d01-124">See also</span></span>



[<span data-ttu-id="c6d01-125">MAPI-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="c6d01-125">MAPI Service Providers</span></span>](mapi-service-providers.md)

