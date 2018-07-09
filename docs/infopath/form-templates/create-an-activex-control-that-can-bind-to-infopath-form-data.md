---
title: Erstellen eines ActiveX-Steuerelements, das an InfoPath-Formulardaten gebunden werden kann
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a0d62047-bf08-9f70-de00-7f81ef1331f1
description: Sie können ActiveX-Steuerelementen in InfoPath-Formulare hosten, die in der InfoPath-Editor geöffnet werden soll. Diese Steuerelemente können (mit einigen Einschränkungen) bereits vorhandene werden oder speziell für InfoPath geschrieben werden können.
ms.openlocfilehash: 90378533a7c3cde4a1927753c0325fdd8d0b3ce5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790725"
---
# <a name="create-an-activex-control-that-can-bind-to-infopath-form-data"></a><span data-ttu-id="12ab9-104">Erstellen eines ActiveX-Steuerelements, das an InfoPath-Formulardaten gebunden werden kann</span><span class="sxs-lookup"><span data-stu-id="12ab9-104">Create an ActiveX Control that can Bind to InfoPath Form Data</span></span>

<span data-ttu-id="12ab9-105">Sie können ActiveX-Steuerelementen in InfoPath-Formulare hosten, die in der InfoPath-Editor geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="12ab9-105">You can host ActiveX controls in InfoPath forms that are designed to be opened in the InfoPath editor.</span></span> <span data-ttu-id="12ab9-106">Diese Steuerelemente können (mit einigen Einschränkungen) bereits vorhandene werden oder speziell für InfoPath geschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="12ab9-106">These controls can be preexisting (with some constraints) or can be written specifically for InfoPath.</span></span>
  
## <a name="write-an-activex-control"></a><span data-ttu-id="12ab9-107">Schreiben eines ActiveX-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="12ab9-107">Write an ActiveX Control</span></span>

<span data-ttu-id="12ab9-108">Wie andere Steuerelemente in InfoPath sollten ActiveX-Steuerelemente vorhandene Component Object Model (COM) Schnittstellen unterstützen:</span><span class="sxs-lookup"><span data-stu-id="12ab9-108">As with other controls in InfoPath, ActiveX controls should support existing Component Object Model (COM) interfaces:</span></span>
  
- <span data-ttu-id="12ab9-109">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="12ab9-109">**IDispatch**</span></span>
    
- <span data-ttu-id="12ab9-110">**IPersistPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="12ab9-110">**IPersistPropertyBag**</span></span>
    
- <span data-ttu-id="12ab9-111">**IPersistStreamInit**</span><span class="sxs-lookup"><span data-stu-id="12ab9-111">**IPersistStreamInit**</span></span>
    
- <span data-ttu-id="12ab9-112">**IPropertyPage-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="12ab9-112">**IPropertyPage**</span></span>
    
- <span data-ttu-id="12ab9-113">**IObjectSafety**</span><span class="sxs-lookup"><span data-stu-id="12ab9-113">**IObjectSafety**</span></span>
    
- <span data-ttu-id="12ab9-114">**IPropertyNotifySink**</span><span class="sxs-lookup"><span data-stu-id="12ab9-114">**IPropertyNotifySink**</span></span>
    
- <span data-ttu-id="12ab9-115">**Die IViewObject**</span><span class="sxs-lookup"><span data-stu-id="12ab9-115">**IViewObject**</span></span>
    
- <span data-ttu-id="12ab9-116">**IOleObject**</span><span class="sxs-lookup"><span data-stu-id="12ab9-116">**IOleObject**</span></span>
    
- <span data-ttu-id="12ab9-117">**IOleInPlaceObject**</span><span class="sxs-lookup"><span data-stu-id="12ab9-117">**IOleInPlaceObject**</span></span>
    
<span data-ttu-id="12ab9-118">Damit InfoPath Eigenschaften in das Modell DOM (Document Object) zum Zeitpunkt aktualisiert, die sie im Steuerelement ändern kann, sollte das Steuerelement die folgenden Schnittstellen implementieren:</span><span class="sxs-lookup"><span data-stu-id="12ab9-118">In order for InfoPath to update properties in the Document Object Model (DOM) at the time that they change in the control, the control should implement the following interfaces:</span></span>
  
- <span data-ttu-id="12ab9-119">**IConnectionPointContainer**</span><span class="sxs-lookup"><span data-stu-id="12ab9-119">**IConnectionPointContainer**</span></span>
    
- <span data-ttu-id="12ab9-120">**IEnumConnectionPoints**</span><span class="sxs-lookup"><span data-stu-id="12ab9-120">**IEnumConnectionPoints**</span></span>
    
- <span data-ttu-id="12ab9-121">**IConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="12ab9-121">**IConnectionPoint**</span></span>
    
- <span data-ttu-id="12ab9-122">**IEnumConnections**</span><span class="sxs-lookup"><span data-stu-id="12ab9-122">**IEnumConnections**</span></span>
    
<span data-ttu-id="12ab9-123">Es gibt auch zwei InfoPath-spezifische COM-Schnittstellen, die eine engere Integration von Steuerelementen ermöglichen:</span><span class="sxs-lookup"><span data-stu-id="12ab9-123">Also, there are two InfoPath-specific COM interfaces that provide tighter integration of controls:</span></span>
  
- [<span data-ttu-id="12ab9-124">IInfoPathControl</span><span class="sxs-lookup"><span data-stu-id="12ab9-124">IInfoPathControl</span></span>](http://msdn.microsoft.com/de-de/library/bb264625.aspx)
    
- [<span data-ttu-id="12ab9-125">IInfoPathControlSite</span><span class="sxs-lookup"><span data-stu-id="12ab9-125">IInfoPathControlSite</span></span>](http://msdn.microsoft.com/de-de/library/bb264627.aspx)
    
## <a name="add-an-activex-control-to-the-infopath-design-environment"></a><span data-ttu-id="12ab9-126">Hinzufügen eines ActiveX-Steuerelements zur InfoPath-Entwicklungsumgebung</span><span class="sxs-lookup"><span data-stu-id="12ab9-126">Add an ActiveX Control to the InfoPath Design Environment</span></span>

<span data-ttu-id="12ab9-127">Der **Steuerelemente hinzufügen oder Entfernen benutzerdefinierter** Befehl auf dem Aufgabenbereich **Steuerelemente** können Sie mithilfe des **Assistenten zum Hinzufügen eines benutzerdefinierten Steuerelements** ein benutzerdefiniertes Steuerelement hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="12ab9-127">The **Add or Remove Custom Controls** command on the **Controls** task pane enables you to use the **Add Custom Control Wizard** to add a custom control.</span></span> <span data-ttu-id="12ab9-128">Mithilfe des Assistenten können Sie ein ActiveX-Steuerelement auswählen, die bereits registriert wurde oder zusätzliche benutzerdefinierte Steuerelemente auf Office Marketplace finden.</span><span class="sxs-lookup"><span data-stu-id="12ab9-128">By using the wizard, you can select an ActiveX control that has already been registered or find additional custom controls on Office Marketplace.</span></span> <span data-ttu-id="12ab9-129">Nachdem Sie ein Steuerelement ausgewählt haben, können Sie die folgenden Elemente angeben.</span><span class="sxs-lookup"><span data-stu-id="12ab9-129">After you select a control, you can specify the following items.</span></span> 
  
- <span data-ttu-id="12ab9-130">Angeben einer CAB-Datei zum Installieren des ActiveX-Steuerelements mit der Formularvorlage</span><span class="sxs-lookup"><span data-stu-id="12ab9-130">Specify a CAB to install the ActiveX control with your form template.</span></span>
    
- <span data-ttu-id="12ab9-131">Angeben einer Bindungseigenschaft zum Binden an die XML-Daten</span><span class="sxs-lookup"><span data-stu-id="12ab9-131">Specify a binding property to bind to the XML.</span></span>
    
- <span data-ttu-id="12ab9-132">Angeben einer Eigenschaft, die zum Aktivieren oder Deaktivieren des Steuerelements als Reaktion auf Regeln oder digitale Signaturen verwendet wird, was beispielsweise hilfreich sein kann, wenn die XML-Daten nicht vorhanden sind oder wenn bedingte Formatierung verwendet wird</span><span class="sxs-lookup"><span data-stu-id="12ab9-132">Specify a property that is used to enable or disable the control in response to rules or digital signatures, which can be useful, for example, when the XML is not present or when conditional formatting is used.</span></span>
    
- <span data-ttu-id="12ab9-133">Angeben der Datentypbindung</span><span class="sxs-lookup"><span data-stu-id="12ab9-133">Specify data type binding.</span></span>
    
> [!NOTE]
> <span data-ttu-id="12ab9-134">Wenn Sie ein ActiveX-Steuerelement entwickeln und es dem Aufgabenbereich **Steuerelemente** in InfoPath hinzugefügt haben, können Sie das ActiveX-Steuerelement neu erstellen, bis InfoPath geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="12ab9-134">If you are developing an ActiveX control and have added it to the **Controls** task pane in InfoPath, you will be unable to rebuild the ActiveX control until InfoPath is closed.</span></span> 
  
## <a name="deploy-an-activex-control"></a><span data-ttu-id="12ab9-135">Bereitstellen eines ActiveX-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="12ab9-135">Deploy an ActiveX Control</span></span>

<span data-ttu-id="12ab9-136">Um ein ActiveX-Steuerelement zu verteilen, können Sie ein Installationsprogramm, das das Steuerelement auf dem Zielcomputer installiert wird und kopiert die Vorlage (ICT Datei InfoPath Control) und der CAB-Datei in den Ordner des Benutzers, Schreiben \Users\\< Username\>\AppData\Local\ Microsoft\InfoPath\Controls.</span><span class="sxs-lookup"><span data-stu-id="12ab9-136">To distribute an ActiveX control, you can write an installer that installs the control on the target computer and copies the InfoPath Control Template (ICT) file and the CAB file to the user's folder, \Users\\<username\>\AppData\Local\Microsoft\InfoPath\Controls.</span></span> <span data-ttu-id="12ab9-137">Beachten Sie, dass, wenn mindestens zwei Entwickler sind zur Entwicklung von Formularen, die ActiveX-Steuerelemente verwenden zusammenarbeiten, jedes Entwicklers sollte die Steuerelemente, die das InfoPath-Design-Umgebung hinzugefügt wurden, oder nicht zum Ändern der Eigenschaften der Steuerelemente aus InfoPath.</span><span class="sxs-lookup"><span data-stu-id="12ab9-137">Note that if two or more developers are collaborating on developing forms that use ActiveX controls, each developer should have the controls that were added to the InfoPath design environment, or they will be unable to modify the properties of the controls from InfoPath.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="12ab9-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12ab9-138">See also</span></span>



<span data-ttu-id="12ab9-139">Übung 6: Hinzufügen von ActiveX-Steuerelementen in InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="12ab9-139">Lab 6: Adding ActiveX Controls in InfoPath 2003</span></span>
  
[<span data-ttu-id="12ab9-140">Erstellen von benutzerdefinierten InfoPath-Steuerelements mit c# und .NET (Blog des InfoPath-Teams)</span><span class="sxs-lookup"><span data-stu-id="12ab9-140">Creating an InfoPath Custom Control using C# and .NET (InfoPath Team Blog)</span></span>](http://blogs.msdn.com/infopath/archive/2005/04/15/creating-an-infopath-custom-control-using-c-and-net.aspx)

