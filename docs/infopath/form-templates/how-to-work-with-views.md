---
title: Arbeiten mit Ansichten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- View-Klasse [Infopath 2007] InfoPath 2007, arbeiten mit Ansichten, Ansichten [InfoPath 2007]
localization_priority: Normal
ms.assetid: 947b33c3-2acc-45d2-a89d-a712b6bc53df
description: Bei der Arbeit mit InfoPath-Formularvorlage können Sie Code schreiben, um die Ansichten des Formulars zuzugreifen, und klicken Sie dann auf die Daten, die die Ansichten enthalten eine Vielzahl von Aktionen ausführen. Die InfoPath-Objektmodell bereitgestellten durch die Microsoft.Office.InfoPath-Namespace Zugriff auf die Ansichten eines Formulars durch Verwendung der Member der View-Klasse unterstützt.
ms.openlocfilehash: 84c32244454e388e50433922c007d556fbef806a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790768"
---
# <a name="work-with-views"></a><span data-ttu-id="d72c7-105">Arbeiten mit Ansichten</span><span class="sxs-lookup"><span data-stu-id="d72c7-105">Work with Views</span></span>

<span data-ttu-id="d72c7-106">Bei der Arbeit mit InfoPath-Formularvorlage können Sie Code schreiben, um die Ansichten des Formulars zuzugreifen, und klicken Sie dann auf die Daten, die die Ansichten enthalten eine Vielzahl von Aktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="d72c7-106">When working with an InfoPath form template, you can write code to access the form's views, and then perform a variety of actions on the data that the views contain.</span></span> <span data-ttu-id="d72c7-107">Das InfoPath-Objektmodell zur Verfügung gestellt, durch die [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace unterstützt den Zugriff auf die Ansichten eines Formulars durch Verwendung der Member der [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="d72c7-107">The InfoPath object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace supports access to a form's views through the use of the members of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class.</span></span> 
  
## <a name="overview-of-the-view-class"></a><span data-ttu-id="d72c7-108">Übersicht über die View-Klasse</span><span class="sxs-lookup"><span data-stu-id="d72c7-108">Overview of the View Class</span></span>

<span data-ttu-id="d72c7-109">[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Klasse bietet die folgenden Methoden und Eigenschaften, die Formularentwickler für die Interaktion mit einer InfoPath-Ansicht verwenden können.</span><span class="sxs-lookup"><span data-stu-id="d72c7-109">The [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class provides the following methods and properties, which form developers can use to interact with an InfoPath view.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d72c7-110">Die Methoden und Eigenschaften der [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Klasse sind während der [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) -Ereignis nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d72c7-110">The methods and properties of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class are not available during the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event.</span></span> 
  
|<span data-ttu-id="d72c7-111">**Name**</span><span class="sxs-lookup"><span data-stu-id="d72c7-111">**Name**</span></span>|<span data-ttu-id="d72c7-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d72c7-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d72c7-113">[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="d72c7-113">[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="d72c7-114">Deaktiviert die automatische Synchronisierung zwischen dem einem Formular zugrunde liegenden XML-Dokument und der zugeordneten Ansicht.</span><span class="sxs-lookup"><span data-stu-id="d72c7-114">Disables automatic synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="d72c7-115">[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="d72c7-115">[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="d72c7-116">Aktiviert die automatische Synchronisierung zwischen dem einem Formular zugrunde liegenden XML-Dokument und der zugeordneten Ansicht.</span><span class="sxs-lookup"><span data-stu-id="d72c7-116">Enables automatic synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="d72c7-117">[ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="d72c7-117">[ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="d72c7-118">Führt basierend auf den Daten, die zurzeit in der Ansicht ausgewählt sind, einen Bearbeitungsbefehl für das einem Formular zugrunde liegende XML-Dokument aus.</span><span class="sxs-lookup"><span data-stu-id="d72c7-118">Executes an editing command against a form's underlying XML document, based on the data currently selected in the view.</span></span>  <br/> |
|<span data-ttu-id="d72c7-119">[ExecuteAction (ActionType, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="d72c7-119">[ExecuteAction(ActionType, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) method</span></span>  <br/> |<span data-ttu-id="d72c7-120">Führt basierend auf dem angegebenen Feld oder der angegebenen Gruppe einen Bearbeitungsbefehl für das einem Formular zugrunde liegende XML-Dokument aus.</span><span class="sxs-lookup"><span data-stu-id="d72c7-120">Executes an editing command against a form's underlying XML document, based on the specified field or group.</span></span>  <br/> |
|<span data-ttu-id="d72c7-121">[Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="d72c7-121">[Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx) method</span></span>  <br/> |<span data-ttu-id="d72c7-122">Exportiert die Ansicht in eine Datei des angegebenen Formats.</span><span class="sxs-lookup"><span data-stu-id="d72c7-122">Exports the view to a file of the specified format.</span></span>  <br/> |
|<span data-ttu-id="d72c7-123">[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="d72c7-123">[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx) method</span></span>  <br/> |<span data-ttu-id="d72c7-124">Erzwingt die Synchronisierung zwischen dem einem Formular zugrunde liegenden XML-Dokument und der zugeordneten Ansicht.</span><span class="sxs-lookup"><span data-stu-id="d72c7-124">Forces synchronization between a form's underlying XML document and the associated view.</span></span>  <br/> |
|<span data-ttu-id="d72c7-125">[GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="d72c7-125">[GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="d72c7-126">Ruft einen Verweis auf ein **XPathNodeIterator** -Objekt zum Durchlaufen der zurückgegebenen XML-Knoten beginnend beim angegebenen Knoten ab.</span><span class="sxs-lookup"><span data-stu-id="d72c7-126">Gets a reference to an **XPathNodeIterator** object for iterating over the returned XML nodes starting from the specified node.</span></span>  <br/> |
|<span data-ttu-id="d72c7-127">[(XPathNavigator, String) GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="d72c7-127">[GetContextNodes(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="d72c7-128">Ruft einen Verweis auf ein **XPathNodeIterator** -Objekt zum Durchlaufen der zurückgegebenen XML-Knoten in der aktuellen Auswahl innerhalb des an das angegebene Feld oder Gruppe gebundenen Steuerelements ab.</span><span class="sxs-lookup"><span data-stu-id="d72c7-128">Gets a reference to an **XPathNodeIterator** object for iterating over the returned XML nodes in the current selection within the control bound to the specified field or group.</span></span>  <br/> |
|<span data-ttu-id="d72c7-129">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="d72c7-129">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="d72c7-130">Ruft einen Verweis auf ein **XPathNodeIterator** -Objekt zum Durchlaufen aller XML-Knoten in der aktuellen Auswahl von Elementen in einer Ansicht ab.</span><span class="sxs-lookup"><span data-stu-id="d72c7-130">Gets a reference to an **XPathNodeIterator** object for iterating over all XML nodes in the current selection of items in a view.</span></span>  <br/> |
|<span data-ttu-id="d72c7-131">[SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="d72c7-131">[SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="d72c7-132">Wählt basierend auf dem angegebenen XML-Startknoten einen Bereich von Knoten in einer Ansicht aus. </span><span class="sxs-lookup"><span data-stu-id="d72c7-132">Selects a range of nodes in a view based on the specified starting XML node.</span></span>  <br/> |
|<span data-ttu-id="d72c7-133">[SelectNodes (XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="d72c7-133">[SelectNodes(XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="d72c7-134">Wählt basierend auf dem angegebenen XML-Startknoten und XML-Endknoten einen Bereich von Knoten in einer Ansicht aus.</span><span class="sxs-lookup"><span data-stu-id="d72c7-134">Selects a range of nodes in a view based on the specified starting XML node and ending XML node.</span></span>  <br/> |
|<span data-ttu-id="d72c7-135">[SelectNodes (XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="d72c7-135">[SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method</span></span>  <br/> |<span data-ttu-id="d72c7-136">Wählt basierend auf dem angegebenen XML-Startknoten, dem XML-Endknoten und dem angegebenen Steuerelement einen Bereich von Knoten in der Ansicht aus. </span><span class="sxs-lookup"><span data-stu-id="d72c7-136">Selects a range of nodes in a view based on the specified starting XML node, the ending XML node, and the specified control.</span></span>  <br/> |
|<span data-ttu-id="d72c7-137">[SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="d72c7-137">[SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="d72c7-138">Wählt den Text in einem bearbeitbaren Steuerelement aus, das auf den durch das an diese Methode übergebene **XPathNavigator** -Objekt angegebenen Knoten gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="d72c7-138">Selects the text contained in an editable control that is bound to the node specified by the **XPathNavigator** object passed to this method.</span></span>  <br/> |
|<span data-ttu-id="d72c7-139">[(XPathNavigator, String) SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="d72c7-139">[SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method</span></span>  <br/> |<span data-ttu-id="d72c7-140">Wählt den Text in einem bearbeitbaren Steuerelement aus, das auf den durch das an diese Methode übergebene **XPathNavigator** -Objekt angegebenen Knoten gebunden ist und das angegebene Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="d72c7-140">Selects the text contained in an editable control that is bound to the node specified by the **XPathNavigator** object passed to this method, and the specified control.</span></span>  <br/> |
|<span data-ttu-id="d72c7-141">[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx) -Methode</span><span class="sxs-lookup"><span data-stu-id="d72c7-141">[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx) method</span></span>  <br/> |<span data-ttu-id="d72c7-142">Erstellt eine e-Mail-Nachricht, die die aktuelle Ansicht enthält.</span><span class="sxs-lookup"><span data-stu-id="d72c7-142">Creates an email message containing the current view.</span></span>  <br/> |
|<span data-ttu-id="d72c7-143">[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d72c7-143">[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) property</span></span>  <br/> |<span data-ttu-id="d72c7-144">Ruft einen Verweis auf ein [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) -Objekt, das der Ansicht zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d72c7-144">Gets a reference to a [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) object associated with the view.</span></span>  <br/> |
|<span data-ttu-id="d72c7-145">[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d72c7-145">[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) property</span></span>  <br/> |<span data-ttu-id="d72c7-146">Ruft einen Verweis auf ein [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Objekt, das der Ansicht zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d72c7-146">Gets a reference to a [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) object associated with the view.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="d72c7-147">Das InfoPath-Objektmodell stellt auch die [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) und [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) -Klasse, die zum Abrufen von Informationen zu allen in einem Formular implementierten Ansichten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d72c7-147">The InfoPath object model also provides the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) and [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) classes, which can be used to get information about all of the views implemented in a form.</span></span> 
  
## <a name="using-the-view-class"></a><span data-ttu-id="d72c7-148">Verwenden der View-Klasse</span><span class="sxs-lookup"><span data-stu-id="d72c7-148">Using the View Class</span></span>

<span data-ttu-id="d72c7-149">[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Klasse erfolgt über die [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) -Eigenschaft der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse, die mit dem **dieser** (c#) oder Schlüsselwort **Me** (Visual Basic) zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="d72c7-149">The [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class is accessed through the [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class, which is accessed using the **this** (C#) or **Me** (Visual Basic) keyword.</span></span> <span data-ttu-id="d72c7-150">Zugriff auf den Namen der Ansicht, müssen Sie Zugriff auf das [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) -Objekt, das der Ansicht zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d72c7-150">To access the name of the view, you need to access the [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) object associated with the view.</span></span> <span data-ttu-id="d72c7-151">Im folgenden Beispiel wird veranschaulicht, wie ein Meldungsfeld mit dem Namen der Ansicht anzuzeigen, die momentan aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="d72c7-151">The following example demonstrates how to display a message box with the name of the view that is currently active.</span></span> 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

<span data-ttu-id="d72c7-152">Alle InfoPath-Formularvorlagen enthalten mindestens eine Standardansicht. InfoPath unterstützt jedoch auch die Erstellung mehrerer Ansichten des einem Formular zugrunde liegenden XML-Dokument.</span><span class="sxs-lookup"><span data-stu-id="d72c7-152">All InfoPath form templates contain at least one default view; however, InfoPath also supports the creation of multiple views of a form's underlying XML document.</span></span> <span data-ttu-id="d72c7-153">Wenn Sie mehrere Ansichten hat, kann [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) entwickelt aller in der Formularvorlage implementierten Ansichten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d72c7-153">When you have multiple views, the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) can be used to work with all of the views implemented in the form template.</span></span> <span data-ttu-id="d72c7-154">Verwenden Sie den Zugriff auf die [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) einer Formularvorlage die [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) -Eigenschaft der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="d72c7-154">To access the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) of a form template, use the [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class.</span></span> <span data-ttu-id="d72c7-155">Sie können die Ansicht, die derzeit aktive wird mithilfe der [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) -Methode der [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , wie im folgenden Codebeispiel wird veranschaulicht, programmgesteuert ändern.</span><span class="sxs-lookup"><span data-stu-id="d72c7-155">You can programmatically change the view that is currently active by using the [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) method of the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , as the following code sample demonstrates.</span></span> 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

<span data-ttu-id="d72c7-156">Im vorherige Beispiel für den Wechsel von einer Ansicht funktioniert nur, wenn das Formular geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="d72c7-156">The previous example for switching a view will work only after the form is opened.</span></span> <span data-ttu-id="d72c7-157">Verwenden Sie die [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) -Eigenschaft der [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) -Klasse, um eine Standardansicht während der [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) -Ereignis festzulegen, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d72c7-157">To set a default view during the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event, use the [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) property of the [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) class as shown in the following example.</span></span> <span data-ttu-id="d72c7-158">Beachten Sie jedoch, dass dieser Wert nur in Kraft treten nach dem das Formular gespeichert und erneut geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="d72c7-158">Note, however, that this value will only take effect after the form is saved and re-opened.</span></span> 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a><span data-ttu-id="d72c7-159">Auswählen von Steuerelementen in einer Ansicht</span><span class="sxs-lookup"><span data-stu-id="d72c7-159">Selecting Controls in a View</span></span>

<span data-ttu-id="d72c7-160">InfoPath bietet zwei Methoden der [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Klasse, die beide überlastet sind, um ein Steuerelement in der aktuellen Ansicht programmgesteuert auswählen: die Methoden [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) und [SelectNodes()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d72c7-160">InfoPath provides two methods of the [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) class, both of which are overloaded, to programmatically select a control in the current view: the [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) and [SelectNodes()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) methods.</span></span> <span data-ttu-id="d72c7-161">Die [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) -Methode wird für die Dateneingabe-Steuerelemente, wie ein **Textfeld**, während die **SelectNodes** -Methode für strukturellen Steuerelemente, wie zum Beispiel ein **Optionaler Abschnitt**verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d72c7-161">The [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method is used for data entry controls, such as a **Text Box**, while the **SelectNodes** method is used for structural controls, such as an **Optional Section**.</span></span> <span data-ttu-id="d72c7-162">Um ein bestimmtes Steuerelement in der Ansicht auswählen, müssen Sie den Knoten und (optional) der ID des Steuerelements ViewContext bereitstellen</span><span class="sxs-lookup"><span data-stu-id="d72c7-162">To select a particular control in the view, you need to provide the node and, optionally, the control's ViewContext ID.</span></span> <span data-ttu-id="d72c7-163">Die ViewContext-ID ist erforderlich, wenn Sie mehrere Steuerelemente an demselben Knoten in der Datenquelle gebunden haben.</span><span class="sxs-lookup"><span data-stu-id="d72c7-163">The ViewContext ID is needed when you have multiple controls bound to the same node in the data source.</span></span> <span data-ttu-id="d72c7-164">InfoPath bietet die ViewContext-ID-Informationen, wenn Sie das Formular entwerfen.</span><span class="sxs-lookup"><span data-stu-id="d72c7-164">InfoPath provides the ViewContext ID information when you design the form.</span></span>
  
<span data-ttu-id="d72c7-165">Ein Steuerelement ViewContext-ID wird auf der Registerkarte **Erweitert** im Dialogfeld Eigenschaften des Steuerelements angezeigt, die zugegriffen wird, indem Sie mit der rechten Maustaste in des Steuerelements, auf _Steuerelementname_ **Eigenschaften**, und klicken Sie dann auf die Registerkarte **Erweitert** . Die ViewContext-ID des Steuerelements wird in **der Registerkarte **Erweitert** Codeabschnitt** aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d72c7-165">A control's ViewContext ID is displayed on the **Advanced** tab of the control's properties dialog box, which is accessed by right-clicking the control, clicking  _ControlName_ **Properties**, and then clicking the **Advanced** tab. The ViewContext ID of the control is listed in the **Code** section of the **Advanced** tab.</span></span> 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a><span data-ttu-id="d72c7-166">Verwendungszweck von "SelectText" und "SelectNodes"</span><span class="sxs-lookup"><span data-stu-id="d72c7-166">When to use SelectText and SelectNodes</span></span>

<span data-ttu-id="d72c7-167">Sie können die folgenden Dateneingabe-Steuerelemente programmgesteuert auswählen, mit der [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) -Methode:</span><span class="sxs-lookup"><span data-stu-id="d72c7-167">You can programmatically select the following data entry controls by using the [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) method:</span></span> 
  
- <span data-ttu-id="d72c7-168">Textfeld</span><span class="sxs-lookup"><span data-stu-id="d72c7-168">Text Box</span></span>
    
- <span data-ttu-id="d72c7-169">Rich-Text-Feld Box</span><span class="sxs-lookup"><span data-stu-id="d72c7-169">Rich Text Box</span></span>
    
- <span data-ttu-id="d72c7-170">Datumsauswahl</span><span class="sxs-lookup"><span data-stu-id="d72c7-170">Date Picker</span></span>
    
<span data-ttu-id="d72c7-171">Sie können die folgenden strukturellen Steuerelemente programmgesteuert auswählen, mit der [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) -Methode:</span><span class="sxs-lookup"><span data-stu-id="d72c7-171">You can programmatically select the following structural controls by using the [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) method:</span></span> 
  
- <span data-ttu-id="d72c7-172">Optionaler Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d72c7-172">Optional Section</span></span>
    
- <span data-ttu-id="d72c7-173">Auswahlabschnitt</span><span class="sxs-lookup"><span data-stu-id="d72c7-173">Choice Section</span></span>
    
- <span data-ttu-id="d72c7-174">Wiederholter Abschnitt (Elemente)</span><span class="sxs-lookup"><span data-stu-id="d72c7-174">Repeating Section (items)</span></span>
    
- <span data-ttu-id="d72c7-175">Wiederholte Tabelle (Zeilen)</span><span class="sxs-lookup"><span data-stu-id="d72c7-175">Repeating Table (rows)</span></span>
    
- <span data-ttu-id="d72c7-176">Wiederholter rekursiver Abschnitt (Elemente)</span><span class="sxs-lookup"><span data-stu-id="d72c7-176">Repeating Recursive Section (items)</span></span>
    
- <span data-ttu-id="d72c7-177">Aufzählung, Nummerierte Liste und Einfache Liste</span><span class="sxs-lookup"><span data-stu-id="d72c7-177">Bulleted, Numbered, and Plain List</span></span>
    
- <span data-ttu-id="d72c7-178">Horizontale wiederholte Tabelle</span><span class="sxs-lookup"><span data-stu-id="d72c7-178">Horizontal Repeating Table</span></span>
    
<span data-ttu-id="d72c7-179">Die folgenden Steuerelemente können nicht programmgesteuert ausgewählt werden, d. h. es ist nicht möglich, den Fokus programmgesteuert darauf zu setzen:</span><span class="sxs-lookup"><span data-stu-id="d72c7-179">You cannot programmatically select, or set focus to, the following controls:</span></span>
  
- <span data-ttu-id="d72c7-180">Dropdown-Listenfeld</span><span class="sxs-lookup"><span data-stu-id="d72c7-180">Drop-Down List Box</span></span>
    
- <span data-ttu-id="d72c7-181">Listenfeld</span><span class="sxs-lookup"><span data-stu-id="d72c7-181">List Box</span></span>
    
- <span data-ttu-id="d72c7-182">Kontrollkästchen</span><span class="sxs-lookup"><span data-stu-id="d72c7-182">Check Box</span></span>
    
- <span data-ttu-id="d72c7-183">Optionsfeld</span><span class="sxs-lookup"><span data-stu-id="d72c7-183">Option Button</span></span>
    
- <span data-ttu-id="d72c7-184">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="d72c7-184">Button</span></span>
    
- <span data-ttu-id="d72c7-185">Bild (verknüpft oder eingeschlossen)</span><span class="sxs-lookup"><span data-stu-id="d72c7-185">Picture (linked or included)</span></span>
    
- <span data-ttu-id="d72c7-186">Freihandzeichnung</span><span class="sxs-lookup"><span data-stu-id="d72c7-186">Ink Picture</span></span>
    
- <span data-ttu-id="d72c7-187">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="d72c7-187">Hyperlink</span></span>
    
- <span data-ttu-id="d72c7-188">Ausdrucksfeld</span><span class="sxs-lookup"><span data-stu-id="d72c7-188">Expression Box</span></span>
    
- <span data-ttu-id="d72c7-189">Vertikales Etikett</span><span class="sxs-lookup"><span data-stu-id="d72c7-189">Vertical Label</span></span>
    
- <span data-ttu-id="d72c7-190">ActiveX-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d72c7-190">ActiveX Section</span></span>
    
- <span data-ttu-id="d72c7-191">Horizontaler Bereich</span><span class="sxs-lookup"><span data-stu-id="d72c7-191">Horizontal Region</span></span>
    
## <a name="using-the-selecttext-and-selectnodes-methods"></a><span data-ttu-id="d72c7-192">Verwenden der "SelectText"- und der "SelectNodes"-Methode</span><span class="sxs-lookup"><span data-stu-id="d72c7-192">Using the SelectText and SelectNodes Methods</span></span>

<span data-ttu-id="d72c7-193">Im folgenden Beispiel wird die [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) Überladung der **SelectText** -Methode, die einen _XmlNode_ -Parameter bereitstellt, auszuwählenden gebunden ist ein **Textfeld** verwendet "Mein: Feld1".</span><span class="sxs-lookup"><span data-stu-id="d72c7-193">In the following example, the [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) overload of the **SelectText** method, which provides one  _xmlNode_ parameter, is used to select a **Text Box** that is bound to "my:field1".</span></span> 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

<span data-ttu-id="d72c7-194">Wenn Sie mehrere an gebundenen Steuerelemente haben "Mein: field1", müssen Sie die [SelectText (XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) Überladung der **SelectText** -Methode, die bietet einen zusätzliche _ViewContext_ -Parameter zum Auswählen eines bestimmten Steuerelements verwenden.</span><span class="sxs-lookup"><span data-stu-id="d72c7-194">If you have multiple controls bound to "my:field1", you must use the [SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) overload of the **SelectText** method, which provides an additional  _viewContext_ parameter to select a specific control.</span></span> <span data-ttu-id="d72c7-195">Im folgende Beispiel wird davon ausgegangen, dass es zwei **Textfeld** -Steuerelemente gibt an gebunden "Mein: field1", mit dem ersten Steuerelement mit der ViewContext-ID "CTRL1" und das zweite Steuerelement mit der ViewContext-ID "CTRL8".</span><span class="sxs-lookup"><span data-stu-id="d72c7-195">The following example assumes that there are two **Text Box** controls bound to "my:field1", with the first control having a ViewContext ID of "CTRL1" and the second control having a ViewContext ID of "CTRL8".</span></span> <span data-ttu-id="d72c7-196">Das zweite Steuerelement ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="d72c7-196">The second control is selected.</span></span> 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

<span data-ttu-id="d72c7-197">Im folgenden Beispiel wird die Überladung [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) , der die **SelectNodes** -Methode, die nur einen _Startknoten_ -Parameter bereitstellt, auf die erste Zeile in einer wiederholten Tabelle, die an die wiederholte Gruppe gebundenen auswählen verwendet "Mein: Mitarbeiter".</span><span class="sxs-lookup"><span data-stu-id="d72c7-197">In the following example, the [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) overload of the **SelectNodes** method, which provides only one  _startNode_ parameter, is used to select the first row in a repeating table bound to the repeating group "my:employee".</span></span> 
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

<span data-ttu-id="d72c7-198">Sie können auch mehrere Zeilen in einer wiederholten Tabelle auswählen.</span><span class="sxs-lookup"><span data-stu-id="d72c7-198">You can also select multiple rows in a repeating table.</span></span> <span data-ttu-id="d72c7-199">Im folgenden Beispiel wird die ersten drei Zeilen einer wiederholten Tabelle an die wiederholte Gruppe gebunden "Mein: Mitarbeiter" werden mithilfe der Überladung [SelectNodes (XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) , der die **SelectNodes** -Methode, die bietet ausgewählt  _Startknoten_ und _EndNode_ -Parameter:</span><span class="sxs-lookup"><span data-stu-id="d72c7-199">In the following example, the first three rows of a repeating table bound to the repeating group "my:employee" are selected using the [SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) overload of the **SelectNodes** method, which provides  _startNode_ and  _endNode_ parameters:</span></span> 
  
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


