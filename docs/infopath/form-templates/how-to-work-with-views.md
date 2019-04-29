---
title: Arbeiten mit Ansichten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- View-Klasse [InfoPath 2007], InfoPath 2007, arbeiten mit Ansichten, Ansichten [InfoPath 2007]
localization_priority: Normal
ms.assetid: 947b33c3-2acc-45d2-a89d-a712b6bc53df
description: Bei der Arbeit mit einer InfoPath-Formularvorlage können Sie Code schreiben, um auf die Ansichten des Formulars zuzugreifen, und dann eine Vielzahl von Aktionen für die in den Ansichten enthaltenen Daten ausführen. Das vom Microsoft. Office. InfoPath-Namespace bereitgestellte InfoPath-Objektmodell unterstützt den Zugriff auf die Ansichten eines Formulars durch die Verwendung der Member der View-Klasse.
ms.openlocfilehash: 829375a87513634ef0b38b6d92de9f33a605e89f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406297"
---
# <a name="work-with-views"></a><span data-ttu-id="a7e95-105">Arbeiten mit Ansichten</span><span class="sxs-lookup"><span data-stu-id="a7e95-105">Work with Views</span></span>

<span data-ttu-id="a7e95-106">Bei der Arbeit mit einer InfoPath-Formularvorlage können Sie Code schreiben, um auf die Ansichten des Formulars zuzugreifen, und dann eine Vielzahl von Aktionen für die in den Ansichten enthaltenen Daten ausführen.</span><span class="sxs-lookup"><span data-stu-id="a7e95-106">When working with an InfoPath form template, you can write code to access the form's views, and then perform a variety of actions on the data that the views contain.</span></span> <span data-ttu-id="a7e95-107">Das vom [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellte InfoPath-Objektmodell unterstützt den Zugriff auf die Ansichten eines Formulars durch die Verwendung der Member der [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="a7e95-107">The InfoPath object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace supports access to a form's views through the use of the members of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class.</span></span> 
  
## <a name="overview-of-the-view-class"></a><span data-ttu-id="a7e95-108">Übersicht über die View-Klasse</span><span class="sxs-lookup"><span data-stu-id="a7e95-108">Overview of the View Class</span></span>

<span data-ttu-id="a7e95-109">Die [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Klasse stellt die folgenden Methoden und Eigenschaften bereit, die Formularentwickler für die Interaktion mit einer InfoPath-Ansicht verwenden können.</span><span class="sxs-lookup"><span data-stu-id="a7e95-109">The [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class provides the following methods and properties, which form developers can use to interact with an InfoPath view.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a7e95-110">Die Methoden und Eigenschaften der [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Klasse stehen während des [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) -Ereignisses nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="a7e95-110">The methods and properties of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class are not available during the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event.</span></span> 
  
|<span data-ttu-id="a7e95-111">**Name**</span><span class="sxs-lookup"><span data-stu-id="a7e95-111">**Name**</span></span>|<span data-ttu-id="a7e95-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a7e95-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a7e95-113">[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="a7e95-113">[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="a7e95-114">Deaktiviert die automatische Synchronisierung zwischen dem einem Formular zugrunde liegenden XML-Dokument und der zugeordneten Ansicht.</span><span class="sxs-lookup"><span data-stu-id="a7e95-114">Disables automatic synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="a7e95-115">[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="a7e95-115">[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="a7e95-116">Aktiviert die automatische Synchronisierung zwischen dem einem Formular zugrunde liegenden XML-Dokument und der zugeordneten Ansicht.</span><span class="sxs-lookup"><span data-stu-id="a7e95-116">Enables automatic synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="a7e95-117">[Execute-Methode (Action Type)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7e95-117">[ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="a7e95-118">Führt basierend auf den Daten, die zurzeit in der Ansicht ausgewählt sind, einen Bearbeitungsbefehl für das einem Formular zugrunde liegende XML-Dokument aus.</span><span class="sxs-lookup"><span data-stu-id="a7e95-118">Executes an editing command against a form's underlying XML document, based on the data currently selected in the view.</span></span>  <br/> |
|<span data-ttu-id="a7e95-119">[Execute-Methode (Action Type, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7e95-119">[ExecuteAction(ActionType, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="a7e95-120">Führt basierend auf dem angegebenen Feld oder der angegebenen Gruppe einen Bearbeitungsbefehl für das einem Formular zugrunde liegende XML-Dokument aus.</span><span class="sxs-lookup"><span data-stu-id="a7e95-120">Executes an editing command against a form's underlying XML document, based on the specified field or group.</span></span>  <br/> |
|<span data-ttu-id="a7e95-121">[Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="a7e95-121">[Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx) method</span></span>  <br/> |<span data-ttu-id="a7e95-122">Exportiert die Ansicht in eine Datei des angegebenen Formats.</span><span class="sxs-lookup"><span data-stu-id="a7e95-122">Exports the view to a file of the specified format.</span></span>  <br/> |
|<span data-ttu-id="a7e95-123">[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="a7e95-123">[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="a7e95-124">Erzwingt die Synchronisierung zwischen dem einem Formular zugrunde liegenden XML-Dokument und der zugeordneten Ansicht.</span><span class="sxs-lookup"><span data-stu-id="a7e95-124">Forces synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="a7e95-125">[GetContextNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="a7e95-125">[GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="a7e95-126">Ruft einen Verweis auf ein **XPathNodeIterator**-Objekt zum Durchlaufen der zurückgegebenen XML-Knoten beginnend beim angegebenen Knoten ab.</span><span class="sxs-lookup"><span data-stu-id="a7e95-126">Gets a reference to an **XPathNodeIterator** object for iterating over the returned XML nodes starting from the specified node.</span></span>  <br/> |
|<span data-ttu-id="a7e95-127">[GetContextNodes (XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="a7e95-127">[GetContextNodes(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="a7e95-128">Ruft einen Verweis auf ein **XPathNodeIterator**-Objekt zum Durchlaufen der zurückgegebenen XML-Knoten in der aktuellen Auswahl innerhalb des an das angegebene Feld oder an die angegebene Gruppe gebundenen Steuerelements ab.</span><span class="sxs-lookup"><span data-stu-id="a7e95-128">Gets a reference to an **XPathNodeIterator** object for iterating over the returned XML nodes in the current selection within the control bound to the specified field or group.</span></span>  <br/> |
|<span data-ttu-id="a7e95-129">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="a7e95-129">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="a7e95-130">Ruft einen Verweis auf ein **XPathNodeIterator**-Objekt zum Durchlaufen aller XML-Knoten in der aktuellen Auswahl von Elementen in einer Ansicht ab.</span><span class="sxs-lookup"><span data-stu-id="a7e95-130">Gets a reference to an **XPathNodeIterator** object for iterating over all XML nodes in the current selection of items in a view.</span></span>  <br/> |
|<span data-ttu-id="a7e95-131">[SelectNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="a7e95-131">[SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="a7e95-132">Wählt basierend auf dem angegebenen XML-Startknoten einen Bereich von Knoten in einer Ansicht aus.</span><span class="sxs-lookup"><span data-stu-id="a7e95-132">Selects a range of nodes in a view based on the specified starting XML node.</span></span>  <br/> |
|<span data-ttu-id="a7e95-133">[SelectNodes (XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="a7e95-133">[SelectNodes(XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="a7e95-134">Wählt basierend auf dem angegebenen XML-Startknoten und XML-Endknoten einen Bereich von Knoten in einer Ansicht aus.</span><span class="sxs-lookup"><span data-stu-id="a7e95-134">Selects a range of nodes in a view based on the specified starting XML node and ending XML node.</span></span>  <br/> |
|<span data-ttu-id="a7e95-135">[SelectNodes (XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="a7e95-135">[SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="a7e95-136">Wählt basierend auf dem angegebenen XML-Startknoten, dem XML-Endknoten und dem angegebenen Steuerelement einen Bereich von Knoten in der Ansicht aus.</span><span class="sxs-lookup"><span data-stu-id="a7e95-136">Selects a range of nodes in a view based on the specified starting XML node, the ending XML node, and the specified control.</span></span>  <br/> |
|<span data-ttu-id="a7e95-137">[SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="a7e95-137">[SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="a7e95-138">Wählt den Text in einem bearbeitbaren Steuerelement aus, das an den Knoten gebunden ist, der durch das an diese Methode übergebene **XPathNavigator**-Objekt angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a7e95-138">Selects the text contained in an editable control that is bound to the node specified by the **XPathNavigator** object passed to this method.</span></span>  <br/> |
|<span data-ttu-id="a7e95-139">[SelectText (XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="a7e95-139">[SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="a7e95-140">Wählt den Text in einem bearbeitbaren Steuerelement aus, das an den Knoten gebunden ist, der durch das an diese Methode übergebene **XPathNavigator**-Objekt angegeben wird, und das angegebene Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="a7e95-140">Selects the text contained in an editable control that is bound to the node specified by the **XPathNavigator** object passed to this method, and the specified control.</span></span>  <br/> |
|<span data-ttu-id="a7e95-141">[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="a7e95-141">[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx) method</span></span>  <br/> |<span data-ttu-id="a7e95-142">Erstellt eine e-Mail-Nachricht mit der aktuellen Ansicht.</span><span class="sxs-lookup"><span data-stu-id="a7e95-142">Creates an email message containing the current view.</span></span>  <br/> |
|<span data-ttu-id="a7e95-143">[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a7e95-143">[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) property</span></span>  <br/> |<span data-ttu-id="a7e95-144">Ruft einen Verweis auf ein [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) -Objekt ab, das der Ansicht zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a7e95-144">Gets a reference to a [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) object associated with the view.</span></span>  <br/> |
|<span data-ttu-id="a7e95-145">[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a7e95-145">[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) property</span></span>  <br/> |<span data-ttu-id="a7e95-146">Ruft einen Verweis auf ein [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Objekt ab, das der Ansicht zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a7e95-146">Gets a reference to a [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) object associated with the view.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="a7e95-147">Das InfoPath-Objektmodell stellt auch [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) die ViewInfoCollection-und [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) -Klassen bereit, die zum Abrufen von Informationen zu allen in einem Formular implementierten Ansichten verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a7e95-147">The InfoPath object model also provides the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) and [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) classes, which can be used to get information about all of the views implemented in a form.</span></span> 
  
## <a name="using-the-view-class"></a><span data-ttu-id="a7e95-148">Verwenden der View-Klasse</span><span class="sxs-lookup"><span data-stu-id="a7e95-148">Using the View Class</span></span>

<span data-ttu-id="a7e95-149">Der Zugriff auf die [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Klasse erfolgt über die [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) -Eigenschaft der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse, auf die mithilfe des Schlüsselwortes **this** (C#) oder **Me** (Visual Basic) zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="a7e95-149">The [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class is accessed through the [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class, which is accessed using the **this** (C#) or **Me** (Visual Basic) keyword.</span></span> <span data-ttu-id="a7e95-150">Um auf den Namen der Ansicht zuzugreifen, müssen Sie auf das [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) -Objekt zugreifen, das der Ansicht zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a7e95-150">To access the name of the view, you need to access the [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) object associated with the view.</span></span> <span data-ttu-id="a7e95-151">Das folgende Beispiel zeigt, wie ein Meldungsfeld mit dem Namen der momentan aktiven Ansicht angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a7e95-151">The following example demonstrates how to display a message box with the name of the view that is currently active.</span></span> 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

<span data-ttu-id="a7e95-152">Alle InfoPath-Formularvorlagen enthalten mindestens eine Standardansicht. InfoPath unterstützt jedoch auch das Erstellen mehrerer Ansichten des einem Formular zugrunde liegenden XML-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="a7e95-152">All InfoPath form templates contain at least one default view; however, InfoPath also supports the creation of multiple views of a form's underlying XML document.</span></span> <span data-ttu-id="a7e95-153">Wenn Sie über mehrere Ansichten verfügen, [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) kann die ViewInfoCollection verwendet werden, um mit allen in der Formularvorlage implementierten Ansichten zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a7e95-153">When you have multiple views, the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) can be used to work with all of the views implemented in the form template.</span></span> <span data-ttu-id="a7e95-154">Um auf die [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) einer Formularvorlage zuzugreifen, verwenden Sie die [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) - [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) Eigenschaft der XmlForm-Klasse.</span><span class="sxs-lookup"><span data-stu-id="a7e95-154">To access the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) of a form template, use the [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class.</span></span> <span data-ttu-id="a7e95-155">Sie können die derzeit aktive Ansicht programmgesteuert ändern, indem Sie die [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) -Methode der [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) verwenden, wie im folgenden Codebeispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="a7e95-155">You can programmatically change the view that is currently active by using the [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) method of the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , as the following code sample demonstrates.</span></span> 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

<span data-ttu-id="a7e95-156">Das obige Beispiel für das Wechseln einer Ansicht funktioniert nur nach dem Öffnen des Formulars.</span><span class="sxs-lookup"><span data-stu-id="a7e95-156">The previous example for switching a view will work only after the form is opened.</span></span> <span data-ttu-id="a7e95-157">Verwenden Sie zum Festlegen einer Standardansicht während des [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) -Ereignisses die [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) -Eigenschaft der [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) -Klasse, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a7e95-157">To set a default view during the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event, use the [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) property of the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) class as shown in the following example.</span></span> <span data-ttu-id="a7e95-158">Beachten Sie jedoch, dass dieser Wert erst wirksam wird, nachdem das Formular gespeichert und erneut geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="a7e95-158">Note, however, that this value will only take effect after the form is saved and re-opened.</span></span> 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a><span data-ttu-id="a7e95-159">Auswählen von Steuerelementen in einer Ansicht</span><span class="sxs-lookup"><span data-stu-id="a7e95-159">Selecting Controls in a View</span></span>

<span data-ttu-id="a7e95-160">InfoPath stellt zwei Methoden der [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Klasse bereit, die beide überlastet sind, um ein Steuerelement in der aktuellen Ansicht programmgesteuert auszuwählen: die Methoden [SelectText ()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) und [SelectNodes ()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a7e95-160">InfoPath provides two methods of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class, both of which are overloaded, to programmatically select a control in the current view: the [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) and [SelectNodes()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) methods.</span></span> <span data-ttu-id="a7e95-161">Die [SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) -Methode wird für Dateneingabe Steuerelemente wie ein **Textfeld**verwendet, während die **SelectNodes** -Methode für strukturelle Steuerelemente wie einen **optionalen Abschnitt**verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a7e95-161">The [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method is used for data entry controls, such as a **Text Box**, while the **SelectNodes** method is used for structural controls, such as an **Optional Section**.</span></span> <span data-ttu-id="a7e95-162">Zum Auswählen eines bestimmten Steuerelements in der Ansicht müssen Sie den Knoten und optional den ViewContext-Bezeichner des Steuerelements bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a7e95-162">To select a particular control in the view, you need to provide the node and, optionally, the control's ViewContext ID.</span></span> <span data-ttu-id="a7e95-163">Den ViewContext-Bezeichner benötigen Sie, wenn Sie mehrere Steuerelemente haben, die an den gleichen Knoten in der Datenquelle gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="a7e95-163">The ViewContext ID is needed when you have multiple controls bound to the same node in the data source.</span></span> <span data-ttu-id="a7e95-164">InfoPath stellt die Informationen für den ViewContext-Bezeichner bereit, wenn Sie das Formular entwerfen.</span><span class="sxs-lookup"><span data-stu-id="a7e95-164">InfoPath provides the ViewContext ID information when you design the form.</span></span>
  
<span data-ttu-id="a7e95-165">Die ViewContext-ID eines Steuerelements wird auf der Registerkarte **erweitert** des Dialogfelds Eigenschaften des Steuerelements angezeigt, auf das durch Klicken mit der rechten Maustaste auf das Steuerelement, klicken auf _Steuerelement_ **Eigenschaften**und klicken auf die Registerkarte **erweitert** zugegriffen wird. Die ViewContext-ID des Steuerelements wird im Abschnitt **Code** der Registerkarte **erweitert** aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7e95-165">A control's ViewContext ID is displayed on the **Advanced** tab of the control's properties dialog box, which is accessed by right-clicking the control, clicking  _ControlName_ **Properties**, and then clicking the **Advanced** tab. The ViewContext ID of the control is listed in the **Code** section of the **Advanced** tab.</span></span> 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a><span data-ttu-id="a7e95-166">Verwendungszweck von "SelectText" und "SelectNodes"</span><span class="sxs-lookup"><span data-stu-id="a7e95-166">When to use SelectText and SelectNodes</span></span>

<span data-ttu-id="a7e95-167">Mithilfe der [SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) -Methode können Sie die folgenden Dateneingabe-Steuerelemente programmgesteuert auswählen:</span><span class="sxs-lookup"><span data-stu-id="a7e95-167">You can programmatically select the following data entry controls by using the [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method:</span></span> 
  
- <span data-ttu-id="a7e95-168">Textfeld</span><span class="sxs-lookup"><span data-stu-id="a7e95-168">Text Box</span></span>
    
- <span data-ttu-id="a7e95-169">Rich-Text-Feld Box</span><span class="sxs-lookup"><span data-stu-id="a7e95-169">Rich Text Box</span></span>
    
- <span data-ttu-id="a7e95-170">Datumsauswahl</span><span class="sxs-lookup"><span data-stu-id="a7e95-170">Date Picker</span></span>
    
<span data-ttu-id="a7e95-171">Mithilfe der [SelectNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) -Methode können Sie die folgenden strukturellen Steuerelemente programmgesteuert auswählen:</span><span class="sxs-lookup"><span data-stu-id="a7e95-171">You can programmatically select the following structural controls by using the [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method:</span></span> 
  
- <span data-ttu-id="a7e95-172">Optionaler Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a7e95-172">Optional Section</span></span>
    
- <span data-ttu-id="a7e95-173">Auswahlabschnitt</span><span class="sxs-lookup"><span data-stu-id="a7e95-173">Choice Section</span></span>
    
- <span data-ttu-id="a7e95-174">Wiederholter Abschnitt (Elemente)</span><span class="sxs-lookup"><span data-stu-id="a7e95-174">Repeating Section (items)</span></span>
    
- <span data-ttu-id="a7e95-175">Wiederholte Tabelle (Zeilen)</span><span class="sxs-lookup"><span data-stu-id="a7e95-175">Repeating Table (rows)</span></span>
    
- <span data-ttu-id="a7e95-176">Wiederholter rekursiver Abschnitt (Elemente)</span><span class="sxs-lookup"><span data-stu-id="a7e95-176">Repeating Recursive Section (items)</span></span>
    
- <span data-ttu-id="a7e95-177">Aufzählung, Nummerierte Liste und Einfache Liste</span><span class="sxs-lookup"><span data-stu-id="a7e95-177">Bulleted, Numbered, and Plain List</span></span>
    
- <span data-ttu-id="a7e95-178">Horizontale wiederholte Tabelle</span><span class="sxs-lookup"><span data-stu-id="a7e95-178">Horizontal Repeating Table</span></span>
    
<span data-ttu-id="a7e95-179">Die folgenden Steuerelemente können nicht programmgesteuert ausgewählt werden, d. h. es ist nicht möglich, den Fokus programmgesteuert darauf zu setzen:</span><span class="sxs-lookup"><span data-stu-id="a7e95-179">You cannot programmatically select, or set focus to, the following controls:</span></span>
  
- <span data-ttu-id="a7e95-180">Dropdown-Listenfeld</span><span class="sxs-lookup"><span data-stu-id="a7e95-180">Drop-Down List Box</span></span>
    
- <span data-ttu-id="a7e95-181">Listenfeld</span><span class="sxs-lookup"><span data-stu-id="a7e95-181">List Box</span></span>
    
- <span data-ttu-id="a7e95-182">Kontrollkästchen</span><span class="sxs-lookup"><span data-stu-id="a7e95-182">Check Box</span></span>
    
- <span data-ttu-id="a7e95-183">Optionsfeld</span><span class="sxs-lookup"><span data-stu-id="a7e95-183">Option Button</span></span>
    
- <span data-ttu-id="a7e95-184">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="a7e95-184">Button</span></span>
    
- <span data-ttu-id="a7e95-185">Bild (verknüpft oder eingeschlossen)</span><span class="sxs-lookup"><span data-stu-id="a7e95-185">Picture (linked or included)</span></span>
    
- <span data-ttu-id="a7e95-186">Freihandzeichnung</span><span class="sxs-lookup"><span data-stu-id="a7e95-186">Ink Picture</span></span>
    
- <span data-ttu-id="a7e95-187">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="a7e95-187">Hyperlink</span></span>
    
- <span data-ttu-id="a7e95-188">Ausdrucksfeld</span><span class="sxs-lookup"><span data-stu-id="a7e95-188">Expression Box</span></span>
    
- <span data-ttu-id="a7e95-189">Vertikales Etikett</span><span class="sxs-lookup"><span data-stu-id="a7e95-189">Vertical Label</span></span>
    
- <span data-ttu-id="a7e95-190">ActiveX-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a7e95-190">ActiveX Section</span></span>
    
- <span data-ttu-id="a7e95-191">Horizontaler Bereich</span><span class="sxs-lookup"><span data-stu-id="a7e95-191">Horizontal Region</span></span>
    
## <a name="using-the-selecttext-and-selectnodes-methods"></a><span data-ttu-id="a7e95-192">Verwenden der "SelectText"- und der "SelectNodes"-Methode</span><span class="sxs-lookup"><span data-stu-id="a7e95-192">Using the SelectText and SelectNodes Methods</span></span>

<span data-ttu-id="a7e95-193">Im folgenden Beispiel wird die [SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) -überLadung der **SelectText** -Methode, die einen _XmlNode_ -Parameter bereitStellt, zum Auswählen eines Textfelds verwendet, das an "My: Feld1" gebunden ist. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a7e95-193">In the following example, the [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) overload of the **SelectText** method, which provides one  _xmlNode_ parameter, is used to select a **Text Box** that is bound to "my:field1".</span></span> 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

<span data-ttu-id="a7e95-194">Wenn Sie mehrere Steuerelemente an "My: Feld1" gebunden haben, müssen Sie die [SelectText (XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) -überLadung der **SelectText** -Methode verwenden, die einen zusätzlichen _ViewContext_ -Parameter zum Auswählen eines bestimmten Steuerelements bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a7e95-194">If you have multiple controls bound to "my:field1", you must use the [SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) overload of the **SelectText** method, which provides an additional  _viewContext_ parameter to select a specific control.</span></span> <span data-ttu-id="a7e95-195">Im folgenden Beispiel wird davon ausgegangen, dass zwei **Textfeld** -Steuerelemente an "My: Feld1" gebunden sind, wobei das erste Steuerelement eine VIEWCONTEXT-ID von "CTRL1" und das zweite Steuerelement eine VIEWCONTEXT-ID von "CTRL8" hat.</span><span class="sxs-lookup"><span data-stu-id="a7e95-195">The following example assumes that there are two **Text Box** controls bound to "my:field1", with the first control having a ViewContext ID of "CTRL1" and the second control having a ViewContext ID of "CTRL8".</span></span> <span data-ttu-id="a7e95-196">Das zweite Steuerelement ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="a7e95-196">The second control is selected.</span></span> 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

<span data-ttu-id="a7e95-197">Im folgenden Beispiel wird die [SelectNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) -überLadung der **SelectNodes** -Methode, die nur einen _startNode_ -Parameter bereitstellt, zum Auswählen der ersten Zeile in einer wiederholten Tabelle verwendet, die an die wiederholte Gruppe "My: Employee ".</span><span class="sxs-lookup"><span data-stu-id="a7e95-197">In the following example, the [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) overload of the **SelectNodes** method, which provides only one  _startNode_ parameter, is used to select the first row in a repeating table bound to the repeating group "my:employee".</span></span> 
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

<span data-ttu-id="a7e95-198">Sie können auch mehrere Zeilen in einer wiederholten Tabelle auswählen.</span><span class="sxs-lookup"><span data-stu-id="a7e95-198">You can also select multiple rows in a repeating table.</span></span> <span data-ttu-id="a7e95-199">Im folgenden Beispiel werden die ersten drei Zeilen einer wiederholten Tabelle, die an die wiederholte Gruppe "My: Employee" gebunden sind, mit der SelectNodes-Überladung [(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) der **SelectNodes** -Methode ausgewählt, die  Parameter _startNode_ und _Endnode_ :</span><span class="sxs-lookup"><span data-stu-id="a7e95-199">In the following example, the first three rows of a repeating table bound to the repeating group "my:employee" are selected using the [SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) overload of the **SelectNodes** method, which provides  _startNode_ and  _endNode_ parameters:</span></span> 
  
```cs
// Create XPathNavigators to specify range of nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
XPathNavigator repeatingTableRow3 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:myemployee[3]", NamespaceManager);
// Select range of nodes in specified XPathNavigators.
CurrentView.SelectNodes(repeatingTableRow1, repeatingTableRow3);
```


