---
title: Arbeiten mit Ansichten mithilfe des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2003-kompatible Formularvorlagen, Ansichten,Ansichten [InfoPath 2007], InfoPath 2003-kompatible Formularvorlagen
localization_priority: Normal
ms.assetid: feb1bfcb-1cb1-4d5c-bc84-df86a33a5934
description: Bei der Arbeit mit einer InfoPath-Formularvorlage können Sie Code schreiben, um auf die Ansichten des Formulars zuzugreifen, und dann eine Vielzahl von Aktionen für die in den Ansichten enthaltenen Daten ausführen. Das InfoPath 2003-kompatible Objektmodell unterstützt den Zugriff auf die Ansichten eines Formulars mithilfe der Elemente der ViewObject-Schnittstelle.
ms.openlocfilehash: 6a2dd408ba51e5c8394120944e0c28897e768738
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411883"
---
# <a name="work-with-views-using-the-infopath-2003-object-model"></a>Arbeiten mit Ansichten mithilfe des InfoPath 2003-Objektmodells

Bei der Arbeit mit einer InfoPath-Formularvorlage können Sie Code schreiben, um auf die Ansichten des Formulars zuzugreifen, und dann eine Vielzahl von Aktionen für die in den Ansichten enthaltenen Daten ausführen. Das InfoPath 2003-kompatible Objektmodell unterstützt den Zugriff auf die Ansichten eines Formulars mithilfe der Elemente der [ViewObject-Schnittstelle.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) 
  
## <a name="overview-of-the-viewobject-interface"></a>Übersicht über die ViewObject-Schnittstelle

Die [ViewObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) bietet die folgenden Methoden und Eigenschaften, mit denen Formularentwickler mit einer InfoPath-Ansicht interagieren können. 
  
> [!NOTE]
> Die Methoden und Eigenschaften der [ViewObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) sind während des [OnLoad-Ereignisses nicht](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) verfügbar. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[DisableAutoUpdate-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.DisableAutoUpdate.aspx)  <br/> |Deaktiviert die Synchronisierung von XML-DOM (Document Object Model) und der Ansicht.  <br/> |
|[EnableAutoUpdate-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.EnableAutoUpdate.aspx)  <br/> |Aktiviert die Synchronisierung von XML-DOM und der Ansicht.  <br/> |
|[ExecuteAction-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ExecuteAction.aspx)  <br/> |Führt eine Bearbeitungsaktion von InfoPath aus.  <br/> |
|[Exportmethode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Export.aspx)  <br/> |Exportiert die Ansicht als Datei des angegebenen Formats.  <br/> |
|[ForceUpdate-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ForceUpdate.aspx)  <br/> |Synchronisiert XML-DOM mit der Ansicht.  <br/> |
|[GetContextNodes-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetContextNodes.aspx)  <br/> |Gibt einen Verweis auf die [XMLNodesCollection-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLNodesCollection.aspx) zurück, basierend auf dem angegebenen XML-Knoten und Ansichtskontext oder auf der aktuellen Auswahl in der Ansicht.  <br/> |
|[GetSelectedNodes-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetSelectedNodes.aspx)  <br/> |Gibt einen Verweis auf die **XMLNodesCollection**-Schnittstelle auf Grundlage der aktuellen Auswahl in der Ansicht zurück.  <br/> |
|[SelectNodes-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectNodes.aspx)  <br/> |Wählt einen Bereich mit XML-Knoten in der Ansicht aus.  <br/> |
|[SelectText-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectText.aspx)  <br/> |Wählt den im in der Ansicht enthaltenen angegebenen XML-Knoten aus.  <br/> |
|[SwitchView-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SwitchView.aspx)  <br/> |Wechselt von einem InfoPath-Formular zur angegebenen Ansicht.  <br/> |
|[Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Name.aspx)-Eigenschaft  <br/> |Gibt einen Zeichenfolgenwert zurück, der den Namen der aktuellen Ansicht angibt.  <br/> |
|[Window-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx)  <br/> |Gibt einen Verweis auf die [WindowObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) zurück, die **auf das der Ansicht** zugeordnete Fenster zutritt.  <br/> |
   
> [!NOTE]
> Das InfoPath 2003-kompatible Objektmodell stellt auch die [ViewInfosCollection-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfosCollection.aspx) bereit, die zum Abrufen von Informationen zu allen in einem Formular implementierten Ansichten verwendet werden kann. 
  
## <a name="using-the-viewobject-interface"></a>Verwenden der ViewObject-Schnittstelle

Auf [die ViewObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) wird über die [View-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx) der [XDocument-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) zugegriffen (auf die über die Variable zugegriffen wird, die in der Methode der Formularcodeklasse initialisiert  `thisXDocument`  `_Startup` wird). Im folgenden Codebeispiel wird beispielsweise veranschaulicht, wie Sie mithilfe der [Alert-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) der [UIObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) ein Meldungsfeld mit dem Namen der aktuellen Ansicht anzeigen, die dem einem Formular zugrunde liegenden XML-Dokument zugeordnet ist. 
  
```cs
thisXDocument.UI.Alert("Current view name: " + 
   thisXDocument.View.Name);
```

```vb
thisXDocument.UI.Alert("Current view name: " &amp; _
   thisXDocument.View.Name)
```

Alle InfoPath-Formulare enthalten mindestens eine Standardansicht. InfoPath unterstützt dennoch das Erstellen mehrerer Ansichten des zugrunde liegenden XML-Dokuments eines Formulars. Wenn in einem Formular mehrere Ansichten vorhanden sind, kann das **View**-Objekt zur Interaktion mit der aktuell aktiven Ansicht verwendet werden. Sie können die aktuell aktive Ansicht programmgesteuert ändern, indem Sie die **SwitchView**-Methode des **View**-Objekts verwenden, wie im folgenden Codebeispiel dargestellt. 
  
```cs
thisXDocument.View.SwitchView("MySecondView");
```

```vb
thisXDocument.View.SwitchView("MySecondView")
```

Das obige Beispiel für das Wechseln einer Ansicht funktioniert nur nach dem Öffnen des Formulars. Verwenden Sie zum Festlegen einer Standardansicht während des **OnLoad-Ereignisses** die [IsDefault-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.IsDefault.aspx) der [ViewInfoObject-Schnittstelle,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfoObject.aspx) wie im folgenden Beispiel gezeigt. 
  
```cs
thisXDocument.ViewInfos["MyDefaultView"].IsDefault = true;
```

```vb
thisXDocument.ViewInfos("MyDefaultView").IsDefault = True
```


