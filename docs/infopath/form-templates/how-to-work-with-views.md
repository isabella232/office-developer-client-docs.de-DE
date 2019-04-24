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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303542"
---
# <a name="work-with-views"></a>Arbeiten mit Ansichten

Bei der Arbeit mit einer InfoPath-Formularvorlage können Sie Code schreiben, um auf die Ansichten des Formulars zuzugreifen, und dann eine Vielzahl von Aktionen für die in den Ansichten enthaltenen Daten ausführen. Das vom [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellte InfoPath-Objektmodell unterstützt den Zugriff auf die Ansichten eines Formulars durch die Verwendung der Member der [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Klasse. 
  
## <a name="overview-of-the-view-class"></a>Übersicht über die View-Klasse

Die [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Klasse stellt die folgenden Methoden und Eigenschaften bereit, die Formularentwickler für die Interaktion mit einer InfoPath-Ansicht verwenden können. 
  
> [!NOTE]
> Die Methoden und Eigenschaften der [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Klasse stehen während des [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) -Ereignisses nicht zur Verfügung. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx) -Methode  <br/> |Deaktiviert die automatische Synchronisierung zwischen dem einem Formular zugrunde liegenden XML-Dokument und der zugeordneten Ansicht.  <br/> |
|[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx) -Methode  <br/> |Aktiviert die automatische Synchronisierung zwischen dem einem Formular zugrunde liegenden XML-Dokument und der zugeordneten Ansicht.  <br/> |
|[Execute-Methode (Action Type)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)  <br/> |Führt basierend auf den Daten, die zurzeit in der Ansicht ausgewählt sind, einen Bearbeitungsbefehl für das einem Formular zugrunde liegende XML-Dokument aus.  <br/> |
|[Execute-Methode (Action Type, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx)  <br/> |Führt basierend auf dem angegebenen Feld oder der angegebenen Gruppe einen Bearbeitungsbefehl für das einem Formular zugrunde liegende XML-Dokument aus.  <br/> |
|[Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx) -Methode  <br/> |Exportiert die Ansicht in eine Datei des angegebenen Formats.  <br/> |
|[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx) -Methode  <br/> |Erzwingt die Synchronisierung zwischen dem einem Formular zugrunde liegenden XML-Dokument und der zugeordneten Ansicht.  <br/> |
|[GetContextNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) -Methode  <br/> |Ruft einen Verweis auf ein **XPathNodeIterator**-Objekt zum Durchlaufen der zurückgegebenen XML-Knoten beginnend beim angegebenen Knoten ab.  <br/> |
|[GetContextNodes (XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) -Methode  <br/> |Ruft einen Verweis auf ein **XPathNodeIterator**-Objekt zum Durchlaufen der zurückgegebenen XML-Knoten in der aktuellen Auswahl innerhalb des an das angegebene Feld oder an die angegebene Gruppe gebundenen Steuerelements ab.  <br/> |
|[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) -Methode  <br/> |Ruft einen Verweis auf ein **XPathNodeIterator**-Objekt zum Durchlaufen aller XML-Knoten in der aktuellen Auswahl von Elementen in einer Ansicht ab.  <br/> |
|[SelectNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) -Methode  <br/> |Wählt basierend auf dem angegebenen XML-Startknoten einen Bereich von Knoten in einer Ansicht aus.  <br/> |
|[SelectNodes (XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) -Methode  <br/> |Wählt basierend auf dem angegebenen XML-Startknoten und XML-Endknoten einen Bereich von Knoten in einer Ansicht aus.  <br/> |
|[SelectNodes (XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) -Methode  <br/> |Wählt basierend auf dem angegebenen XML-Startknoten, dem XML-Endknoten und dem angegebenen Steuerelement einen Bereich von Knoten in der Ansicht aus.  <br/> |
|[SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) -Methode  <br/> |Wählt den Text in einem bearbeitbaren Steuerelement aus, das an den Knoten gebunden ist, der durch das an diese Methode übergebene **XPathNavigator**-Objekt angegeben wird.  <br/> |
|[SelectText (XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) -Methode  <br/> |Wählt den Text in einem bearbeitbaren Steuerelement aus, das an den Knoten gebunden ist, der durch das an diese Methode übergebene **XPathNavigator**-Objekt angegeben wird, und das angegebene Steuerelement.  <br/> |
|[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx) -Methode  <br/> |Erstellt eine e-Mail-Nachricht mit der aktuellen Ansicht.  <br/> |
|[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf ein [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) -Objekt ab, das der Ansicht zugeordnet ist.  <br/> |
|[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf ein [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Objekt ab, das der Ansicht zugeordnet ist.  <br/> |
   
> [!NOTE]
> Das InfoPath-Objektmodell stellt auch [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) die ViewInfoCollection-und [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) -Klassen bereit, die zum Abrufen von Informationen zu allen in einem Formular implementierten Ansichten verwendet werden können. 
  
## <a name="using-the-view-class"></a>Verwenden der View-Klasse

Der Zugriff auf die [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Klasse erfolgt über die [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) -Eigenschaft der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse, auf die mithilfe des Schlüsselwortes **this** (C#) oder **Me** (Visual Basic) zugegriffen wird. Um auf den Namen der Ansicht zuzugreifen, müssen Sie auf das [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) -Objekt zugreifen, das der Ansicht zugeordnet ist. Das folgende Beispiel zeigt, wie ein Meldungsfeld mit dem Namen der momentan aktiven Ansicht angezeigt werden kann. 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

Alle InfoPath-Formularvorlagen enthalten mindestens eine Standardansicht. InfoPath unterstützt jedoch auch das Erstellen mehrerer Ansichten des einem Formular zugrunde liegenden XML-Dokuments. Wenn Sie über mehrere Ansichten verfügen, [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) kann die ViewInfoCollection verwendet werden, um mit allen in der Formularvorlage implementierten Ansichten zu arbeiten. Um auf die [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) einer Formularvorlage zuzugreifen, verwenden Sie die [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) - [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) Eigenschaft der XmlForm-Klasse. Sie können die derzeit aktive Ansicht programmgesteuert ändern, indem Sie die [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) -Methode der [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) verwenden, wie im folgenden Codebeispiel veranschaulicht. 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

Das obige Beispiel für das Wechseln einer Ansicht funktioniert nur nach dem Öffnen des Formulars. Verwenden Sie zum Festlegen einer Standardansicht während des [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) -Ereignisses die [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) -Eigenschaft der [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) -Klasse, wie im folgenden Beispiel gezeigt. Beachten Sie jedoch, dass dieser Wert erst wirksam wird, nachdem das Formular gespeichert und erneut geöffnet wurde. 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a>Auswählen von Steuerelementen in einer Ansicht

InfoPath stellt zwei Methoden der [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Klasse bereit, die beide überlastet sind, um ein Steuerelement in der aktuellen Ansicht programmgesteuert auszuwählen: die Methoden [SelectText ()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) und [SelectNodes ()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) . Die [SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) -Methode wird für Dateneingabe Steuerelemente wie ein **Textfeld**verwendet, während die **SelectNodes** -Methode für strukturelle Steuerelemente wie einen **optionalen Abschnitt**verwendet wird. Zum Auswählen eines bestimmten Steuerelements in der Ansicht müssen Sie den Knoten und optional den ViewContext-Bezeichner des Steuerelements bereitstellen. Den ViewContext-Bezeichner benötigen Sie, wenn Sie mehrere Steuerelemente haben, die an den gleichen Knoten in der Datenquelle gebunden sind. InfoPath stellt die Informationen für den ViewContext-Bezeichner bereit, wenn Sie das Formular entwerfen.
  
Die ViewContext-ID eines Steuerelements wird auf der Registerkarte **erweitert** des Dialogfelds Eigenschaften des Steuerelements angezeigt, auf das durch Klicken mit der rechten Maustaste auf das Steuerelement, klicken auf _Steuerelement_ **Eigenschaften**und klicken auf die Registerkarte **erweitert** zugegriffen wird. Die ViewContext-ID des Steuerelements wird im Abschnitt **Code** der Registerkarte **erweitert** aufgeführt. 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a>Verwendungszweck von "SelectText" und "SelectNodes"

Mithilfe der [SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) -Methode können Sie die folgenden Dateneingabe-Steuerelemente programmgesteuert auswählen: 
  
- Textfeld
    
- Rich-Text-Feld Box
    
- Datumsauswahl
    
Mithilfe der [SelectNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) -Methode können Sie die folgenden strukturellen Steuerelemente programmgesteuert auswählen: 
  
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

Im folgenden Beispiel wird die [SelectText (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) -überLadung der **SelectText** -Methode, die einen _XmlNode_ -Parameter bereitStellt, zum Auswählen eines Textfelds verwendet, das an "My: Feld1" gebunden ist. **** 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

Wenn Sie mehrere Steuerelemente an "My: Feld1" gebunden haben, müssen Sie die [SelectText (XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) -überLadung der **SelectText** -Methode verwenden, die einen zusätzlichen _ViewContext_ -Parameter zum Auswählen eines bestimmten Steuerelements bereitstellt. Im folgenden Beispiel wird davon ausgegangen, dass zwei **Textfeld** -Steuerelemente an "My: Feld1" gebunden sind, wobei das erste Steuerelement eine VIEWCONTEXT-ID von "CTRL1" und das zweite Steuerelement eine VIEWCONTEXT-ID von "CTRL8" hat. Das zweite Steuerelement ist ausgewählt. 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

Im folgenden Beispiel wird die [SelectNodes (XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) -überLadung der **SelectNodes** -Methode, die nur einen _startNode_ -Parameter bereitstellt, zum Auswählen der ersten Zeile in einer wiederholten Tabelle verwendet, die an die wiederholte Gruppe "My: Employee ". 
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

Sie können auch mehrere Zeilen in einer wiederholten Tabelle auswählen. Im folgenden Beispiel werden die ersten drei Zeilen einer wiederholten Tabelle, die an die wiederholte Gruppe "My: Employee" gebunden sind, mit der SelectNodes-Überladung [(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) der **SelectNodes** -Methode ausgewählt, die  Parameter _startNode_ und _Endnode_ : 
  
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


