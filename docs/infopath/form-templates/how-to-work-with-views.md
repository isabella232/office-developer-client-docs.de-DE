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
# <a name="work-with-views"></a>Arbeiten mit Ansichten

Bei der Arbeit mit InfoPath-Formularvorlage können Sie Code schreiben, um die Ansichten des Formulars zuzugreifen, und klicken Sie dann auf die Daten, die die Ansichten enthalten eine Vielzahl von Aktionen ausführen. Das InfoPath-Objektmodell zur Verfügung gestellt, durch die [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace unterstützt den Zugriff auf die Ansichten eines Formulars durch Verwendung der Member der [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Klasse. 
  
## <a name="overview-of-the-view-class"></a>Übersicht über die View-Klasse

[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Klasse bietet die folgenden Methoden und Eigenschaften, die Formularentwickler für die Interaktion mit einer InfoPath-Ansicht verwenden können. 
  
> [!NOTE]
> Die Methoden und Eigenschaften der [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Klasse sind während der [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) -Ereignis nicht verfügbar. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx) -Methode  <br/> |Deaktiviert die automatische Synchronisierung zwischen dem einem Formular zugrunde liegenden XML-Dokument und der zugeordneten Ansicht.  <br/> |
|[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx) -Methode  <br/> |Aktiviert die automatische Synchronisierung zwischen dem einem Formular zugrunde liegenden XML-Dokument und der zugeordneten Ansicht.  <br/> |
|[ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) -Methode  <br/> |Führt basierend auf den Daten, die zurzeit in der Ansicht ausgewählt sind, einen Bearbeitungsbefehl für das einem Formular zugrunde liegende XML-Dokument aus.  <br/> |
|[ExecuteAction (ActionType, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) -Methode  <br/> |Führt basierend auf dem angegebenen Feld oder der angegebenen Gruppe einen Bearbeitungsbefehl für das einem Formular zugrunde liegende XML-Dokument aus.  <br/> |
|[Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx) -Methode  <br/> |Exportiert die Ansicht in eine Datei des angegebenen Formats.  <br/> |
|[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx) -Methode  <br/> |Erzwingt die Synchronisierung zwischen dem einem Formular zugrunde liegenden XML-Dokument und der zugeordneten Ansicht.  <br/> |
|[GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) -Methode  <br/> |Ruft einen Verweis auf ein **XPathNodeIterator** -Objekt zum Durchlaufen der zurückgegebenen XML-Knoten beginnend beim angegebenen Knoten ab.  <br/> |
|[(XPathNavigator, String) GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) -Methode  <br/> |Ruft einen Verweis auf ein **XPathNodeIterator** -Objekt zum Durchlaufen der zurückgegebenen XML-Knoten in der aktuellen Auswahl innerhalb des an das angegebene Feld oder Gruppe gebundenen Steuerelements ab.  <br/> |
|[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) -Methode  <br/> |Ruft einen Verweis auf ein **XPathNodeIterator** -Objekt zum Durchlaufen aller XML-Knoten in der aktuellen Auswahl von Elementen in einer Ansicht ab.  <br/> |
|[SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) -Methode  <br/> |Wählt basierend auf dem angegebenen XML-Startknoten einen Bereich von Knoten in einer Ansicht aus.   <br/> |
|[SelectNodes (XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) -Methode  <br/> |Wählt basierend auf dem angegebenen XML-Startknoten und XML-Endknoten einen Bereich von Knoten in einer Ansicht aus.  <br/> |
|[SelectNodes (XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) -Methode  <br/> |Wählt basierend auf dem angegebenen XML-Startknoten, dem XML-Endknoten und dem angegebenen Steuerelement einen Bereich von Knoten in der Ansicht aus.   <br/> |
|[SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) -Methode  <br/> |Wählt den Text in einem bearbeitbaren Steuerelement aus, das auf den durch das an diese Methode übergebene **XPathNavigator** -Objekt angegebenen Knoten gebunden ist.  <br/> |
|[(XPathNavigator, String) SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) -Methode  <br/> |Wählt den Text in einem bearbeitbaren Steuerelement aus, das auf den durch das an diese Methode übergebene **XPathNavigator** -Objekt angegebenen Knoten gebunden ist und das angegebene Steuerelement.  <br/> |
|[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx) -Methode  <br/> |Erstellt eine e-Mail-Nachricht, die die aktuelle Ansicht enthält.  <br/> |
|[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf ein [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) -Objekt, das der Ansicht zugeordnet.  <br/> |
|[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf ein [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Objekt, das der Ansicht zugeordnet.  <br/> |
   
> [!NOTE]
> Das InfoPath-Objektmodell stellt auch die [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) und [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) -Klasse, die zum Abrufen von Informationen zu allen in einem Formular implementierten Ansichten verwendet werden kann. 
  
## <a name="using-the-view-class"></a>Verwenden der View-Klasse

[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Klasse erfolgt über die [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) -Eigenschaft der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse, die mit dem **dieser** (c#) oder Schlüsselwort **Me** (Visual Basic) zugegriffen wird. Zugriff auf den Namen der Ansicht, müssen Sie Zugriff auf das [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) -Objekt, das der Ansicht zugeordnet. Im folgenden Beispiel wird veranschaulicht, wie ein Meldungsfeld mit dem Namen der Ansicht anzuzeigen, die momentan aktiv ist. 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

Alle InfoPath-Formularvorlagen enthalten mindestens eine Standardansicht. InfoPath unterstützt jedoch auch die Erstellung mehrerer Ansichten des einem Formular zugrunde liegenden XML-Dokument. Wenn Sie mehrere Ansichten hat, kann [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) entwickelt aller in der Formularvorlage implementierten Ansichten verwendet werden. Verwenden Sie den Zugriff auf die [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) einer Formularvorlage die [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) -Eigenschaft der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse. Sie können die Ansicht, die derzeit aktive wird mithilfe der [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) -Methode der [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) , wie im folgenden Codebeispiel wird veranschaulicht, programmgesteuert ändern. 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

Im vorherige Beispiel für den Wechsel von einer Ansicht funktioniert nur, wenn das Formular geöffnet wird. Verwenden Sie die [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) -Eigenschaft der [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) -Klasse, um eine Standardansicht während der [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) -Ereignis festzulegen, wie im folgenden Beispiel dargestellt. Beachten Sie jedoch, dass dieser Wert nur in Kraft treten nach dem das Formular gespeichert und erneut geöffnet wird. 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a>Auswählen von Steuerelementen in einer Ansicht

InfoPath bietet zwei Methoden der [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Klasse, die beide überlastet sind, um ein Steuerelement in der aktuellen Ansicht programmgesteuert auswählen: die Methoden [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) und [SelectNodes()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) . Die [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) -Methode wird für die Dateneingabe-Steuerelemente, wie ein **Textfeld**, während die **SelectNodes** -Methode für strukturellen Steuerelemente, wie zum Beispiel ein **Optionaler Abschnitt**verwendet wird. Um ein bestimmtes Steuerelement in der Ansicht auswählen, müssen Sie den Knoten und (optional) der ID des Steuerelements ViewContext bereitstellen Die ViewContext-ID ist erforderlich, wenn Sie mehrere Steuerelemente an demselben Knoten in der Datenquelle gebunden haben. InfoPath bietet die ViewContext-ID-Informationen, wenn Sie das Formular entwerfen.
  
Ein Steuerelement ViewContext-ID wird auf der Registerkarte **Erweitert** im Dialogfeld Eigenschaften des Steuerelements angezeigt, die zugegriffen wird, indem Sie mit der rechten Maustaste in des Steuerelements, auf _Steuerelementname_ **Eigenschaften**, und klicken Sie dann auf die Registerkarte **Erweitert** . Die ViewContext-ID des Steuerelements wird in **der Registerkarte **Erweitert** Codeabschnitt** aufgeführt. 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a>Verwendungszweck von "SelectText" und "SelectNodes"

Sie können die folgenden Dateneingabe-Steuerelemente programmgesteuert auswählen, mit der [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) -Methode: 
  
- Textfeld
    
- Rich-Text-Feld Box
    
- Datumsauswahl
    
Sie können die folgenden strukturellen Steuerelemente programmgesteuert auswählen, mit der [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) -Methode: 
  
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

Im folgenden Beispiel wird die [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) Überladung der **SelectText** -Methode, die einen _XmlNode_ -Parameter bereitstellt, auszuwählenden gebunden ist ein **Textfeld** verwendet "Mein: Feld1". 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

Wenn Sie mehrere an gebundenen Steuerelemente haben "Mein: field1", müssen Sie die [SelectText (XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) Überladung der **SelectText** -Methode, die bietet einen zusätzliche _ViewContext_ -Parameter zum Auswählen eines bestimmten Steuerelements verwenden. Im folgende Beispiel wird davon ausgegangen, dass es zwei **Textfeld** -Steuerelemente gibt an gebunden "Mein: field1", mit dem ersten Steuerelement mit der ViewContext-ID "CTRL1" und das zweite Steuerelement mit der ViewContext-ID "CTRL8". Das zweite Steuerelement ausgewählt ist. 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

Im folgenden Beispiel wird die Überladung [SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) , der die **SelectNodes** -Methode, die nur einen _Startknoten_ -Parameter bereitstellt, auf die erste Zeile in einer wiederholten Tabelle, die an die wiederholte Gruppe gebundenen auswählen verwendet "Mein: Mitarbeiter". 
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

Sie können auch mehrere Zeilen in einer wiederholten Tabelle auswählen. Im folgenden Beispiel wird die ersten drei Zeilen einer wiederholten Tabelle an die wiederholte Gruppe gebunden "Mein: Mitarbeiter" werden mithilfe der Überladung [SelectNodes (XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) , der die **SelectNodes** -Methode, die bietet ausgewählt  _Startknoten_ und _EndNode_ -Parameter: 
  
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


