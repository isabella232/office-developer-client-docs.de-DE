---
title: Arbeiten Sie mit Ansichten mithilfe des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2003-kompatible Formularvorlagen, Ansichten, Ansichten [InfoPath 2007], InfoPath 2003-kompatible Formularvorlagen
localization_priority: Normal
ms.assetid: feb1bfcb-1cb1-4d5c-bc84-df86a33a5934
description: Bei der Arbeit mit InfoPath-Formularvorlage können Sie Code schreiben, um die Ansichten des Formulars zuzugreifen, und klicken Sie dann auf die Daten, die die Ansichten enthalten eine Vielzahl von Aktionen ausführen. Das InfoPath 2003-kompatible Objektmodell unterstützt den Zugriff auf die Ansichten eines Formulars durch Verwendung der Member der ViewObject-Schnittstelle.
ms.openlocfilehash: 1cbc472993ff18b26f31e3bc28b12a75e559644a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790753"
---
# <a name="work-with-views-using-the-infopath-2003-object-model"></a>Arbeiten Sie mit Ansichten mithilfe des InfoPath 2003-Objektmodells

Bei der Arbeit mit InfoPath-Formularvorlage können Sie Code schreiben, um die Ansichten des Formulars zuzugreifen, und klicken Sie dann auf die Daten, die die Ansichten enthalten eine Vielzahl von Aktionen ausführen. Das InfoPath 2003-kompatible Objektmodell unterstützt den Zugriff auf die Ansichten eines Formulars durch Verwendung der Member der [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) -Schnittstelle. 
  
## <a name="overview-of-the-viewobject-interface"></a>Übersicht über die ViewObject-Schnittstelle

Die [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) -Schnittstelle bietet die folgenden Methoden und Eigenschaften, die Formularentwickler für die Interaktion mit einer InfoPath-Ansicht verwenden können. 
  
> [!NOTE]
> Die Methoden und Eigenschaften der [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) -Schnittstelle sind während des [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) -Ereignisses nicht verfügbar. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.DisableAutoUpdate.aspx) -Methode  <br/> |Deaktiviert die Synchronisierung von XML-DOM (Document Object Model) und der Ansicht.  <br/> |
|[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.EnableAutoUpdate.aspx) -Methode  <br/> |Aktiviert die Synchronisierung von XML-DOM und der Ansicht.  <br/> |
|[ExecuteAction](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ExecuteAction.aspx) -Methode  <br/> |Führt eine Bearbeitungsaktion von InfoPath aus.  <br/> |
|[Export](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Export.aspx) -Methode  <br/> |Exportiert die Ansicht als Datei des angegebenen Formats.  <br/> |
|[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ForceUpdate.aspx) -Methode  <br/> |Synchronisiert XML-DOM mit der Ansicht.  <br/> |
|[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetContextNodes.aspx) -Methode  <br/> |Gibt einen Verweis auf die [XMLNodesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLNodesCollection.aspx) -Schnittstelle, basierend auf der angegebenen XML-Knoten und dem Ansichtskontext oder auf der aktuellen Auswahl in der Ansicht zurück.  <br/> |
|[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetSelectedNodes.aspx) -Methode  <br/> |Gibt einen Verweis auf die **XMLNodesCollection** -Schnittstelle, basierend auf der aktuellen Auswahl in der Ansicht zurück.  <br/> |
|[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectNodes.aspx) -Methode  <br/> |Wählt einen Bereich mit XML-Knoten in der Ansicht aus.  <br/> |
|[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectText.aspx) -Methode  <br/> |Wählt den im in der Ansicht enthaltenen angegebenen XML-Knoten aus.  <br/> |
|[SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SwitchView.aspx) -Methode  <br/> |Wechselt von einem InfoPath-Formular zur angegebenen Ansicht.   <br/> |
|[Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Name.aspx)-Eigenschaft  <br/> |Gibt einen Zeichenfolgenwert zurück, der den Namen der aktuellen Ansicht angibt.  <br/> |
|[Window](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf die [WindowObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) -Schnittstelle die greift auf das **Fenster** , das der Ansicht zugeordnet.  <br/> |
   
> [!NOTE]
> Das InfoPath 2003-kompatible Objektmodell stellt auch die [ViewInfosCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfosCollection.aspx) -Schnittstelle, die zum Abrufen von Informationen zu allen in einem Formular implementierten Ansichten verwendet werden kann. 
  
## <a name="using-the-viewobject-interface"></a>Verwenden der ViewObject-Schnittstelle

Die [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) -Schnittstelle erfolgt über die [View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx) -Eigenschaft des [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) -Schnittstelle (die erfolgt über die `thisXDocument` Variable, die in initialisiert wird die `_Startup` -Methode des Form-Codeklasse). Im folgenden Codebeispiel wird beispielsweise veranschaulicht, wie die [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) -Methode des [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Schnittstelle verwenden, um ein Meldungsfeld mit dem Namen der aktuellen Ansicht anzuzeigen, die einem Formular zugrunde liegenden XML-Dokument zugeordnet ist. 
  
```cs
thisXDocument.UI.Alert("Current view name: " + 
   thisXDocument.View.Name);
```

```vb
thisXDocument.UI.Alert("Current view name: " &amp; _
   thisXDocument.View.Name)
```

Alle InfoPath-Formulare enthalten mindestens eine Standardansicht. InfoPath unterstützt jedoch auch die Erstellung mehrerer Ansichten des einem Formular zugrunde liegenden XML-Dokument. Wenn Sie mehrere Ansichten in einem Formular hat, kann das **View** -Objekt der Ansicht entwickelt, die derzeit aktive verwendet werden. Sie können die Ansicht, die derzeit aktive wird mithilfe der **SwitchView** -Methode des **View** -Objekts, wie im folgenden Codebeispiel wird veranschaulicht, programmgesteuert ändern. 
  
```cs
thisXDocument.View.SwitchView("MySecondView");
```

```vb
thisXDocument.View.SwitchView("MySecondView")
```

Im vorherige Beispiel für den Wechsel von einer Ansicht funktioniert nur, wenn das Formular geöffnet wird. Verwenden Sie die [IsDefault](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.IsDefault.aspx) -Eigenschaft der [ViewInfoObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfoObject.aspx) -Schnittstelle, um eine Standardansicht während das **OnLoad** -Ereignis festzulegen, wie im folgenden Beispiel dargestellt. 
  
```cs
thisXDocument.ViewInfos["MyDefaultView"].IsDefault = true;
```

```vb
thisXDocument.ViewInfos("MyDefaultView").IsDefault = True
```


