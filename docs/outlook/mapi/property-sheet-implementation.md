---
title: Implementierung von Eigenschaftenblatt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f3475206-0237-4b5b-8efd-abd5d5e0b6c3
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3f1c6497a182231645691f669d8900d33b495503
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430049"
---
# <a name="property-sheet-implementation"></a><span data-ttu-id="88861-103">Implementierung von Eigenschaftenblatt</span><span class="sxs-lookup"><span data-stu-id="88861-103">Property Sheet Implementation</span></span>

  
  
<span data-ttu-id="88861-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88861-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88861-105">Ein Eigenschaftenblatt ist ein Dialogfeld zum Anzeigen der Eigenschaften eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="88861-105">A property sheet is a dialog box for displaying the properties of an object.</span></span> <span data-ttu-id="88861-106">Die Eigenschaften können schreibgeschützt sein, sodass der Benutzer sie nur anzeigen oder lesen/schreiben kann, sodass der Benutzer Änderungen vornehmen kann.</span><span class="sxs-lookup"><span data-stu-id="88861-106">The properties can be read-only, enabling the user only to view them, or read/write, enabling the user to make changes.</span></span> <span data-ttu-id="88861-107">Ein Eigenschaftenblatt enthält ein oder mehrere überlappende untergeordnete Fenster, die als Seiten bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="88861-107">A property sheet contains one or more overlapping child windows called pages.</span></span> <span data-ttu-id="88861-108">Jede Seite enthält Steuerelementfenster zum Festlegen einer Gruppe verwandter Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="88861-108">Each page contains control windows for setting a group of related properties.</span></span> <span data-ttu-id="88861-109">Benutzer navigieren von Seite zu Seite, indem sie eine Registerkarte auswählen, die die entsprechende Seite in den Vordergrund des Eigenschaftenblatts rückt.</span><span class="sxs-lookup"><span data-stu-id="88861-109">Users navigate from page to page by selecting a tab that brings the corresponding page to the foreground of the property sheet.</span></span>
  
<span data-ttu-id="88861-110">Dienstanbieter müssen ein Eigenschaftenblatt implementieren, das einen minimalen Satz von Eigenschaften im Zusammenhang mit der Konfiguration im Nachrichtendienst anzeigt.</span><span class="sxs-lookup"><span data-stu-id="88861-110">Service providers must implement a property sheet that displays a minimal set of properties related to configuration in the message service.</span></span> <span data-ttu-id="88861-111">Wenn Sie zulassen, dass diese Nachrichtendiensteigenschaften geändert werden, können Sie entweder Benutzern von Clientanwendungen, z. B. der Systemsteuerung, erlauben, die Änderungen vorzunehmen oder die Änderungen programmgesteuert zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="88861-111">If you allow these message service properties to be changed, you can either allow users of client applications, such as the Control Panel, to make the changes or implement the changes programmatically.</span></span> <span data-ttu-id="88861-112">Das Implementieren von Eigenschaftenblättern zum Anzeigen und Bearbeiten anderer Eigenschaftentypen ist optional.</span><span class="sxs-lookup"><span data-stu-id="88861-112">Implementing property sheets to display and edit other types of properties is optional.</span></span> 
  
<span data-ttu-id="88861-113">In der Regel müssen Sie in den folgenden Situationen ein Eigenschaftenblatt anzeigen:</span><span class="sxs-lookup"><span data-stu-id="88861-113">Typically, you will need to display a property sheet in the following situations:</span></span>
  
- <span data-ttu-id="88861-114">Wenn ein Client die [IMAPIStatus::SettingsDialog-Methode des Statusobjekts aufruft.](imapistatus-settingsdialog.md)</span><span class="sxs-lookup"><span data-stu-id="88861-114">When a client calls your status object's [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method.</span></span> 
    
- <span data-ttu-id="88861-115">Wenn MAPI die Anmeldemethode des Anbieterobjekts aufruft.</span><span class="sxs-lookup"><span data-stu-id="88861-115">When MAPI calls your provider object's logon method.</span></span>
    
- <span data-ttu-id="88861-116">Wenn MAPI die Einstiegspunktfunktion für den Nachrichtendienst Ihres Anbieters aufruft.</span><span class="sxs-lookup"><span data-stu-id="88861-116">When MAPI calls the entry point function for your provider's message service.</span></span>
    
<span data-ttu-id="88861-117">Transportanbieter implementieren auch Eigenschaftenblätter, um Eigenschaften im Zusammenhang mit Nachrichtenoptionen anzuzeigen, und Adressbuchanbieter implementieren Eigenschaftenblätter, um detaillierte Informationen zu Messagingbenutzern und Verteilerlisten, erweiterten Suchkriterien und Vorlagen für die Eingabe neuer Benutzer anzuzeigen und zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="88861-117">Transport providers also implement property sheets to display properties related to message options, and address book providers implement property sheets to view and edit detailed information about messaging users and distribution lists, advanced search criteria, and templates for entering new users.</span></span>
  
<span data-ttu-id="88861-118">Sie können eine der folgenden drei Techniken verwenden, um ein Eigenschaftenblatt zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="88861-118">You can use one of the following three techniques to create a property sheet:</span></span>
  
- <span data-ttu-id="88861-119">Manuell, wie in einem beliebigen Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="88861-119">Manually, as you would any dialog box.</span></span>
    
- <span data-ttu-id="88861-120">Verwenden Sie das allgemeine Steuerelement des Eigenschaftenblatts im Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="88861-120">By using the property sheet common control provided in the Windows SDK.</span></span>
    
- <span data-ttu-id="88861-121">Mithilfe einer MAPI-Anzeigetabelle.</span><span class="sxs-lookup"><span data-stu-id="88861-121">By using a MAPI display table.</span></span>
    
<span data-ttu-id="88861-122">Anbieter sollten die letzte Option auswählen (Erstellen eines Eigenschaftenblatts mithilfe einer Anzeigetabelle).</span><span class="sxs-lookup"><span data-stu-id="88861-122">Providers should choose the last option (create a property sheet by using a display table).</span></span> <span data-ttu-id="88861-123">Dies ist die einfachste Option, da sie die Arbeit mit der Benutzeroberfläche Windows entfällt.</span><span class="sxs-lookup"><span data-stu-id="88861-123">This is the simplest option because it eliminates the need to work with the Windows user interface.</span></span> 
  
<span data-ttu-id="88861-124">Verwenden Sie das folgende Verfahren, um ein Eigenschaftenblatt zu implementieren, das aus einer Anzeigetabelle für die Nachrichtendiensteigenschaften erstellt wurde:</span><span class="sxs-lookup"><span data-stu-id="88861-124">To implement a property sheet built from a display table for your message service properties, use the following procedure:</span></span>
  
1. <span data-ttu-id="88861-125">Rufen [Sie IMAPISupport::OpenProfileSection auf,](imapisupport-openprofilesection.md) um einen Abschnitt im aktuellen Profil zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="88861-125">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) to open a section in the current profile.</span></span> <span data-ttu-id="88861-126">Übergeben Sie [Ihre MAPIUID](mapiuid.md) oder NULL, um den Profilabschnitt Ihres Anbieters zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="88861-126">Pass your [MAPIUID](mapiuid.md) or NULL to open your provider's profile section.</span></span> 
    
2. <span data-ttu-id="88861-127">Rufen [Sie CreateIProp auf,](createiprop.md) um ein Eigenschaftsdatenobjekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="88861-127">Call [CreateIProp](createiprop.md) to create a property data object.</span></span> 
    
3. <span data-ttu-id="88861-128">Rufen Sie die [IMAPIProp::CopyTo-Methode](imapiprop-copyto.md) des Profilabschnitts auf, um alle Eigenschaften des Abschnitts in das Eigenschaftsdatenobjekt zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="88861-128">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy all of the section's properties to the property data object.</span></span> 
    
4. <span data-ttu-id="88861-129">Erstellen Sie eine Anzeigetabelle, indem Sie eine oder mehrere [DTPAGE-Strukturen](dtpage.md) erstellen, die die Steuerelemente beschreiben, die auf dem Eigenschaftenblatt angezeigt werden sollen, und indem Sie die [BuildDisplayTable-Funktion](builddisplaytable.md) aufrufen oder benutzerdefinierten Code implementieren.</span><span class="sxs-lookup"><span data-stu-id="88861-129">Create a display table either by building one or more [DTPAGE](dtpage.md) structures that describe the controls to appear on the property sheet and calling the [BuildDisplayTable](builddisplaytable.md) function, or by implementing custom code.</span></span> 
    
5. <span data-ttu-id="88861-130">Rufen [Sie IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) auf, um ein Eigenschaftenblatt mit den kopierten Eigenschaften anzeigen zu können.</span><span class="sxs-lookup"><span data-stu-id="88861-130">Call [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) to display a property sheet that has the copied properties.</span></span> <span data-ttu-id="88861-131">Übergeben Sie einen Zeiger auf das Eigenschaftsdatenobjekt als _lpConfigData-Parameter_ und einen Zeiger auf die Anzeigetabelle als _lpDisplayTable-Parameter._</span><span class="sxs-lookup"><span data-stu-id="88861-131">Pass a pointer to the property data object as the  _lpConfigData_ parameter and a pointer to the display table as the  _lpDisplayTable_ parameter.</span></span> <span data-ttu-id="88861-132">Wenn Sie den Standardzugriffsmodus für dieses Eigenschaftenblatt außer Kraft setzen möchten, legen Sie nicht das DT_EDITABLE-Flag für jedes Steuerelement in der Anzeigetabelle fest, das eine schreibgeschützte Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="88861-132">If you want to override the default access mode for this property sheet, do not set the DT_EDITABLE flag for each control in the display table that represents a read-only property.</span></span> 
    
6. <span data-ttu-id="88861-133">Wenn alle Änderungen im Eigenschaftenblatt vorgenommen wurden, rufen Sie die **IMAPIProp::CopyTo-Methode** des Eigenschaftendatenobjekts auf, um die geänderten Eigenschaften zurück in den Profilabschnitt zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="88861-133">When all of the changes have been made in the property sheet, call the property data object's **IMAPIProp::CopyTo** method to copy the changed properties back to the profile section.</span></span> 
    
<span data-ttu-id="88861-134">Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="88861-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> 
  
<span data-ttu-id="88861-135">Ausführliche Informationen zu Anzeigetabellen finden Sie unter [Display Table Implementation](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="88861-135">For detailed information about display tables, see [Display Table Implementation](display-table-implementation.md).</span></span> 
  
<span data-ttu-id="88861-136">Informationen zum Implementieren eines Steuerelements finden Sie unter [Control Object Implementation](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="88861-136">For information about implementing a control, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
<span data-ttu-id="88861-137">Warten Sie, bis der Benutzer auf **OK** oder Anwenden klickt, um den Index eines Steuerelements abzurufen, das ein Benutzer in einem Listenfeld der Anzeigetabelle **auswählt.**</span><span class="sxs-lookup"><span data-stu-id="88861-137">To retrieve the index of a control that a user selects in a display table list box, wait until the user clicks **OK** or **Apply**.</span></span> <span data-ttu-id="88861-138">An diesem Punkt wird der Eintragsbezeichner des ausgewählten Elements zurück in die [IMAPIProp : IUnknown-Schnittstelle als](imapipropiunknown.md) Wert der Eigenschaft geschrieben, die vom **ulPRSetProperty-Element** in der [DTBLLBX-Struktur](dtbllbx.md) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="88861-138">At this point, the entry identifier of the selected item is written back to the [IMAPIProp : IUnknown](imapipropiunknown.md) interface as the value of the property specified by the **ulPRSetProperty** member in the [DTBLLBX](dtbllbx.md) structure.</span></span> 
  
<span data-ttu-id="88861-139">Wenn Sie Elemente aus Dem Listenfeld hinzufügen oder entfernen müssen, funktioniert die Verwendung einer Anzeigetabelle und der [IMAPISupport::D oConfigPropsheet-Methode](imapisupport-doconfigpropsheet.md) nicht.</span><span class="sxs-lookup"><span data-stu-id="88861-139">If you need to be able to add or remove items from your list box, using a display table and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method will not work.</span></span> <span data-ttu-id="88861-140">Erwägen Sie stattdessen die Implementierung eines Eigenschaftenblatts mit der Win32-Eigenschaftenblatt-API, die in der comdlg32.dll ist.</span><span class="sxs-lookup"><span data-stu-id="88861-140">Instead, consider implementing a property sheet with the Win32 property sheet API contained in the comdlg32.dll file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="88861-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88861-141">See also</span></span>



[<span data-ttu-id="88861-142">MAPI-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="88861-142">MAPI Service Providers</span></span>](mapi-service-providers.md)

