---
title: Erstellen eines ActiveX-Steuerelements, das an InfoPath-Formulardaten gebunden werden kann
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a0d62047-bf08-9f70-de00-7f81ef1331f1
description: Sie können ActiveX-Steuerelemente in InfoPath-Formularen hosten, die im InfoPath-Editor geöffnet werden sollen. Diese Steuerelemente können bereits vorhanden sein (mit einigen Einschränkungen) oder speziell für InfoPath geschrieben werden.
ms.openlocfilehash: 70ac6a16b305403ffa99d8fe840a165913642f57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300189"
---
# <a name="create-an-activex-control-that-can-bind-to-infopath-form-data"></a><span data-ttu-id="f6ac2-104">Erstellen eines ActiveX-Steuerelements, das an InfoPath-Formulardaten gebunden werden kann</span><span class="sxs-lookup"><span data-stu-id="f6ac2-104">Create an ActiveX Control that can Bind to InfoPath Form Data</span></span>

<span data-ttu-id="f6ac2-105">Sie können ActiveX-Steuerelemente in InfoPath-Formularen hosten, die im InfoPath-Editor geöffnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f6ac2-105">You can host ActiveX controls in InfoPath forms that are designed to be opened in the InfoPath editor.</span></span> <span data-ttu-id="f6ac2-106">Diese Steuerelemente können bereits vorhanden sein (mit einigen Einschränkungen) oder speziell für InfoPath geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f6ac2-106">These controls can be preexisting (with some constraints) or can be written specifically for InfoPath.</span></span>
  
## <a name="write-an-activex-control"></a><span data-ttu-id="f6ac2-107">Schreiben eines ActiveX-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="f6ac2-107">Write an ActiveX Control</span></span>

<span data-ttu-id="f6ac2-108">Wie bei anderen Steuerelementen in InfoPath sollten ActiveX-Steuerelemente vorhandene COM-Schnittstellen (Component Object Model) unterstützen:</span><span class="sxs-lookup"><span data-stu-id="f6ac2-108">As with other controls in InfoPath, ActiveX controls should support existing Component Object Model (COM) interfaces:</span></span>
  
- <span data-ttu-id="f6ac2-109">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="f6ac2-109">**IDispatch**</span></span>
    
- <span data-ttu-id="f6ac2-110">**IPersistPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="f6ac2-110">**IPersistPropertyBag**</span></span>
    
- <span data-ttu-id="f6ac2-111">**IPersistStreamInit**</span><span class="sxs-lookup"><span data-stu-id="f6ac2-111">**IPersistStreamInit**</span></span>
    
- <span data-ttu-id="f6ac2-112">**IPropertyPage**</span><span class="sxs-lookup"><span data-stu-id="f6ac2-112">**IPropertyPage**</span></span>
    
- <span data-ttu-id="f6ac2-113">**IObjectSafety**</span><span class="sxs-lookup"><span data-stu-id="f6ac2-113">**IObjectSafety**</span></span>
    
- <span data-ttu-id="f6ac2-114">**IPropertyNotifySink**</span><span class="sxs-lookup"><span data-stu-id="f6ac2-114">**IPropertyNotifySink**</span></span>
    
- <span data-ttu-id="f6ac2-115">**IViewObject**</span><span class="sxs-lookup"><span data-stu-id="f6ac2-115">**IViewObject**</span></span>
    
- <span data-ttu-id="f6ac2-116">**IOleObject**</span><span class="sxs-lookup"><span data-stu-id="f6ac2-116">**IOleObject**</span></span>
    
- <span data-ttu-id="f6ac2-117">**IOleInPlaceObject**</span><span class="sxs-lookup"><span data-stu-id="f6ac2-117">**IOleInPlaceObject**</span></span>
    
<span data-ttu-id="f6ac2-118">Damit InfoPath Eigenschaften im DOM (Document Object Model) aktualisieren kann, wenn Sie sich im Steuerelement ändern, sollte das Steuerelement die folgenden Schnittstellen implementieren:</span><span class="sxs-lookup"><span data-stu-id="f6ac2-118">In order for InfoPath to update properties in the Document Object Model (DOM) at the time that they change in the control, the control should implement the following interfaces:</span></span>
  
- <span data-ttu-id="f6ac2-119">**IConnectionPointContainer**</span><span class="sxs-lookup"><span data-stu-id="f6ac2-119">**IConnectionPointContainer**</span></span>
    
- <span data-ttu-id="f6ac2-120">**IEnumConnectionPoints**</span><span class="sxs-lookup"><span data-stu-id="f6ac2-120">**IEnumConnectionPoints**</span></span>
    
- <span data-ttu-id="f6ac2-121">**IConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="f6ac2-121">**IConnectionPoint**</span></span>
    
- <span data-ttu-id="f6ac2-122">**IEnumConnections**</span><span class="sxs-lookup"><span data-stu-id="f6ac2-122">**IEnumConnections**</span></span>
    
<span data-ttu-id="f6ac2-123">Außerdem gibt es zwei InfoPath-spezifische COM-Schnittstellen, die eine engere Integration von Steuerelementen ermöglichen:</span><span class="sxs-lookup"><span data-stu-id="f6ac2-123">Also, there are two InfoPath-specific COM interfaces that provide tighter integration of controls:</span></span>
  
- [<span data-ttu-id="f6ac2-124">IInfoPathControl</span><span class="sxs-lookup"><span data-stu-id="f6ac2-124">IInfoPathControl</span></span>](https://msdn.microsoft.com/library/bb264625.aspx)
    
- [<span data-ttu-id="f6ac2-125">IInfoPathControlSite</span><span class="sxs-lookup"><span data-stu-id="f6ac2-125">IInfoPathControlSite</span></span>](https://msdn.microsoft.com/library/bb264627.aspx)
    
## <a name="add-an-activex-control-to-the-infopath-design-environment"></a><span data-ttu-id="f6ac2-126">Hinzufügen eines ActiveX-Steuerelements zur InfoPath-Entwicklungsumgebung</span><span class="sxs-lookup"><span data-stu-id="f6ac2-126">Add an ActiveX Control to the InfoPath Design Environment</span></span>

<span data-ttu-id="f6ac2-127">Mit dem Befehl **benutzerdefinierte Steuerelemente hinzufügen oder entfernen** im Aufgabenbereich **Steuerelemente** können Sie den **Assistenten zum Hinzufügen** eines benutzerdefinierten Steuerelements verwenden, um ein benutzerdefiniertes Steuerelement hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f6ac2-127">The **Add or Remove Custom Controls** command on the **Controls** task pane enables you to use the **Add Custom Control Wizard** to add a custom control.</span></span> <span data-ttu-id="f6ac2-128">Mithilfe des Assistenten können Sie ein ActiveX-Steuerelement auswählen, das bereits registriert wurde, oder zusätzliche benutzerdefinierte Steuerelemente auf Office Marketplace finden.</span><span class="sxs-lookup"><span data-stu-id="f6ac2-128">By using the wizard, you can select an ActiveX control that has already been registered or find additional custom controls on Office Marketplace.</span></span> <span data-ttu-id="f6ac2-129">Nachdem Sie ein Steuerelement ausgewählt haben, können Sie die folgenden Elemente angeben.</span><span class="sxs-lookup"><span data-stu-id="f6ac2-129">After you select a control, you can specify the following items.</span></span> 
  
- <span data-ttu-id="f6ac2-130">Angeben einer CAB-Datei zum Installieren des ActiveX-Steuerelements mit der Formularvorlage</span><span class="sxs-lookup"><span data-stu-id="f6ac2-130">Specify a CAB to install the ActiveX control with your form template.</span></span>
    
- <span data-ttu-id="f6ac2-131">Angeben einer Bindungseigenschaft zum Binden an die XML-Daten</span><span class="sxs-lookup"><span data-stu-id="f6ac2-131">Specify a binding property to bind to the XML.</span></span>
    
- <span data-ttu-id="f6ac2-132">Angeben einer Eigenschaft, die zum Aktivieren oder Deaktivieren des Steuerelements als Reaktion auf Regeln oder digitale Signaturen verwendet wird, was beispielsweise hilfreich sein kann, wenn die XML-Daten nicht vorhanden sind oder wenn bedingte Formatierung verwendet wird</span><span class="sxs-lookup"><span data-stu-id="f6ac2-132">Specify a property that is used to enable or disable the control in response to rules or digital signatures, which can be useful, for example, when the XML is not present or when conditional formatting is used.</span></span>
    
- <span data-ttu-id="f6ac2-133">Angeben der Datentypbindung</span><span class="sxs-lookup"><span data-stu-id="f6ac2-133">Specify data type binding.</span></span>
    
> [!NOTE]
> <span data-ttu-id="f6ac2-134">Wenn Sie ein ActiveX-Steuerelement entwickeln und es dem Aufgabenbereich **Steuerelemente** in InfoPath hinzugefügt haben, können Sie das ActiveX-Steuerelement erst neu erstellen, nachdem InfoPath geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="f6ac2-134">If you are developing an ActiveX control and have added it to the **Controls** task pane in InfoPath, you will be unable to rebuild the ActiveX control until InfoPath is closed.</span></span> 
  
## <a name="deploy-an-activex-control"></a><span data-ttu-id="f6ac2-135">Bereitstellen eines ActiveX-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="f6ac2-135">Deploy an ActiveX Control</span></span>

<span data-ttu-id="f6ac2-136">Um ein ActiveX-Steuerelement zu verteilen, können Sie ein Installationsprogramm schreiben, das das Steuerelement auf dem Zielcomputer installiert und die InfoPath-Steuerelementvorlage (ICT) und die CAB-Datei\\in\>den Ordner des Benutzers kopiert, \Users <username \AppData\Local\ Microsoft\InfoPath\Controls.</span><span class="sxs-lookup"><span data-stu-id="f6ac2-136">To distribute an ActiveX control, you can write an installer that installs the control on the target computer and copies the InfoPath Control Template (ICT) file and the CAB file to the user's folder, \Users\\<username\>\AppData\Local\Microsoft\InfoPath\Controls.</span></span> <span data-ttu-id="f6ac2-137">Beachten Sie, dass, wenn zwei oder mehr Entwickler an der Entwicklung von Formularen arbeiten, die ActiveX-Steuerelemente verwenden, jeder Entwickler über die Steuerelemente verfügen sollte, die der InfoPath-Entwurfsumgebung hinzugefügt wurden, oder Sie können die Eigenschaften der Steuerelemente nicht ändern. InfoPath.</span><span class="sxs-lookup"><span data-stu-id="f6ac2-137">Note that if two or more developers are collaborating on developing forms that use ActiveX controls, each developer should have the controls that were added to the InfoPath design environment, or they will be unable to modify the properties of the controls from InfoPath.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f6ac2-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6ac2-138">See also</span></span>

<span data-ttu-id="f6ac2-139">Lab 6: Hinzufügen von ActiveX-Steuerelementen in InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="f6ac2-139">Lab 6: Adding ActiveX Controls in InfoPath 2003</span></span>
  
[<span data-ttu-id="f6ac2-140">Erstellen eines benutzerdefinierten InfoPath-Steuerelements mithilfe von C# und .NET (InfoPath-teamBlog)</span><span class="sxs-lookup"><span data-stu-id="f6ac2-140">Creating an InfoPath Custom Control using C# and .NET (InfoPath Team Blog)</span></span>](https://blogs.msdn.microsoft.com/infopath/2005/04/15/creating-an-infopath-custom-control-using-c-and-net/)

