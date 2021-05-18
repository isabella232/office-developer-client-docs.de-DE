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
# <a name="work-with-views"></a>Arbeiten mit Ansichten

Bei der Arbeit mit einer InfoPath-Formularvorlage können Sie Code schreiben, um auf die Ansichten des Formulars zuzugreifen, und dann eine Vielzahl von Aktionen für die in den Ansichten enthaltenen Daten ausführen. Das vom [Microsoft.Office.InfoPath-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) bereitgestellte InfoPath-Objektmodell unterstützt den Zugriff auf die Ansichten eines Formulars mithilfe der Elemente der [View-Klasse.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) 
  
## <a name="overview-of-the-view-class"></a>Übersicht über die View-Klasse

Die [View-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) stellt die folgenden Methoden und Eigenschaften zur Verfügung, mit denen Formularentwickler mit einer InfoPath-Ansicht interagieren können. 
  
> [!NOTE]
> Die Methoden und Eigenschaften der [View-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) sind während des Loading-Ereignisses [nicht](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) verfügbar. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[DisableAutoUpdate-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx)  <br/> |Deaktiviert die automatische Synchronisierung zwischen dem einem Formular zugrunde liegenden XML-Dokument und der zugeordneten Ansicht.  <br/> |
|[EnableAutoUpdate-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx)  <br/> |Aktiviert die automatische Synchronisierung zwischen dem einem Formular zugrunde liegenden XML-Dokument und der zugeordneten Ansicht.  <br/> |
|[ExecuteAction(ActionType)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)  <br/> |Führt basierend auf den Daten, die zurzeit in der Ansicht ausgewählt sind, einen Bearbeitungsbefehl für das einem Formular zugrunde liegende XML-Dokument aus.  <br/> |
|[ExecuteAction(ActionType, String)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)  <br/> |Führt basierend auf dem angegebenen Feld oder der angegebenen Gruppe einen Bearbeitungsbefehl für das einem Formular zugrunde liegende XML-Dokument aus.  <br/> |
|[Exportmethode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx)  <br/> |Exportiert die Ansicht in eine Datei des angegebenen Formats.  <br/> |
|[ForceUpdate-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx)  <br/> |Erzwingt die Synchronisierung zwischen dem einem Formular zugrunde liegenden XML-Dokument und der zugeordneten Ansicht.  <br/> |
|[GetContextNodes(XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |Ruft einen Verweis auf ein **XPathNodeIterator**-Objekt zum Durchlaufen der zurückgegebenen XML-Knoten beginnend beim angegebenen Knoten ab.  <br/> |
|[GetContextNodes(XPathNavigator, String)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |Ruft einen Verweis auf ein **XPathNodeIterator**-Objekt zum Durchlaufen der zurückgegebenen XML-Knoten in der aktuellen Auswahl innerhalb des an das angegebene Feld oder an die angegebene Gruppe gebundenen Steuerelements ab.  <br/> |
|[GetSelectedNodes-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)  <br/> |Ruft einen Verweis auf ein **XPathNodeIterator**-Objekt zum Durchlaufen aller XML-Knoten in der aktuellen Auswahl von Elementen in einer Ansicht ab.  <br/> |
|[SelectNodes(XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Wählt basierend auf dem angegebenen XML-Startknoten einen Bereich von Knoten in einer Ansicht aus.  <br/> |
|[SelectNodes(XPathNavigator, XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Wählt basierend auf dem angegebenen XML-Startknoten und XML-Endknoten einen Bereich von Knoten in einer Ansicht aus.  <br/> |
|[SelectNodes(XPathNavigator, XPathNavigator, String)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |Wählt basierend auf dem angegebenen XML-Startknoten, dem XML-Endknoten und dem angegebenen Steuerelement einen Bereich von Knoten in der Ansicht aus.  <br/> |
|[SelectText(XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |Wählt den Text in einem bearbeitbaren Steuerelement aus, das an den Knoten gebunden ist, der durch das an diese Methode übergebene **XPathNavigator**-Objekt angegeben wird.  <br/> |
|[SelectText(XPathNavigator, String)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |Wählt den Text in einem bearbeitbaren Steuerelement aus, das an den Knoten gebunden ist, der durch das an diese Methode übergebene **XPathNavigator**-Objekt angegeben wird, und das angegebene Steuerelement.  <br/> |
|[ShowMailItem-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx)  <br/> |Erstellt eine E-Mail-Nachricht, die die aktuelle Ansicht enthält.  <br/> |
|[ViewInfo-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx)  <br/> |Ruft einen Verweis auf ein [ViewInfo-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) ab, das der Ansicht zugeordnet ist.  <br/> |
|[Window-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx)  <br/> |Ruft einen Verweis auf ein [Window-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) ab, das der Ansicht zugeordnet ist.  <br/> |
   
> [!NOTE]
> Das InfoPath-Objektmodell stellt auch die [ViewInfoCollection-](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) und [ViewInfo-Klassen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) zur Verfügung, die zum Abrufen von Informationen zu allen in einem Formular implementierten Ansichten verwendet werden können. 
  
## <a name="using-the-view-class"></a>Verwenden der View-Klasse

Auf [die View-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) wird über die [CurrentView-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) der [XmlForm-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) zugegriffen, auf die mithilfe des Schlüsselworts this **(C#)** oder **Me** (Visual Basic) zugegriffen wird. Um auf den Namen der Ansicht zu zugreifen, müssen Sie auf das [ViewInfo-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) zugreifen, das der Ansicht zugeordnet ist. Das folgende Beispiel zeigt, wie ein Meldungsfeld mit dem Namen der momentan aktiven Ansicht angezeigt werden kann. 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

Alle #A0 enthalten mindestens eine Standardansicht. InfoPath unterstützt jedoch auch das Erstellen mehrerer Ansichten des einem Formular zugrunde liegenden XML-Dokuments. Wenn Sie über mehrere Ansichten verfügen, kann [die ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) verwendet werden, um mit allen in der Formularvorlage implementierten Ansichten zu arbeiten. Um auf [die ViewInfoCollection einer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) Formularvorlage zu zugreifen, verwenden Sie die [ViewInfos-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) der [XmlForm-Klasse.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) Sie können die derzeit aktive Ansicht programmgesteuert ändern, indem Sie die [SwitchView-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) der [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) verwenden, wie im folgenden Codebeispiel veranschaulicht wird. 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

Das obige Beispiel für das Wechseln einer Ansicht funktioniert nur nach dem Öffnen des Formulars. Verwenden Sie zum Festlegen [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) einer Standardansicht während des Loading-Ereignisses die [Initial-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) der [ViewInfoCollection-Klasse,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) wie im folgenden Beispiel gezeigt. Beachten Sie jedoch, dass dieser Wert erst wirksam wird, nachdem das Formular gespeichert und erneut geöffnet wurde. 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a>Auswählen von Steuerelementen in einer Ansicht

InfoPath bietet zwei [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) Methoden der View-Klasse, die beide überladen sind, um programmgesteuert ein Steuerelement in der aktuellen Ansicht auszuwählen: die [Methoden SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) und [SelectNodes().](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) Die [SelectText(XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) wird für Dateneingabesteuerelemente wie ein **Textfeld** verwendet, während die **SelectNodes-Methode** für Struktursteuerelemente verwendet wird, z. B. einen **optionalen Abschnitt**. Zum Auswählen eines bestimmten Steuerelements in der Ansicht müssen Sie den Knoten und optional den ViewContext-Bezeichner des Steuerelements bereitstellen. Den ViewContext-Bezeichner benötigen Sie, wenn Sie mehrere Steuerelemente haben, die an den gleichen Knoten in der Datenquelle gebunden sind. InfoPath stellt die Informationen für den ViewContext-Bezeichner bereit, wenn Sie das Formular entwerfen.
  
Die ViewContext-ID eines Steuerelements  wird auf der Registerkarte Erweitert des Eigenschaftendialogfelds des Steuerelements angezeigt, auf das zugegriffen wird, indem mit der rechten Maustaste auf das Steuerelement geklickt wird, auf _ControlName-Eigenschaften_ und dann auf die Registerkarte **Erweitert.** Die ViewContext-ID des Steuerelements wird im Abschnitt **Code** auf der Registerkarte **Erweitert** aufgeführt. 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a>Verwendungszweck von "SelectText" und "SelectNodes"

Mit der [SelectText(XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) können Sie programmgesteuert die folgenden Dateneingabesteuerelemente auswählen: 
  
- Textfeld
    
- Rich-Text-Feld Box
    
- Datumsauswahl
    
Mithilfe der [SelectNodes(XPathNavigator)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) können Sie die folgenden Struktursteuerelemente programmgesteuert auswählen: 
  
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

Im folgenden Beispiel wird die [SelectText(XPathNavigator)-Überladung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) der **SelectText-Methode,** die einen  _xmlNode-Parameter_ enthält, verwendet, um ein Textfeld auszuwählen, das an "my:field1" gebunden ist. 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

Wenn mehrere Steuerelemente an "my:field1" gebunden sind, müssen Sie die [SelectText(XPathNavigator, String)-Überladung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) der **SelectText-Methode** verwenden, die einen zusätzlichen  _viewContext-Parameter_ zur Auswahl eines bestimmten Steuerelements bietet. Im folgenden Beispiel wird davon  ausgegangen, dass zwei Textfeldsteuerelemente an "my:field1" gebunden sind, mit dem ersten Steuerelement mit der ViewContext-ID "STRG1" und dem zweiten Steuerelement mit der ViewContext-ID "STRG8". Das zweite Steuerelement ist ausgewählt. 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

Im folgenden Beispiel wird die [SelectNodes(XPathNavigator)-Überladung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) der **SelectNodes-Methode,** die nur einen  _startNode-Parameter_ enthält, verwendet, um die erste Zeile in einer wiederholten Tabelle auszuwählen, die an die wiederholte Gruppe "my:employee" gebunden ist. 
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

Sie können auch mehrere Zeilen in einer wiederholten Tabelle auswählen. Im folgenden Beispiel werden die ersten drei Zeilen einer wiederholten Tabelle, die an die wiederholte Gruppe "my:employee" gebunden ist, mithilfe der [SelectNodes(XPathNavigator, XPathNavigator, String)-Überladung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) der **SelectNodes-Methode** ausgewählt, die  _die Parameter startNode_ und  _endNode_ enthält: 
  
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


