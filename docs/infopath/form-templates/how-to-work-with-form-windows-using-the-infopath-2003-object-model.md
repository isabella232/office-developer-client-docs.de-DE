---
title: Arbeiten mit formular Windows Verwenden des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2003-kompatible Formularvorlagen, Formularfenster, Formularfenster [InfoPath 2007], InfoPath 2003-kompatible Formularvorlagen
localization_priority: Normal
ms.assetid: fbcf3a04-ee0f-40a6-8edd-583ae203e2e1
description: Sie können bei der Programmierarbeit mit einem InfoPath-Formular Code schreiben, mit dem auf die Fenster eines Formulars zugegriffen wird, und dann einige der häufig enthaltenen Elemente anpassen. Das InfoPath 2003-kompatible Objektmodell unterstützt den Zugriff auf die Fenster eines Formulars mithilfe der WindowObject-Schnittstelle in Verbindung mit der WindowsCollection-Schnittstelle.
ms.openlocfilehash: f8939fc562cf16c1bce0f6f88bba659e895254f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427577"
---
# <a name="work-with-form-windows-using-the-infopath-2003-object-model"></a>Arbeiten mit formular Windows Verwenden des InfoPath 2003-Objektmodells

Sie können bei der Programmierarbeit mit einem InfoPath-Formular Code schreiben, mit dem auf die Fenster eines Formulars zugegriffen wird, und dann einige der häufig enthaltenen Elemente anpassen. Das InfoPath 2003-kompatible Objektmodell unterstützt den Zugriff auf die Fenster eines Formulars mithilfe der [WindowObject-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) in Verbindung mit der [WindowsCollection-Schnittstelle.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowsCollection.aspx) 
  
In InfoPath gibt es zwei verschiedene Arten von Fenstern:
  
- Das Bearbeitungsfenster, das verwendet wird, wenn ein Benutzer ein Formular ausfüllt.
    
- Das Entwurfsfenster, das verwendet wird, wenn ein Benutzer eine Formularvorlage entwirft.
    
Beim Schreiben von Code in einer Formularvorlage bietet das Bearbeitungsfenster die nützlichste Funktionalität, da Sie hier eine **WindowObject**-Instanz verwenden, die darauf verweist, um auf eine Reihe von Eigenschaften und Methoden zuzugreifen, die zum Anpassen des Konzepts für die Formularbearbeitung verwendet werden kann. 
  
## <a name="overview-of-the-windowscollection-interface"></a>Übersicht über die WindowsCollection-Schnittstelle

Die **WindowsCollection**-Schnittstelle bietet die folgenden Eigenschaften, die Formularvorlagenentwickler zum Verwalten der enthaltenen **WindowObject**-Instanzen verwenden können. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Windows.Count.aspx)-Eigenschaft  <br/> |Gibt die Anzahl der **Window**-Objekte zurück, die in der Auflistung enthalten sind.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Windows.Item.aspx)-Eigenschaft  <br/> |Gibt einen Verweis auf das angegebene **Window**-Objekt zurück.  <br/> **HINWEIS**: Visual C# über einen Indexer auf Auflistungen zu, anstatt die **Item-Eigenschaft auf aufruft.** Zum Beispiel: `thisApplication.Windows[0].Caption`.           |
   
## <a name="overview-of-the-window-object"></a>Übersicht über das Window-Objekt

Die **WindowObject**-Schnittstelle stellt die folgenden Methoden und Eigenschaften bereit, die Formularentwickler für die Interaktion mit einem InfoPath-Fenster verwenden können. Die Unterstützung für diese Methoden und Eigenschaften hängt vom Typ des Fensters ( [XdWindowType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowType.aspx) ) ab, mit dem Sie arbeiten. Einige Methoden und Eigenschaften interagieren nur mit dem Bearbeitungsfenstertyp (**XdWindowType.xdEditorWindow**). Die restlichen Methoden und Eigenschaften können sowohl mit dem Bearbeitungsfenstertyp als auch mit dem Entwurfsfenstertyp (**XdWindowType.xdDesignerWindow**) verwendet werden. Darüber hinaus kann die Unterstützung für Methoden und Eigenschaften wie bei allen InfoPath-Objektmodellmembern je nach der Sicherheitsebene und der Bereitstellungsart des Formulars variieren.
  
|**Name**|**Beschreibung**|**Unterstützung des Fenstertyps**|
|:-----|:-----|:-----|
|[Activate-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Activate.aspx)  <br/> |Legt das Fenster als derzeit aktives Fenster fest.  <br/> |Sowohl der **xdDesignWindow**- als auch der **xdEditorWindow**-Typ  <br/> |
|[Active-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Active.aspx)  <br/> |Gibt einen **Boolean**-Wert zurück, der angibt, ob das Fenster das derzeit aktive Fenster ist.  <br/> |Sowohl **die Typen xdDesignWindow** als **auch xdEditorWindow**  <br/> |
|[Caption-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Caption.aspx)  <br/> |Eine Eigenschaft mit Lese-/Schreibzugriff, die den Beschriftungstext für das durch das **Window**-Objekt dargestellte Fenster zurückgibt oder festlegt.  <br/> |Nur der **xdEditorWindow**-Typ  <br/> |
|[Close](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Close.aspx)-Methode  <br/> |Schließt ein Fenster.  <br/> |Nur der **xdEditorWindow**-Typ  <br/> |
|[CommandBars-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.CommandBars.aspx)  <br/> |Gibt einen Verweis auf das **CommandBars**-Objekt von Microsoft Office zurück.  <br/> |Sowohl **die Typen xdDesignWindow** als **auch xdEditorWindow**  <br/> |
|[Height-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Height.aspx)  <br/> |Eine Eigenschaft mit Lese-/Schreibzugriff des Typs "Lange ganze Zahl", die die Höhe des durch das **Window**-Objekt dargestellten Fensters in Punkt angibt.  <br/> |Sowohl **die Typen xdDesignWindow** als **auch xdEditorWindow**  <br/> |
|[Left-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Left.aspx)  <br/> |Eine Eigenschaft mit Lese-/Schreibzugriff des Typs "Lange ganze Zahl", die die horizontale Position des durch das **Window**-Objekt dargestellten Fensters in Punkt angibt.  <br/> |Sowohl **die Typen xdDesignWindow** als **auch xdEditorWindow**  <br/> |
|[MailEnvelope-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.MailEnvelope.aspx)  <br/> |Gibt einen Verweis auf das [MailEnvelopeObject-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.MailEnvelopeObject.aspx) zurück.  <br/> |Nur der **xdEditorWindow**-Typ  <br/> |
|[TaskPanes-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.TaskPanes.aspx)  <br/> |Gibt einen Verweis auf die [TaskPanesCollection-Auflistung](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.TaskPanesCollection.aspx) zurück.  <br/> |Sowohl **die Typen xdDesignWindow** als **auch xdEditorWindow**  <br/> |
|[Top-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Top.aspx)  <br/> |Eine Eigenschaft mit Lese-/Schreibzugriff des Typs "Lange ganze Zahl", die die vertikale Position des durch das **Window**-Objekt dargestellten Fensters in Punkt angibt.  <br/> |Sowohl **die Typen xdDesignWindow** als **auch xdEditorWindow**  <br/> |
|[WindowType-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.WindowType.aspx)  <br/> |Gibt eine Zahl zurück, die den Typ des Fensters basierend auf der [XdWindowType-Aufzählung](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowType.aspx) angibt.  <br/> |Sowohl **die Typen xdDesignWindow** als **auch xdEditorWindow**  <br/> |
|[Width-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Width.aspx)  <br/> |Eine Eigenschaft mit Lese-/Schreibzugriff des Typs "Lange ganze Zahl", die die Breite des durch das **Window**-Objekt dargestellten Fensters in Punkt angibt.  <br/> |Sowohl **die Typen xdDesignWindow** als **auch xdEditorWindow**  <br/> |
|[WindowState-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.WindowState.aspx)  <br/> |Eine Lese-/Schreibeigenschaft vom Typ [XdWindowState,](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowState.aspx) die den Status des Fensters zurückgibt oder legt diesen fest, der durch das **Window-Objekt dargestellt** wird.  <br/> |Sowohl **die Typen xdDesignWindow** als **auch xdEditorWindow**  <br/> |
|[XDocument-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.XDocument.aspx)  <br/> |Gibt einen Verweis auf das [_XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument.aspx) dem Fenster zugeordneten Objekt zurück.  <br/> |Nur der **xdEditorWindow**-Typ  <br/> |
   
## <a name="using-the-windowscollection-and-window-interfaces"></a>Verwenden der WindowsCollection- und Window-Schnittstellen

Auf **die WindowsCollection-Schnittstelle** kann über die [Windows](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Windows.aspx) der [Application-Schnittstelle zugegriffen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) werden. Wenn Sie die **WindowsCollection**-Schnittstelle für den Zugriff auf das Fenster eines Formulars verwenden, verwenden Sie entweder eine Indexerstellung (Visual C#) oder übergeben eine lange ganze Zahl an die **Item**-Eigenschaft (Visual Basic), um einen Verweis auf eine **WindowObject**-Schnittstelleninstanz zurückzugeben. Durch den folgenden Code wird beispielsweise ein Verweis auf das erste **WindowObject** festgelegt, das in der **WindowsCollection** enthalten ist.
  
```cs
WindowObject objWindow = thisApplication.Windows[0];
```

```vb
Dim objWindow As WindowObject = thisApplication.Windows(0)
```

Sie können jedoch direkt über die [ActiveWindow-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.ActiveWindow.aspx) der **Application-Schnittstelle** auf das derzeit geöffnete Fenster zugreifen, ohne die ** WindowsCollection **, wie der folgende Code veranschaulicht, zu durch gehen.
  
```cs
WindowObject objWindow = thisApplication.ActiveWindow;
```

```vb
Dim objWindow As WindowObject = thisApplication.ActiveWindow
```

> [!NOTE]
> Beim Debuggen eines InfoPath-Projekts mit verwaltetem Code gibt die **ActiveWindow**-Eigenschaft immer **null** zurück, da das Debugfenster aktiv ist. 
  
Auf **ein WindowObject** kann auch über die [Window-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx) der [View-Schnittstelle](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.aspx) zugegriffen werden, die dem dem Formular zugrunde liegenden XML-Dokument zugeordnet ist. Die **View**-Eigenschaft der **XDocument**-Schnittstelle wird zum Zugreifen auf das **View**-Objekt verwendet. Durch den folgenden Code wird beispielsweise ein Verweis auf das **WindowObject** festgelegt, das der Ansicht des zugrunde liegenden XML-Dokuments eines Formulars zugeordnet ist. 
  
```cs
WindowObject objWindow = thisXDocument.View.Window;
```

```vb
Dim objWindow As WindowObject = thisXDocument.View.Window
```

> [!NOTE]
> Einige Eigenschaften und Methoden des **Window**-Objekts sind nur für den Bearbeitungsfenstertyp verfügbar. Wenn Sie mit dem Entwurfsfenstertyp verwendet werden, wird ein Fehler zurückgegeben. Die für jeden Fenstertyp unterstützten Eigenschaften und Methoden sind in der in diesem Thema bereits dargestellten Tabelle aufgelistet. Sie können die **WindowType**-Eigenschaft im Code verwenden, um zu bestimmen, mit welchem Fenstertyp Sie arbeiten. 
  

