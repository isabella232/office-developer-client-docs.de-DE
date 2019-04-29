---
title: Arbeiten mit Formularfenstern mithilfe des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2003-kompatible Formularvorlagen, Formularfenster, Formularfenster [InfoPath 2007], InfoPath 2003-kompatible Formularvorlagen
localization_priority: Normal
ms.assetid: fbcf3a04-ee0f-40a6-8edd-583ae203e2e1
description: Sie können bei der Programmierarbeit mit einem InfoPath-Formular Code schreiben, mit dem auf die Fenster eines Formulars zugegriffen wird, und dann einige der häufig enthaltenen Elemente anpassen. Das InfoPath 2003-kompatible Objektmodell unterstützt den Zugriff auf die Fenster eines Formulars, indem die WindowObject-Schnittstelle in Verbindung mit der WindowsCollection-Schnittstelle verwendet wird.
ms.openlocfilehash: f8939fc562cf16c1bce0f6f88bba659e895254f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427577"
---
# <a name="work-with-form-windows-using-the-infopath-2003-object-model"></a>Arbeiten mit Formularfenstern mithilfe des InfoPath 2003-Objektmodells

Sie können bei der Programmierarbeit mit einem InfoPath-Formular Code schreiben, mit dem auf die Fenster eines Formulars zugegriffen wird, und dann einige der häufig enthaltenen Elemente anpassen. Das InfoPath 2003-kompatible Objektmodell unterstützt den Zugriff auf die Fenster eines Formulars, indem die [WindowObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) -Schnittstelle in Verbindung [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowsCollection.aspx) mit der WindowsCollection-Schnittstelle verwendet wird. 
  
In InfoPath gibt es zwei verschiedene Arten von Fenstern:
  
- Das Bearbeitungsfenster, das verwendet wird, wenn ein Benutzer ein Formular ausfüllt.
    
- Das Entwurfsfenster, das verwendet wird, wenn ein Benutzer eine Formularvorlage entwirft.
    
Beim Schreiben von Code in einer Formularvorlage bietet das Bearbeitungsfenster die nützlichste Funktionalität, da Sie hier eine **WindowObject**-Instanz verwenden, die darauf verweist, um auf eine Reihe von Eigenschaften und Methoden zuzugreifen, die zum Anpassen des Konzepts für die Formularbearbeitung verwendet werden kann. 
  
## <a name="overview-of-the-windowscollection-interface"></a>Übersicht über die WindowsCollection-Schnittstelle

Die **WindowsCollection**-Schnittstelle bietet die folgenden Eigenschaften, die Formularvorlagenentwickler zum Verwalten der enthaltenen **WindowObject**-Instanzen verwenden können. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Windows.Count.aspx)-Eigenschaft  <br/> |Gibt die Anzahl der **Window**-Objekte zurück, die in der Auflistung enthalten sind.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Windows.Item.aspx)-Eigenschaft  <br/> |Gibt einen Verweis auf das angegebene **Window**-Objekt zurück.  <br/> **Hinweis**: Visual C# greift auf Auflistungen mithilfe eines Indexers zu, statt die **Item** -Eigenschaft aufzurufen. Zum Beispiel: `thisApplication.Windows[0].Caption`.           |
   
## <a name="overview-of-the-window-object"></a>Übersicht über das Window-Objekt

Die **WindowObject**-Schnittstelle stellt die folgenden Methoden und Eigenschaften bereit, die Formularentwickler für die Interaktion mit einem InfoPath-Fenster verwenden können. Die Unterstützung für diese Methoden und Eigenschaften hängt vom Typ des Fensters ( [XdWindowType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowType.aspx) ) ab, mit dem Sie arbeiten. Einige Methoden und Eigenschaften interagieren nur mit dem Bearbeitungsfenstertyp (**XdWindowType.xdEditorWindow**). Die restlichen Methoden und Eigenschaften können sowohl mit dem Bearbeitungsfenstertyp als auch mit dem Entwurfsfenstertyp (**XdWindowType.xdDesignerWindow**) verwendet werden. Darüber hinaus kann die Unterstützung für Methoden und Eigenschaften wie bei allen InfoPath-Objektmodellmembern je nach der Sicherheitsebene und der Bereitstellungsart des Formulars variieren.
  
|**Name**|**Beschreibung**|**Unterstützung des Fenstertyps**|
|:-----|:-----|:-----|
|[Activate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Activate.aspx) -Methode  <br/> |Legt das Fenster als derzeit aktives Fenster fest.  <br/> |Sowohl der **xdDesignWindow**- als auch der **xdEditorWindow**-Typ  <br/> |
|[Active](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Active.aspx) -Eigenschaft  <br/> |Gibt einen **Boolean**-Wert zurück, der angibt, ob das Fenster das derzeit aktive Fenster ist.  <br/> |Sowohl die **xdDesignWindow** -als auch die **xdEditorWindow** -Typen  <br/> |
|[Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Caption.aspx) -Eigenschaft  <br/> |Eine Eigenschaft mit Lese-/Schreibzugriff, die den Beschriftungstext für das durch das **Window**-Objekt dargestellte Fenster zurückgibt oder festlegt.  <br/> |Nur der **xdEditorWindow**-Typ  <br/> |
|[Close](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Close.aspx)-Methode  <br/> |Schließt ein Fenster.  <br/> |Nur der **xdEditorWindow**-Typ  <br/> |
|[CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.CommandBars.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf das **CommandBars**-Objekt von Microsoft Office zurück.  <br/> |Sowohl die **xdDesignWindow** -als auch die **xdEditorWindow** -Typen  <br/> |
|[Height](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Height.aspx) -Eigenschaft  <br/> |Eine Eigenschaft mit Lese-/Schreibzugriff des Typs "Lange ganze Zahl", die die Höhe des durch das **Window**-Objekt dargestellten Fensters in Punkt angibt.  <br/> |Sowohl die **xdDesignWindow** -als auch die **xdEditorWindow** -Typen  <br/> |
|[Left](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Left.aspx) -Eigenschaft  <br/> |Eine Eigenschaft mit Lese-/Schreibzugriff des Typs "Lange ganze Zahl", die die horizontale Position des durch das **Window**-Objekt dargestellten Fensters in Punkt angibt.  <br/> |Sowohl die **xdDesignWindow** -als auch die **xdEditorWindow** -Typen  <br/> |
|[MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.MailEnvelope.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf das [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.MailEnvelopeObject.aspx) MailEnvelopeObject-Objekt zurück.  <br/> |Nur der **xdEditorWindow**-Typ  <br/> |
|[TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.TaskPanes.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf die [TaskPanesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.TaskPanesCollection.aspx) -Auflistung zurück.  <br/> |Sowohl die **xdDesignWindow** -als auch die **xdEditorWindow** -Typen  <br/> |
|[Top](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Top.aspx) -Eigenschaft  <br/> |Eine Eigenschaft mit Lese-/Schreibzugriff des Typs "Lange ganze Zahl", die die vertikale Position des durch das **Window**-Objekt dargestellten Fensters in Punkt angibt.  <br/> |Sowohl die **xdDesignWindow** -als auch die **xdEditorWindow** -Typen  <br/> |
|[WindowType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.WindowType.aspx) -Eigenschaft  <br/> |Gibt eine Zahl zurück, die den Typ des Fensters angibt, basierend auf der [XdWindowType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowType.aspx) -Aufzählung.  <br/> |Sowohl die **xdDesignWindow** -als auch die **xdEditorWindow** -Typen  <br/> |
|[Width](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Width.aspx) -Eigenschaft  <br/> |Eine Eigenschaft mit Lese-/Schreibzugriff des Typs "Lange ganze Zahl", die die Breite des durch das **Window**-Objekt dargestellten Fensters in Punkt angibt.  <br/> |Sowohl die **xdDesignWindow** -als auch die **xdEditorWindow** -Typen  <br/> |
|[WindowState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.WindowState.aspx) -Eigenschaft  <br/> |Eine Eigenschaft mit Lese-/Schreibzugriff vom Typ [XdWindowState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowState.aspx) , die den Zustand des durch das **Window** -Objekt dargestellten Fensters zurückgibt oder festlegt.  <br/> |Sowohl die **xdDesignWindow** -als auch die **xdEditorWindow** -Typen  <br/> |
|[XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.XDocument.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf das [_XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument.aspx) -Objekt zurück, das dem Fenster zugeordnet ist.  <br/> |Nur der **xdEditorWindow**-Typ  <br/> |
   
## <a name="using-the-windowscollection-and-window-interfaces"></a>Verwenden der WindowsCollection- und Window-Schnittstellen

Auf **** die WindowsCollection-Schnittstelle kann über die [Windows](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Windows.aspx) -Eigenschaft der [Anwendungs](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) Schnittstelle zugegriffen werden. Wenn Sie die **WindowsCollection**-Schnittstelle für den Zugriff auf das Fenster eines Formulars verwenden, verwenden Sie entweder eine Indexerstellung (Visual C#) oder übergeben eine lange ganze Zahl an die **Item**-Eigenschaft (Visual Basic), um einen Verweis auf eine **WindowObject**-Schnittstelleninstanz zurückzugeben. Durch den folgenden Code wird beispielsweise ein Verweis auf das erste **WindowObject** festgelegt, das in der **WindowsCollection** enthalten ist.
  
```cs
WindowObject objWindow = thisApplication.Windows[0];
```

```vb
Dim objWindow As WindowObject = thisApplication.Windows(0)
```

Sie können jedoch direkt auf das derzeit geöffnete Fenster zugreifen, indem Sie die [ActiveWindow](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.ActiveWindow.aspx) -Eigenschaft der **Anwendungs** Schnittstelle verwenden, ohne die * * WindowsCollection * *, wie im folgenden Code veranschaulicht.
  
```cs
WindowObject objWindow = thisApplication.ActiveWindow;
```

```vb
Dim objWindow As WindowObject = thisApplication.ActiveWindow
```

> [!NOTE]
> Beim Debuggen eines InfoPath-Projekts mit verwaltetem Code gibt die **ActiveWindow**-Eigenschaft immer **null** zurück, da das Debugfenster aktiv ist. 
  
Auf eine **WindowObject** kann auch über die [Window](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx) -Eigenschaft der [View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.aspx) -Schnittstelle zugegriffen werden, die dem dem Formular zugrunde liegenden XML-Dokument zugeordnet ist. Die **View**-Eigenschaft der **XDocument**-Schnittstelle wird zum Zugreifen auf das **View**-Objekt verwendet. Durch den folgenden Code wird beispielsweise ein Verweis auf das **WindowObject** festgelegt, das der Ansicht des zugrunde liegenden XML-Dokuments eines Formulars zugeordnet ist. 
  
```cs
WindowObject objWindow = thisXDocument.View.Window;
```

```vb
Dim objWindow As WindowObject = thisXDocument.View.Window
```

> [!NOTE]
> Einige der Eigenschaften und Methoden des **Window** -Objekts sind nur für den Bearbeitungsfenstertyp; Wenn Sie mit dem Entwurfs Fenstertyp verwendet wird, wird ein Fehler zurückgegeben. Die Eigenschaften und Methoden, die für jeden Fenstertyp unterstützt werden, werden in der Tabelle weiter oben in diesem Thema aufgeführt. Sie können die **WindowType** -Eigenschaft im Code verwenden, um zu bestimmen, mit welchem Fenstertyp Sie arbeiten. 
  

