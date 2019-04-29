---
title: Arbeiten mit Ansichten mithilfe des InfoPath-Objektmodells 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2003-kompatible Formularvorlagen, Ansichten, Ansichten [InfoPath 2007], InfoPath 2003-kompatible Formularvorlagen
localization_priority: Normal
ms.assetid: feb1bfcb-1cb1-4d5c-bc84-df86a33a5934
description: Bei der Arbeit mit einer InfoPath-Formularvorlage können Sie Code schreiben, um auf die Ansichten des Formulars zuzugreifen, und dann eine Vielzahl von Aktionen für die in den Ansichten enthaltenen Daten ausführen. Das InfoPath 2003-kompatible Objektmodell unterstützt den Zugriff auf die Ansichten eines Formulars, indem die Elemente der ViewObject-Schnittstelle verwendet werden.
ms.openlocfilehash: 6a2dd408ba51e5c8394120944e0c28897e768738
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411883"
---
# <a name="work-with-views-using-the-infopath-2003-object-model"></a>Arbeiten mit Ansichten mithilfe des InfoPath-Objektmodells 2003

Bei der Arbeit mit einer InfoPath-Formularvorlage können Sie Code schreiben, um auf die Ansichten des Formulars zuzugreifen, und dann eine Vielzahl von Aktionen für die in den Ansichten enthaltenen Daten ausführen. Das InfoPath 2003-kompatible Objektmodell unterstützt den Zugriff auf die Ansichten eines Formulars, indem die Elemente der [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) -Schnittstelle verwendet werden. 
  
## <a name="overview-of-the-viewobject-interface"></a>Übersicht über die ViewObject-Schnittstelle

Die [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) -Schnittstelle stellt die folgenden Methoden und Eigenschaften bereit, die Formularentwickler für die Interaktion mit einer InfoPath-Ansicht verwenden können. 
  
> [!NOTE]
> Die Methoden und Eigenschaften der [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) -Schnittstelle stehen während des onlade-Ereignisses nicht zur Verfügung. [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.DisableAutoUpdate.aspx) -Methode  <br/> |Deaktiviert die Synchronisierung von XML-DOM (Document Object Model) und der Ansicht.  <br/> |
|[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.EnableAutoUpdate.aspx) -Methode  <br/> |Aktiviert die Synchronisierung von XML-DOM und der Ansicht.  <br/> |
|[Execute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ExecuteAction.aspx) -Methode  <br/> |Führt eine Bearbeitungsaktion von InfoPath aus.  <br/> |
|[Export](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Export.aspx) -Methode  <br/> |Exportiert die Ansicht als Datei des angegebenen Formats.  <br/> |
|[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ForceUpdate.aspx) -Methode  <br/> |Synchronisiert XML-DOM mit der Ansicht.  <br/> |
|[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetContextNodes.aspx) GetContextNodes-Methode  <br/> |Gibt einen Verweis auf die [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLNodesCollection.aspx) XMLNodes-Schnittstelle zurück, basierend auf dem angegebenen XML-Knoten und Ansichtskontext oder in der aktuellen Auswahl in der Ansicht.  <br/> |
|[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetSelectedNodes.aspx) -Methode  <br/> |Gibt einen Verweis auf die **XMLNodesCollection**-Schnittstelle auf Grundlage der aktuellen Auswahl in der Ansicht zurück.  <br/> |
|[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectNodes.aspx) -Methode  <br/> |Wählt einen Bereich mit XML-Knoten in der Ansicht aus.  <br/> |
|[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectText.aspx) -Methode  <br/> |Wählt den im in der Ansicht enthaltenen angegebenen XML-Knoten aus.  <br/> |
|[SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SwitchView.aspx) -Methode  <br/> |Wechselt von einem InfoPath-Formular zur angegebenen Ansicht.  <br/> |
|[Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Name.aspx)-Eigenschaft  <br/> |Gibt einen Zeichenfolgenwert zurück, der den Namen der aktuellen Ansicht angibt.  <br/> |
|[Window](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf die [WindowObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) -Schnittstelle zurück, die auf das der Ansicht zugeordnete **Fenster** zugreift.  <br/> |
   
> [!NOTE]
> Das InfoPath 2003-kompatible Objektmodell stellt außerdem die [ViewInfosCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfosCollection.aspx) -Schnittstelle bereit, die zum Abrufen von Informationen zu allen in einem Formular implementierten Ansichten verwendet werden kann. 
  
## <a name="using-the-viewobject-interface"></a>Verwenden der ViewObject-Schnittstelle

Der [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) Zugriff auf die ViewObject-Schnittstelle erfolgt über die [View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx) -Eigenschaft der [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Schnittstelle `thisXDocument` (auf die über die Variable `_Startup` zugegriffen wird, die in der Methode der Formularcodeklasse initialisiert wird). Im folgenden Codebeispiel wird veranschaulicht, wie die [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) -Methode der [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Schnittstelle verwendet wird, um ein Meldungsfeld mit dem Namen der aktuellen Ansicht anzuzeigen, die dem einem Formular zuGRUNDE liegenden XML-Dokument zugeordnet ist. 
  
```cs
thisXDocument.UI.Alert("Current view name: " + 
   thisXDocument.View.Name);
```

```vb
thisXDocument.UI.Alert("Current view name: " &amp; _
   thisXDocument.View.Name)
```

Alle InfoPath-Formulare enthalten mindestens eine Standardansicht; InfoPath unterstützt jedoch auch das Erstellen mehrerer Ansichten des einem Formular zugrunde liegenden XML-Dokuments. Wenn Sie in einem Formular über mehrere Ansichten verfügen, kann das **View** -Objekt verwendet werden, um mit der aktuell aktiven Ansicht zu arbeiten. Sie können die derzeit aktive Ansicht programmgesteuert ändern, indem Sie die **SwitchView** -Methode des **View** -Objekts verwenden, wie im folgenden Codebeispiel veranschaulicht. 
  
```cs
thisXDocument.View.SwitchView("MySecondView");
```

```vb
thisXDocument.View.SwitchView("MySecondView")
```

Das obige Beispiel für das Wechseln einer Ansicht funktioniert nur nach dem Öffnen des Formulars. Verwenden Sie zum Festlegen einer Standardansicht **** während des onladen-Ereignisses die IsDefault-Eigenschaft der [ViewInfoObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfoObject.aspx) -Schnittstelle, wie im folgenden Beispiel dargestellt. [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.IsDefault.aspx) 
  
```cs
thisXDocument.ViewInfos["MyDefaultView"].IsDefault = true;
```

```vb
thisXDocument.ViewInfos("MyDefaultView").IsDefault = True
```


