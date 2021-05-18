---
title: Arbeiten mit Ansichten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- view class [infopath 2007],InfoPath 2007, working with views,views [InfoPath 2007]
localization_priority: Normal
ms.assetid: 947b33c3-2acc-45d2-a89d-a712b6bc53df
description: Bei der Arbeit mit einer InfoPath-Formularvorlage können Sie Code schreiben, um auf die Ansichten des Formulars zuzugreifen, und dann eine Vielzahl von Aktionen für die in den Ansichten enthaltenen Daten ausführen. Das vom Microsoft.Office.InfoPath-Namespace bereitgestellte InfoPath-Objektmodell unterstützt den Zugriff auf die Ansichten eines Formulars mithilfe der Elemente der View-Klasse.
ms.openlocfilehash: 829375a87513634ef0b38b6d92de9f33a605e89f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406297"
---
# <a name="work-with-views"></a><span data-ttu-id="957c6-105">Arbeiten mit Ansichten</span><span class="sxs-lookup"><span data-stu-id="957c6-105">Work with Views</span></span>

<span data-ttu-id="957c6-106">Bei der Arbeit mit einer InfoPath-Formularvorlage können Sie Code schreiben, um auf die Ansichten des Formulars zuzugreifen, und dann eine Vielzahl von Aktionen für die in den Ansichten enthaltenen Daten ausführen.</span><span class="sxs-lookup"><span data-stu-id="957c6-106">When working with an InfoPath form template, you can write code to access the form's views, and then perform a variety of actions on the data that the views contain.</span></span> <span data-ttu-id="957c6-107">Das vom [Microsoft.Office.InfoPath-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) bereitgestellte InfoPath-Objektmodell unterstützt den Zugriff auf die Ansichten eines Formulars mithilfe der Elemente der [View-Klasse.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx)</span><span class="sxs-lookup"><span data-stu-id="957c6-107">The InfoPath object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace supports access to a form's views through the use of the members of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class.</span></span> 
  
## <a name="overview-of-the-view-class"></a><span data-ttu-id="957c6-108">Übersicht über die View-Klasse</span><span class="sxs-lookup"><span data-stu-id="957c6-108">Overview of the View Class</span></span>

<span data-ttu-id="957c6-109">Die [View-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) stellt die folgenden Methoden und Eigenschaften zur Verfügung, mit denen Formularentwickler mit einer InfoPath-Ansicht interagieren können.</span><span class="sxs-lookup"><span data-stu-id="957c6-109">The [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class provides the following methods and properties, which form developers can use to interact with an InfoPath view.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="957c6-110">Die Methoden und Eigenschaften der [View-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) sind während des Loading-Ereignisses [nicht](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="957c6-110">The methods and properties of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class are not available during the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event.</span></span> 
  
|<span data-ttu-id="957c6-111">**Name**</span><span class="sxs-lookup"><span data-stu-id="957c6-111">**Name**</span></span>|<span data-ttu-id="957c6-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="957c6-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="957c6-113">[DisableAutoUpdate-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="957c6-113">[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="957c6-114">Deaktiviert die automatische Synchronisierung zwischen dem einem Formular zugrunde liegenden XML-Dokument und der zugeordneten Ansicht.</span><span class="sxs-lookup"><span data-stu-id="957c6-114">Disables automatic synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="957c6-115">[EnableAutoUpdate-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="957c6-115">[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="957c6-116">Aktiviert die automatische Synchronisierung zwischen dem einem Formular zugrunde liegenden XML-Dokument und der zugeordneten Ansicht.</span><span class="sxs-lookup"><span data-stu-id="957c6-116">Enables automatic synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="957c6-117">[ExecuteAction(ActionType)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)</span><span class="sxs-lookup"><span data-stu-id="957c6-117">[ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="957c6-118">Führt basierend auf den Daten, die zurzeit in der Ansicht ausgewählt sind, einen Bearbeitungsbefehl für das einem Formular zugrunde liegende XML-Dokument aus.</span><span class="sxs-lookup"><span data-stu-id="957c6-118">Executes an editing command against a form's underlying XML document, based on the data currently selected in the view.</span></span>  <br/> |
|<span data-ttu-id="957c6-119">[ExecuteAction(ActionType, String)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)</span><span class="sxs-lookup"><span data-stu-id="957c6-119">[ExecuteAction(ActionType, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="957c6-120">Führt basierend auf dem angegebenen Feld oder der angegebenen Gruppe einen Bearbeitungsbefehl für das einem Formular zugrunde liegende XML-Dokument aus.</span><span class="sxs-lookup"><span data-stu-id="957c6-120">Executes an editing command against a form's underlying XML document, based on the specified field or group.</span></span>  <br/> |
|<span data-ttu-id="957c6-121">[Exportmethode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx)</span><span class="sxs-lookup"><span data-stu-id="957c6-121">[Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx) method</span></span>  <br/> |<span data-ttu-id="957c6-122">Exportiert die Ansicht in eine Datei des angegebenen Formats.</span><span class="sxs-lookup"><span data-stu-id="957c6-122">Exports the view to a file of the specified format.</span></span>  <br/> |
|<span data-ttu-id="957c6-123">[ForceUpdate-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx)</span><span class="sxs-lookup"><span data-stu-id="957c6-123">[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="957c6-124">Erzwingt die Synchronisierung zwischen dem einem Formular zugrunde liegenden XML-Dokument und der zugeordneten Ansicht.</span><span class="sxs-lookup"><span data-stu-id="957c6-124">Forces synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="957c6-125">[GetContextNodes(XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="957c6-125">[GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="957c6-126">Ruft einen Verweis auf ein **XPathNodeIterator**-Objekt zum Durchlaufen der zurückgegebenen XML-Knoten beginnend beim angegebenen Knoten ab.</span><span class="sxs-lookup"><span data-stu-id="957c6-126">Gets a reference to an **XPathNodeIterator** object for iterating over the returned XML nodes starting from the specified node.</span></span>  <br/> |
|<span data-ttu-id="957c6-127">[GetContextNodes(XPathNavigator, String)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="957c6-127">[GetContextNodes(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="957c6-128">Ruft einen Verweis auf ein **XPathNodeIterator**-Objekt zum Durchlaufen der zurückgegebenen XML-Knoten in der aktuellen Auswahl innerhalb des an das angegebene Feld oder an die angegebene Gruppe gebundenen Steuerelements ab.</span><span class="sxs-lookup"><span data-stu-id="957c6-128">Gets a reference to an **XPathNodeIterator** object for iterating over the returned XML nodes in the current selection within the control bound to the specified field or group.</span></span>  <br/> |
|<span data-ttu-id="957c6-129">[GetSelectedNodes-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="957c6-129">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="957c6-130">Ruft einen Verweis auf ein **XPathNodeIterator**-Objekt zum Durchlaufen aller XML-Knoten in der aktuellen Auswahl von Elementen in einer Ansicht ab.</span><span class="sxs-lookup"><span data-stu-id="957c6-130">Gets a reference to an **XPathNodeIterator** object for iterating over all XML nodes in the current selection of items in a view.</span></span>  <br/> |
|<span data-ttu-id="957c6-131">[SelectNodes(XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="957c6-131">[SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="957c6-132">Wählt basierend auf dem angegebenen XML-Startknoten einen Bereich von Knoten in einer Ansicht aus.</span><span class="sxs-lookup"><span data-stu-id="957c6-132">Selects a range of nodes in a view based on the specified starting XML node.</span></span>  <br/> |
|<span data-ttu-id="957c6-133">[SelectNodes(XPathNavigator, XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="957c6-133">[SelectNodes(XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="957c6-134">Wählt basierend auf dem angegebenen XML-Startknoten und XML-Endknoten einen Bereich von Knoten in einer Ansicht aus.</span><span class="sxs-lookup"><span data-stu-id="957c6-134">Selects a range of nodes in a view based on the specified starting XML node and ending XML node.</span></span>  <br/> |
|<span data-ttu-id="957c6-135">[SelectNodes(XPathNavigator, XPathNavigator, String)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="957c6-135">[SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="957c6-136">Wählt basierend auf dem angegebenen XML-Startknoten, dem XML-Endknoten und dem angegebenen Steuerelement einen Bereich von Knoten in der Ansicht aus.</span><span class="sxs-lookup"><span data-stu-id="957c6-136">Selects a range of nodes in a view based on the specified starting XML node, the ending XML node, and the specified control.</span></span>  <br/> |
|<span data-ttu-id="957c6-137">[SelectText(XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)</span><span class="sxs-lookup"><span data-stu-id="957c6-137">[SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="957c6-138">Wählt den Text in einem bearbeitbaren Steuerelement aus, das an den Knoten gebunden ist, der durch das an diese Methode übergebene **XPathNavigator**-Objekt angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="957c6-138">Selects the text contained in an editable control that is bound to the node specified by the **XPathNavigator** object passed to this method.</span></span>  <br/> |
|<span data-ttu-id="957c6-139">[SelectText(XPathNavigator, String)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)</span><span class="sxs-lookup"><span data-stu-id="957c6-139">[SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="957c6-140">Wählt den Text in einem bearbeitbaren Steuerelement aus, das an den Knoten gebunden ist, der durch das an diese Methode übergebene **XPathNavigator**-Objekt angegeben wird, und das angegebene Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="957c6-140">Selects the text contained in an editable control that is bound to the node specified by the **XPathNavigator** object passed to this method, and the specified control.</span></span>  <br/> |
|<span data-ttu-id="957c6-141">[ShowMailItem-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx)</span><span class="sxs-lookup"><span data-stu-id="957c6-141">[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx) method</span></span>  <br/> |<span data-ttu-id="957c6-142">Erstellt eine E-Mail-Nachricht, die die aktuelle Ansicht enthält.</span><span class="sxs-lookup"><span data-stu-id="957c6-142">Creates an email message containing the current view.</span></span>  <br/> |
|<span data-ttu-id="957c6-143">[ViewInfo-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx)</span><span class="sxs-lookup"><span data-stu-id="957c6-143">[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) property</span></span>  <br/> |<span data-ttu-id="957c6-144">Ruft einen Verweis auf ein [ViewInfo-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) ab, das der Ansicht zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="957c6-144">Gets a reference to a [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) object associated with the view.</span></span>  <br/> |
|<span data-ttu-id="957c6-145">[Window-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx)</span><span class="sxs-lookup"><span data-stu-id="957c6-145">[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) property</span></span>  <br/> |<span data-ttu-id="957c6-146">Ruft einen Verweis auf ein [Window-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) ab, das der Ansicht zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="957c6-146">Gets a reference to a [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) object associated with the view.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="957c6-147">Das InfoPath-Objektmodell stellt auch die [ViewInfoCollection-](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) und [ViewInfo-Klassen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) zur Verfügung, die zum Abrufen von Informationen zu allen in einem Formular implementierten Ansichten verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="957c6-147">The InfoPath object model also provides the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) and [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) classes, which can be used to get information about all of the views implemented in a form.</span></span> 
  
## <a name="using-the-view-class"></a><span data-ttu-id="957c6-148">Verwenden der View-Klasse</span><span class="sxs-lookup"><span data-stu-id="957c6-148">Using the View Class</span></span>

<span data-ttu-id="957c6-149">Auf [die View-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) wird über die [CurrentView-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) der [XmlForm-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) zugegriffen, auf die mithilfe des Schlüsselworts this **(C#)** oder **Me** (Visual Basic) zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="957c6-149">The [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class is accessed through the [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class, which is accessed using the **this** (C#) or **Me** (Visual Basic) keyword.</span></span> <span data-ttu-id="957c6-150">Um auf den Namen der Ansicht zu zugreifen, müssen Sie auf das [ViewInfo-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) zugreifen, das der Ansicht zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="957c6-150">To access the name of the view, you need to access the [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) object associated with the view.</span></span> <span data-ttu-id="957c6-151">Das folgende Beispiel zeigt, wie ein Meldungsfeld mit dem Namen der momentan aktiven Ansicht angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="957c6-151">The following example demonstrates how to display a message box with the name of the view that is currently active.</span></span> 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

<span data-ttu-id="957c6-152">Alle #A0 enthalten mindestens eine Standardansicht. InfoPath unterstützt jedoch auch das Erstellen mehrerer Ansichten des einem Formular zugrunde liegenden XML-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="957c6-152">All InfoPath form templates contain at least one default view; however, InfoPath also supports the creation of multiple views of a form's underlying XML document.</span></span> <span data-ttu-id="957c6-153">Wenn Sie über mehrere Ansichten verfügen, kann [die ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) verwendet werden, um mit allen in der Formularvorlage implementierten Ansichten zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="957c6-153">When you have multiple views, the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) can be used to work with all of the views implemented in the form template.</span></span> <span data-ttu-id="957c6-154">Um auf [die ViewInfoCollection einer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) Formularvorlage zu zugreifen, verwenden Sie die [ViewInfos-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) der [XmlForm-Klasse.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)</span><span class="sxs-lookup"><span data-stu-id="957c6-154">To access the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) of a form template, use the [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class.</span></span> <span data-ttu-id="957c6-155">Sie können die derzeit aktive Ansicht programmgesteuert ändern, indem Sie die [SwitchView-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) der [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) verwenden, wie im folgenden Codebeispiel veranschaulicht wird.</span><span class="sxs-lookup"><span data-stu-id="957c6-155">You can programmatically change the view that is currently active by using the [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) method of the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , as the following code sample demonstrates.</span></span> 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

<span data-ttu-id="957c6-156">Das obige Beispiel für das Wechseln einer Ansicht funktioniert nur nach dem Öffnen des Formulars.</span><span class="sxs-lookup"><span data-stu-id="957c6-156">The previous example for switching a view will work only after the form is opened.</span></span> <span data-ttu-id="957c6-157">Verwenden Sie zum Festlegen [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) einer Standardansicht während des Loading-Ereignisses die [Initial-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) der [ViewInfoCollection-Klasse,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="957c6-157">To set a default view during the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event, use the [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) property of the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) class as shown in the following example.</span></span> <span data-ttu-id="957c6-158">Beachten Sie jedoch, dass dieser Wert erst wirksam wird, nachdem das Formular gespeichert und erneut geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="957c6-158">Note, however, that this value will only take effect after the form is saved and re-opened.</span></span> 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a><span data-ttu-id="957c6-159">Auswählen von Steuerelementen in einer Ansicht</span><span class="sxs-lookup"><span data-stu-id="957c6-159">Selecting Controls in a View</span></span>

<span data-ttu-id="957c6-160">InfoPath bietet zwei [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) Methoden der View-Klasse, die beide überladen sind, um programmgesteuert ein Steuerelement in der aktuellen Ansicht auszuwählen: die [Methoden SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) und [SelectNodes().](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="957c6-160">InfoPath provides two methods of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class, both of which are overloaded, to programmatically select a control in the current view: the [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) and [SelectNodes()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) methods.</span></span> <span data-ttu-id="957c6-161">Die [SelectText(XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) wird für Dateneingabesteuerelemente wie ein **Textfeld** verwendet, während die **SelectNodes-Methode** für Struktursteuerelemente verwendet wird, z. B. einen **optionalen Abschnitt**.</span><span class="sxs-lookup"><span data-stu-id="957c6-161">The [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method is used for data entry controls, such as a **Text Box**, while the **SelectNodes** method is used for structural controls, such as an **Optional Section**.</span></span> <span data-ttu-id="957c6-162">Zum Auswählen eines bestimmten Steuerelements in der Ansicht müssen Sie den Knoten und optional den ViewContext-Bezeichner des Steuerelements bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="957c6-162">To select a particular control in the view, you need to provide the node and, optionally, the control's ViewContext ID.</span></span> <span data-ttu-id="957c6-163">Den ViewContext-Bezeichner benötigen Sie, wenn Sie mehrere Steuerelemente haben, die an den gleichen Knoten in der Datenquelle gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="957c6-163">The ViewContext ID is needed when you have multiple controls bound to the same node in the data source.</span></span> <span data-ttu-id="957c6-164">InfoPath stellt die Informationen für den ViewContext-Bezeichner bereit, wenn Sie das Formular entwerfen.</span><span class="sxs-lookup"><span data-stu-id="957c6-164">InfoPath provides the ViewContext ID information when you design the form.</span></span>
  
<span data-ttu-id="957c6-165">Die ViewContext-ID eines Steuerelements  wird auf der Registerkarte Erweitert des Eigenschaftendialogfelds des Steuerelements angezeigt, auf das zugegriffen wird, indem mit der rechten Maustaste auf das Steuerelement geklickt wird, auf _ControlName-Eigenschaften_ und dann auf die Registerkarte **Erweitert.** Die ViewContext-ID des Steuerelements wird im Abschnitt **Code** auf der Registerkarte **Erweitert** aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="957c6-165">A control's ViewContext ID is displayed on the **Advanced** tab of the control's properties dialog box, which is accessed by right-clicking the control, clicking  _ControlName_ **Properties**, and then clicking the **Advanced** tab. The ViewContext ID of the control is listed in the **Code** section of the **Advanced** tab.</span></span> 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a><span data-ttu-id="957c6-166">Verwendungszweck von "SelectText" und "SelectNodes"</span><span class="sxs-lookup"><span data-stu-id="957c6-166">When to use SelectText and SelectNodes</span></span>

<span data-ttu-id="957c6-167">Mit der [SelectText(XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) können Sie programmgesteuert die folgenden Dateneingabesteuerelemente auswählen:</span><span class="sxs-lookup"><span data-stu-id="957c6-167">You can programmatically select the following data entry controls by using the [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method:</span></span> 
  
- <span data-ttu-id="957c6-168">Textfeld</span><span class="sxs-lookup"><span data-stu-id="957c6-168">Text Box</span></span>
    
- <span data-ttu-id="957c6-169">Rich-Text-Feld Box</span><span class="sxs-lookup"><span data-stu-id="957c6-169">Rich Text Box</span></span>
    
- <span data-ttu-id="957c6-170">Datumsauswahl</span><span class="sxs-lookup"><span data-stu-id="957c6-170">Date Picker</span></span>
    
<span data-ttu-id="957c6-171">Mithilfe der [SelectNodes(XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) können Sie die folgenden Struktursteuerelemente programmgesteuert auswählen:</span><span class="sxs-lookup"><span data-stu-id="957c6-171">You can programmatically select the following structural controls by using the [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method:</span></span> 
  
- <span data-ttu-id="957c6-172">Optionaler Abschnitt</span><span class="sxs-lookup"><span data-stu-id="957c6-172">Optional Section</span></span>
    
- <span data-ttu-id="957c6-173">Auswahlabschnitt</span><span class="sxs-lookup"><span data-stu-id="957c6-173">Choice Section</span></span>
    
- <span data-ttu-id="957c6-174">Wiederholter Abschnitt (Elemente)</span><span class="sxs-lookup"><span data-stu-id="957c6-174">Repeating Section (items)</span></span>
    
- <span data-ttu-id="957c6-175">Wiederholte Tabelle (Zeilen)</span><span class="sxs-lookup"><span data-stu-id="957c6-175">Repeating Table (rows)</span></span>
    
- <span data-ttu-id="957c6-176">Wiederholter rekursiver Abschnitt (Elemente)</span><span class="sxs-lookup"><span data-stu-id="957c6-176">Repeating Recursive Section (items)</span></span>
    
- <span data-ttu-id="957c6-177">Aufzählung, Nummerierte Liste und Einfache Liste</span><span class="sxs-lookup"><span data-stu-id="957c6-177">Bulleted, Numbered, and Plain List</span></span>
    
- <span data-ttu-id="957c6-178">Horizontale wiederholte Tabelle</span><span class="sxs-lookup"><span data-stu-id="957c6-178">Horizontal Repeating Table</span></span>
    
<span data-ttu-id="957c6-179">Die folgenden Steuerelemente können nicht programmgesteuert ausgewählt werden, d. h. es ist nicht möglich, den Fokus programmgesteuert darauf zu setzen:</span><span class="sxs-lookup"><span data-stu-id="957c6-179">You cannot programmatically select, or set focus to, the following controls:</span></span>
  
- <span data-ttu-id="957c6-180">Dropdown-Listenfeld</span><span class="sxs-lookup"><span data-stu-id="957c6-180">Drop-Down List Box</span></span>
    
- <span data-ttu-id="957c6-181">Listenfeld</span><span class="sxs-lookup"><span data-stu-id="957c6-181">List Box</span></span>
    
- <span data-ttu-id="957c6-182">Kontrollkästchen</span><span class="sxs-lookup"><span data-stu-id="957c6-182">Check Box</span></span>
    
- <span data-ttu-id="957c6-183">Optionsfeld</span><span class="sxs-lookup"><span data-stu-id="957c6-183">Option Button</span></span>
    
- <span data-ttu-id="957c6-184">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="957c6-184">Button</span></span>
    
- <span data-ttu-id="957c6-185">Bild (verknüpft oder eingeschlossen)</span><span class="sxs-lookup"><span data-stu-id="957c6-185">Picture (linked or included)</span></span>
    
- <span data-ttu-id="957c6-186">Freihandzeichnung</span><span class="sxs-lookup"><span data-stu-id="957c6-186">Ink Picture</span></span>
    
- <span data-ttu-id="957c6-187">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="957c6-187">Hyperlink</span></span>
    
- <span data-ttu-id="957c6-188">Ausdrucksfeld</span><span class="sxs-lookup"><span data-stu-id="957c6-188">Expression Box</span></span>
    
- <span data-ttu-id="957c6-189">Vertikales Etikett</span><span class="sxs-lookup"><span data-stu-id="957c6-189">Vertical Label</span></span>
    
- <span data-ttu-id="957c6-190">ActiveX-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="957c6-190">ActiveX Section</span></span>
    
- <span data-ttu-id="957c6-191">Horizontaler Bereich</span><span class="sxs-lookup"><span data-stu-id="957c6-191">Horizontal Region</span></span>
    
## <a name="using-the-selecttext-and-selectnodes-methods"></a><span data-ttu-id="957c6-192">Verwenden der "SelectText"- und der "SelectNodes"-Methode</span><span class="sxs-lookup"><span data-stu-id="957c6-192">Using the SelectText and SelectNodes Methods</span></span>

<span data-ttu-id="957c6-193">Im folgenden Beispiel wird die [SelectText(XPathNavigator)-Überladung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) der **SelectText-Methode,** die einen  _xmlNode-Parameter_ enthält, verwendet, um ein Textfeld auszuwählen, das an "my:field1" gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="957c6-193">In the following example, the [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) overload of the **SelectText** method, which provides one  _xmlNode_ parameter, is used to select a **Text Box** that is bound to "my:field1".</span></span> 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

<span data-ttu-id="957c6-194">Wenn mehrere Steuerelemente an "my:field1" gebunden sind, müssen Sie die [SelectText(XPathNavigator, String)-Überladung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) der **SelectText-Methode** verwenden, die einen zusätzlichen  _viewContext-Parameter_ zur Auswahl eines bestimmten Steuerelements bietet.</span><span class="sxs-lookup"><span data-stu-id="957c6-194">If you have multiple controls bound to "my:field1", you must use the [SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) overload of the **SelectText** method, which provides an additional  _viewContext_ parameter to select a specific control.</span></span> <span data-ttu-id="957c6-195">Im folgenden Beispiel wird davon  ausgegangen, dass zwei Textfeldsteuerelemente an "my:field1" gebunden sind, mit dem ersten Steuerelement mit der ViewContext-ID "STRG1" und dem zweiten Steuerelement mit der ViewContext-ID "STRG8".</span><span class="sxs-lookup"><span data-stu-id="957c6-195">The following example assumes that there are two **Text Box** controls bound to "my:field1", with the first control having a ViewContext ID of "CTRL1" and the second control having a ViewContext ID of "CTRL8".</span></span> <span data-ttu-id="957c6-196">Das zweite Steuerelement ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="957c6-196">The second control is selected.</span></span> 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

<span data-ttu-id="957c6-197">Im folgenden Beispiel wird die [SelectNodes(XPathNavigator)-Überladung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) der **SelectNodes-Methode,** die nur einen  _startNode-Parameter_ enthält, verwendet, um die erste Zeile in einer wiederholten Tabelle auszuwählen, die an die wiederholte Gruppe "my:employee" gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="957c6-197">In the following example, the [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) overload of the **SelectNodes** method, which provides only one  _startNode_ parameter, is used to select the first row in a repeating table bound to the repeating group "my:employee".</span></span> 
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

<span data-ttu-id="957c6-198">Sie können auch mehrere Zeilen in einer wiederholten Tabelle auswählen.</span><span class="sxs-lookup"><span data-stu-id="957c6-198">You can also select multiple rows in a repeating table.</span></span> <span data-ttu-id="957c6-199">Im folgenden Beispiel werden die ersten drei Zeilen einer wiederholten Tabelle, die an die wiederholte Gruppe "my:employee" gebunden ist, mithilfe der [SelectNodes(XPathNavigator, XPathNavigator, String)-Überladung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) der **SelectNodes-Methode** ausgewählt, die  _die Parameter startNode_ und  _endNode_ enthält:</span><span class="sxs-lookup"><span data-stu-id="957c6-199">In the following example, the first three rows of a repeating table bound to the repeating group "my:employee" are selected using the [SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) overload of the **SelectNodes** method, which provides  _startNode_ and  _endNode_ parameters:</span></span> 
  
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


