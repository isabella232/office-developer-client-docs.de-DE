---
title: Implementierung von Eigenschaftenblättern
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f3475206-0237-4b5b-8efd-abd5d5e0b6c3
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 406451adac3cd73286feb787bd6b4d2f356aa283
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795325"
---
# <a name="property-sheet-implementation"></a><span data-ttu-id="cde5e-103">Implementierung von Eigenschaftenblättern</span><span class="sxs-lookup"><span data-stu-id="cde5e-103">Property Sheet Implementation</span></span>

  
  
<span data-ttu-id="cde5e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cde5e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cde5e-105">Ein Eigenschaftenblatt wird ein Dialogfeld zum Anzeigen der Eigenschaften eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="cde5e-105">A property sheet is a dialog box for displaying the properties of an object.</span></span> <span data-ttu-id="cde5e-106">Die Eigenschaften können schreibgeschützt, dem der Benutzer nur Sie können diese anzeigen oder Lese-/Schreibzugriff, sodass der Benutzer Änderungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="cde5e-106">The properties can be read-only, enabling the user only to view them, or read/write, enabling the user to make changes.</span></span> <span data-ttu-id="cde5e-107">Ein Eigenschaftenblatt enthält eine oder mehrere überlappende untergeordnete Fenster als Seiten bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="cde5e-107">A property sheet contains one or more overlapping child windows called pages.</span></span> <span data-ttu-id="cde5e-108">Jede Seite enthält Steuerelement Windows für eine Gruppe von verwandten Eigenschaften festlegen.</span><span class="sxs-lookup"><span data-stu-id="cde5e-108">Each page contains control windows for setting a group of related properties.</span></span> <span data-ttu-id="cde5e-109">Benutzer Navigieren von einer Seite auf durch Auswählen einer Registerkarte, die die entsprechende Seite im Vordergrund im Eigenschaftsfenster bringt.</span><span class="sxs-lookup"><span data-stu-id="cde5e-109">Users navigate from page to page by selecting a tab that brings the corresponding page to the foreground of the property sheet.</span></span>
  
<span data-ttu-id="cde5e-110">Dienstanbieter müssen ein Eigenschaftenblatt implementieren, die einen minimalen Satz von Eigenschaften im Zusammenhang mit der Konfiguration im Nachrichtendienst angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cde5e-110">Service providers must implement a property sheet that displays a minimal set of properties related to configuration in the message service.</span></span> <span data-ttu-id="cde5e-111">Wenn Sie diesen Dienst Nachrichteneigenschaften geändert werden können, können Sie entweder Benutzer des Clients zulassen Anwendungen wie die Systemsteuerung, um die Änderungen vornehmen, oder die Änderungen programmgesteuert implementieren.</span><span class="sxs-lookup"><span data-stu-id="cde5e-111">If you allow these message service properties to be changed, you can either allow users of client applications, such as the Control Panel, to make the changes or implement the changes programmatically.</span></span> <span data-ttu-id="cde5e-112">Implementieren von Eigenschaftenseiten zum Anzeigen und Bearbeiten von anderen Arten von Eigenschaften ist optional.</span><span class="sxs-lookup"><span data-stu-id="cde5e-112">Implementing property sheets to display and edit other types of properties is optional.</span></span> 
  
<span data-ttu-id="cde5e-113">In der Regel müssen Sie in den folgenden Situationen ein Eigenschaftenfenster anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="cde5e-113">Typically, you will need to display a property sheet in the following situations:</span></span>
  
- <span data-ttu-id="cde5e-114">Wenn ein Client [SettingsDialog Ihr Status des Objekts](imapistatus-settingsdialog.md) aufruft.</span><span class="sxs-lookup"><span data-stu-id="cde5e-114">When a client calls your status object's [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method.</span></span> 
    
- <span data-ttu-id="cde5e-115">Wenn MAPI Anbieter-Objekts Logon-Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="cde5e-115">When MAPI calls your provider object's logon method.</span></span>
    
- <span data-ttu-id="cde5e-116">Wenn MAPI die Eintrags-Funktion für Messagingdiensts des Anbieters aufruft.</span><span class="sxs-lookup"><span data-stu-id="cde5e-116">When MAPI calls the entry point function for your provider's message service.</span></span>
    
<span data-ttu-id="cde5e-117">Transportanbieter auch implementieren Sie Eigenschaftenseiten, um Eigenschaften im Zusammenhang mit Nachrichtenoptionen anzuzeigen und adressbuchanbietern implementierte Eigenschaft Sheets zum Anzeigen und bearbeiten ausführliche Informationen zu Benutzern und Verteilerlisten, erweiterte Suche messaging Kriterien und Vorlagen für neue Benutzer eingeben.</span><span class="sxs-lookup"><span data-stu-id="cde5e-117">Transport providers also implement property sheets to display properties related to message options, and address book providers implement property sheets to view and edit detailed information about messaging users and distribution lists, advanced search criteria, and templates for entering new users.</span></span>
  
<span data-ttu-id="cde5e-118">Eines der folgenden drei Verfahren können Sie um ein Eigenschaftenblatt zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="cde5e-118">You can use one of the following three techniques to create a property sheet:</span></span>
  
- <span data-ttu-id="cde5e-119">Manuell, wie Sie alle im Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="cde5e-119">Manually, as you would any dialog box.</span></span>
    
- <span data-ttu-id="cde5e-120">Mithilfe des common Control Blatt-Eigenschaft im Windows SDK bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="cde5e-120">By using the property sheet common control provided in the Windows SDK.</span></span>
    
- <span data-ttu-id="cde5e-121">Mithilfe von MAPI zeigen Sie Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="cde5e-121">By using a MAPI display table.</span></span>
    
<span data-ttu-id="cde5e-122">Anbieter sollte die letzte Option wählen (erstellen ein Eigenschaftenblatts mithilfe einer Tabelle anzeigen).</span><span class="sxs-lookup"><span data-stu-id="cde5e-122">Providers should choose the last option (create a property sheet by using a display table).</span></span> <span data-ttu-id="cde5e-123">Dies ist die einfachste Möglichkeit, da es entfällt die Notwendigkeit der Windows-Benutzeroberfläche entwickelt.</span><span class="sxs-lookup"><span data-stu-id="cde5e-123">This is the simplest option because it eliminates the need to work with the Windows user interface.</span></span> 
  
<span data-ttu-id="cde5e-124">Um ein Eigenschaftenblatt erstellt aus einer Tabelle Anzeige für Ihre Nachricht Diensteigenschaften implementieren möchten, verwenden Sie die folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="cde5e-124">To implement a property sheet built from a display table for your message service properties, use the following procedure:</span></span>
  
1. <span data-ttu-id="cde5e-125">Rufen Sie [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) , um einen Abschnitt im aktuellen Profil zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cde5e-125">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) to open a section in the current profile.</span></span> <span data-ttu-id="cde5e-126">Übergeben Sie Ihre [MAPIUID](mapiuid.md) oder NULL, um Ihre Anbieterabschnitt Profil zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cde5e-126">Pass your [MAPIUID](mapiuid.md) or NULL to open your provider's profile section.</span></span> 
    
2. <span data-ttu-id="cde5e-127">Rufen Sie [CreateIProp](createiprop.md) um ein Property-Daten-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cde5e-127">Call [CreateIProp](createiprop.md) to create a property data object.</span></span> 
    
3. <span data-ttu-id="cde5e-128">Rufen Sie Profilabschnitt [IMAPIProp::CopyTo](imapiprop-copyto.md) -Methode, um alle Eigenschaften des Bereichs in das Eigenschaftenobjekt Daten kopieren.</span><span class="sxs-lookup"><span data-stu-id="cde5e-128">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy all of the section's properties to the property data object.</span></span> 
    
4. <span data-ttu-id="cde5e-129">Erstellen Sie eine Anzeige Tabelle erstellen eine oder mehrere [DTPAGE](dtpage.md) -Strukturen, die beschreiben, die Steuerelemente auf dem Eigenschaftenblatt und Aufruf der Funktion [BuildDisplayTable](builddisplaytable.md) angezeigt werden soll, indem oder benutzerdefinierten Code implementieren.</span><span class="sxs-lookup"><span data-stu-id="cde5e-129">Create a display table either by building one or more [DTPAGE](dtpage.md) structures that describe the controls to appear on the property sheet and calling the [BuildDisplayTable](builddisplaytable.md) function, or by implementing custom code.</span></span> 
    
5. <span data-ttu-id="cde5e-130">Rufen Sie [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) , um einem Eigenschaftenfenster anzuzeigen, die die kopierten Eigenschaften hat.</span><span class="sxs-lookup"><span data-stu-id="cde5e-130">Call [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) to display a property sheet that has the copied properties.</span></span> <span data-ttu-id="cde5e-131">Übergeben Sie einen Zeiger auf die Daten Property-Objekt als Parameter _LpConfigData_ und einen Zeiger auf die Tabelle Anzeige als _LpDisplayTable_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="cde5e-131">Pass a pointer to the property data object as the  _lpConfigData_ parameter and a pointer to the display table as the  _lpDisplayTable_ parameter.</span></span> <span data-ttu-id="cde5e-132">Wenn Sie der Standardzugriffsmodus für dieses Eigenschaftenblatt außer Kraft setzen möchten, legen Sie die DT_EDITABLE-Flag für jedes Steuerelement nicht in der Tabelle anzeigen, die eine schreibgeschützte Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="cde5e-132">If you want to override the default access mode for this property sheet, do not set the DT_EDITABLE flag for each control in the display table that represents a read-only property.</span></span> 
    
6. <span data-ttu-id="cde5e-133">Wenn alle Änderungen im Eigenschaftenfenster vorgenommen wurden, rufen Sie die Eigenschaft Datenobjekt **IMAPIProp::CopyTo** -Methode, um die geänderten Eigenschaften zurück in den Profilabschnitt zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="cde5e-133">When all of the changes have been made in the property sheet, call the property data object's **IMAPIProp::CopyTo** method to copy the changed properties back to the profile section.</span></span> 
    
<span data-ttu-id="cde5e-134">Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="cde5e-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> 
  
<span data-ttu-id="cde5e-135">Ausführliche Informationen zu Tabellen anzeigen finden Sie unter [Tabelle Implementierung anzuzeigen](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="cde5e-135">For detailed information about display tables, see [Display Table Implementation](display-table-implementation.md).</span></span> 
  
<span data-ttu-id="cde5e-136">Informationen zum Implementieren eines Steuerelements finden Sie unter [Implementierung der Steuerelement-Objekts](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="cde5e-136">For information about implementing a control, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
<span data-ttu-id="cde5e-137">Um den Index eines Steuerelements abzurufen, die ein Benutzer in einem Listenfeld für Anzeige Tabelle auswählt, warten Sie, bis der Benutzer auf **OK** oder **Übernehmen**klickt.</span><span class="sxs-lookup"><span data-stu-id="cde5e-137">To retrieve the index of a control that a user selects in a display table list box, wait until the user clicks **OK** or **Apply**.</span></span> <span data-ttu-id="cde5e-138">Zu diesem Zeitpunkt die Eintrags-ID des ausgewählten Elements wird in zurückgeschrieben der [IMAPIProp: IUnknown](imapipropiunknown.md) -Schnittstelle als der Wert der Eigenschaft durch die **UlPRSetProperty** Mitglied in der Struktur [DTBLLBX](dtbllbx.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="cde5e-138">At this point, the entry identifier of the selected item is written back to the [IMAPIProp : IUnknown](imapipropiunknown.md) interface as the value of the property specified by the **ulPRSetProperty** member in the [DTBLLBX](dtbllbx.md) structure.</span></span> 
  
<span data-ttu-id="cde5e-139">Wenn Sie hinzufügen oder Entfernen von Elementen in Ihrem Listenfeld werden müssen, funktioniert mit einer Tabelle anzeigen und die [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) -Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="cde5e-139">If you need to be able to add or remove items from your list box, using a display table and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method will not work.</span></span> <span data-ttu-id="cde5e-140">Stattdessen Sie Implementieren eines Eigenschaftenblatts mit der Blatt-API in Win32-Eigenschaft, die in der Datei comdlg32.dll enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="cde5e-140">Instead, consider implementing a property sheet with the Win32 property sheet API contained in the comdlg32.dll file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cde5e-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cde5e-141">See also</span></span>



[<span data-ttu-id="cde5e-142">MAPI-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="cde5e-142">MAPI Service Providers</span></span>](mapi-service-providers.md)

