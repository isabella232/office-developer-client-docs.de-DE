---
title: Arbeiten mit Ansichten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- view-Klasse [infopath 2007],InfoPath 2007, working with views,views [InfoPath 2007]
ms.localizationpriority: medium
ms.assetid: 947b33c3-2acc-45d2-a89d-a712b6bc53df
description: Bei der Arbeit mit einer InfoPath-Formularvorlage können Sie Code schreiben, um auf die Ansichten des Formulars zuzugreifen, und dann eine Vielzahl von Aktionen für die in den Ansichten enthaltenen Daten ausführen. Das von Microsoft bereitgestellte InfoPath-Objektmodell. Office. Der InfoPath-Namespace unterstützt den Zugriff auf die Ansichten eines Formulars durch die Verwendung der Member der View-Klasse.
ms.openlocfilehash: ac870441f2e8e6f780eaaa45dc0ee26e7c3cf25a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625833"
---
# <a name="work-with-views"></a>Arbeiten mit Ansichten

Bei der Arbeit mit einer InfoPath-Formularvorlage können Sie Code schreiben, um auf die Ansichten des Formulars zuzugreifen, und dann eine Vielzahl von Aktionen für die in den Ansichten enthaltenen Daten ausführen. Das infoPath-Objektmodell, das von [Microsoft.Office bereitgestellt wird. Der InfoPath-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) unterstützt den Zugriff auf die Ansichten eines Formulars durch die Verwendung der Member der [View-Klasse.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) 
  
## <a name="overview-of-the-view-class"></a>Übersicht über die View-Klasse

Die [View-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) stellt die folgenden Methoden und Eigenschaften bereit, die Formularentwickler für die Interaktion mit einer InfoPath-Ansicht verwenden können. 
  
> [!NOTE]
> Die Methoden und Eigenschaften der [View-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) sind während des [Loading-Ereignisses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) nicht verfügbar. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[DisableAutoUpdate-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx)  <br/> |Deaktiviert die automatische Synchronisierung zwischen dem einem Formular zugrunde liegenden XML-Dokument und der zugeordneten Ansicht.  <br/> |
|[EnableAutoUpdate-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx)  <br/> |Aktiviert die automatische Synchronisierung zwischen dem einem Formular zugrunde liegenden XML-Dokument und der zugeordneten Ansicht.  <br/> |
|[ExecuteAction(ActionType)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)  <br/> |Führt basierend auf den Daten, die zurzeit in der Ansicht ausgewählt sind, einen Bearbeitungsbefehl für das einem Formular zugrunde liegende XML-Dokument aus.  <br/> |
|[ExecuteAction(ActionType, String)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)  <br/> |Führt basierend auf dem angegebenen Feld oder der angegebenen Gruppe einen Bearbeitungsbefehl für das einem Formular zugrunde liegende XML-Dokument aus.  <br/> |
|[Export-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx)  <br/> |Exportiert die Ansicht in eine Datei des angegebenen Formats.  <br/> |
|[ForceUpdate-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx)  <br/> |Erzwingt die Synchronisierung zwischen dem einem Formular zugrunde liegenden XML-Dokument und der zugeordneten Ansicht.  <br/> |
|[GetContextNodes(XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |Ruft einen Verweis auf ein **XPathNodeIterator**-Objekt zum Durchlaufen der zurückgegebenen XML-Knoten beginnend beim angegebenen Knoten ab.  <br/> |
|[GetContextNodes(XPathNavigator, String)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |Ruft einen Verweis auf ein **XPathNodeIterator**-Objekt zum Durchlaufen der zurückgegebenen XML-Knoten in der aktuellen Auswahl innerhalb des an das angegebene Feld oder an die angegebene Gruppe gebundenen Steuerelements ab.  <br/> |
|[GetSelectedNodes-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)  <br/> |Ruft einen Verweis auf ein **XPathNodeIterator**-Objekt zum Durchlaufen aller XML-Knoten in der aktuellen Auswahl von Elementen in einer Ansicht ab.  <br/> |
|[SelectNodes(XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Wählt basierend auf dem angegebenen XML-Startknoten einen Bereich von Knoten in einer Ansicht aus.  <br/> |
|[SelectNodes(XPathNavigator, XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Wählt basierend auf dem angegebenen XML-Startknoten und XML-Endknoten einen Bereich von Knoten in einer Ansicht aus.  <br/> |
|[SelectNodes(XPathNavigator,XPathNavigator, String)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Wählt basierend auf dem angegebenen XML-Startknoten, dem XML-Endknoten und dem angegebenen Steuerelement einen Bereich von Knoten in der Ansicht aus.  <br/> |
|[SelectText(XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |Wählt den Text in einem bearbeitbaren Steuerelement aus, das an den Knoten gebunden ist, der durch das an diese Methode übergebene **XPathNavigator**-Objekt angegeben wird.  <br/> |
|[SelectText(XPathNavigator, String)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |Wählt den Text in einem bearbeitbaren Steuerelement aus, das an den Knoten gebunden ist, der durch das an diese Methode übergebene **XPathNavigator**-Objekt angegeben wird, und das angegebene Steuerelement.  <br/> |
|[ShowMailItem-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx)  <br/> |Erstellt eine E-Mail-Nachricht mit der aktuellen Ansicht.  <br/> |
|[ViewInfo-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx)  <br/> |Ruft einen Verweis auf ein [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) -Objekt ab, das der Ansicht zugeordnet ist.  <br/> |
|[Window-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx)  <br/> |Ruft einen Verweis auf ein [Window -Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) ab, das der Ansicht zugeordnet ist.  <br/> |
   
> [!NOTE]
> Das InfoPath-Objektmodell stellt auch die [Klassen ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) und ViewInfo bereit, die zum Abrufen von Informationen zu allen in einem Formular implementierten Ansichten verwendet werden können. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) 
  
## <a name="using-the-view-class"></a>Verwenden der View-Klasse

Der Zugriff auf die [View-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) erfolgt über die [CurrentView-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) der [XmlForm-Klasse,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) auf die mithilfe des Schlüsselworts C# oder Me (Visual Basic) zugegriffen wird.   Um auf den Namen der Ansicht zuzugreifen, müssen Sie auf das [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) -Objekt zugreifen, das der Ansicht zugeordnet ist. Das folgende Beispiel zeigt, wie ein Meldungsfeld mit dem Namen der momentan aktiven Ansicht angezeigt werden kann. 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

Alle InfoPath-Formularvorlagen enthalten mindestens eine Standardansicht. InfoPath unterstützt jedoch auch das Erstellen mehrerer Ansichten des einem Formular zugrunde liegenden XML-Dokuments. Wenn Sie mehrere Ansichten haben, kann [die ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) verwendet werden, um mit allen Ansichten zu arbeiten, die in der Formularvorlage implementiert sind. Um auf die [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) einer Formularvorlage zuzugreifen, verwenden Sie die [ViewInfos-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) der [XmlForm-Klasse.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) Sie können die aktuell aktive Ansicht programmgesteuert ändern, indem Sie die [SwitchView-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) der [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) verwenden, wie im folgenden Codebeispiel veranschaulicht. 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

Das obige Beispiel für das Wechseln einer Ansicht funktioniert nur nach dem Öffnen des Formulars. Wenn Sie während des [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) Loading-Ereignisses eine Standardansicht festlegen möchten, verwenden Sie die [Initial-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) der [ViewInfoCollection-Klasse,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) wie im folgenden Beispiel gezeigt. Beachten Sie jedoch, dass dieser Wert erst wirksam wird, nachdem das Formular gespeichert und erneut geöffnet wurde. 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a>Auswählen von Steuerelementen in einer Ansicht

InfoPath stellt zwei Methoden der [View-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) bereit, die beide überladen sind, um programmgesteuert ein Steuerelement in der aktuellen Ansicht auszuwählen: die [Methoden SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) und [SelectNodes().](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) Die [SelectText(XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) wird für Dateneingabesteuerelemente wie z. B. ein **Textfeld** verwendet, während die **SelectNodes-Methode** für strukturelle Steuerelemente verwendet wird, z. B. ein **optionaler Abschnitt.** Zum Auswählen eines bestimmten Steuerelements in der Ansicht müssen Sie den Knoten und optional den ViewContext-Bezeichner des Steuerelements bereitstellen. Den ViewContext-Bezeichner benötigen Sie, wenn Sie mehrere Steuerelemente haben, die an den gleichen Knoten in der Datenquelle gebunden sind. InfoPath stellt die Informationen für den ViewContext-Bezeichner bereit, wenn Sie das Formular entwerfen.
  
Die ViewContext-ID eines Steuerelements wird auf der Registerkarte **"Erweitert"** des Dialogfelds "Eigenschaften" des Steuerelements angezeigt, auf das zugegriffen wird, indem Sie mit der rechten Maustaste auf das Steuerelement klicken, auf _"ControlName-Eigenschaften"_ klicken und dann auf die Registerkarte **"Erweitert"** klicken. Die ViewContext-ID des Steuerelements ist im **Codeabschnitt** der Registerkarte **"Erweitert"** aufgeführt. 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a>Verwendungszweck von "SelectText" und "SelectNodes"

Mithilfe der [SelectText(XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) können Sie die folgenden Dateneingabesteuerelemente programmgesteuert auswählen: 
  
- Textfeld
    
- Rich-Text-Feld Box
    
- Datumsauswahl
    
Mithilfe der [SelectNodes(XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) können Sie die folgenden strukturellen Steuerelemente programmgesteuert auswählen: 
  
- Optionaler Abschnitt
    
- Auswahlabschnitt
    
- Wiederholter Abschnitt (Elemente)
    
- Wiederholte Tabelle (Zeilen)
    
- Wiederholter rekursiver Abschnitt (Elemente)
    
- Aufzählung, Nummerierte Liste und Einfache Liste
    
- Horizontale wiederholte Tabelle
    
Die folgenden Steuerelemente können nicht programmgesteuert ausgewählt werden, d. h. es ist nicht möglich, den Fokus programmgesteuert darauf zu setzen:
  
- Dropdown-Listenfeld
    
- Listenfeld
    
- Kontrollkästchen
    
- Optionsfeld
    
- Schaltfläche
    
- Bild (verknüpft oder eingeschlossen)
    
- Freihandzeichnung
    
- Hyperlink
    
- Ausdrucksfeld
    
- Vertikales Etikett
    
- ActiveX-Abschnitt
    
- Horizontaler Bereich
    
## <a name="using-the-selecttext-and-selectnodes-methods"></a>Verwenden der "SelectText"- und der "SelectNodes"-Methode

Im folgenden Beispiel wird die [SelectText(XPathNavigator)-Überladung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) der **SelectText-Methode,** die einen  _xmlNode-Parameter_ bereitstellt, verwendet, um ein **Textfeld** auszuwählen, das an "my:field1" gebunden ist. 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

Wenn mehrere Steuerelemente an "my:field1" gebunden sind, müssen Sie die [SelectText(XPathNavigator, String)-Überladung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) der **SelectText-Methode** verwenden, die einen zusätzlichen  _viewContext-Parameter_ zum Auswählen eines bestimmten Steuerelements bereitstellt. Im folgenden Beispiel wird davon ausgegangen, dass zwei **Textfeld-Steuerelemente** an "my:field1" gebunden sind, wobei das erste Steuerelement die ViewContext-ID "STRG1" und das zweite Steuerelement die ViewContext-ID "STRG8" aufweist. Das zweite Steuerelement ist ausgewählt. 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

Im folgenden Beispiel wird die [SelectNodes(XPathNavigator)-Überladung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) der **SelectNodes-Methode,** die nur einen  _startNode-Parameter_ bereitstellt, verwendet, um die erste Zeile in einer wiederholten Tabelle auszuwählen, die an die wiederholte Gruppe "my:employee" gebunden ist. 
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

Sie können auch mehrere Zeilen in einer wiederholten Tabelle auswählen. Im folgenden Beispiel werden die ersten drei Zeilen einer wiederholten Tabelle, die an die wiederholte Gruppe "my:employee" gebunden sind, mithilfe der [SelectNodes(XPathNavigator, XPathNavigator, String)-Überladung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) der **SelectNodes-Methode** ausgewählt, die  _startNode-_ und  _endNode-Parameter_ bereitstellt: 
  
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


