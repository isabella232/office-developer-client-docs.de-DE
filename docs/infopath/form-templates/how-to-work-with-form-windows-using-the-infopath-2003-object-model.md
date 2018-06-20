---
title: Arbeiten Sie mit Formularfenstern mithilfe des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2003-kompatible Formularvorlagen, Formularfenster, Formular Windows [InfoPath 2007], InfoPath 2003-kompatible Formularvorlagen
localization_priority: Normal
ms.assetid: fbcf3a04-ee0f-40a6-8edd-583ae203e2e1
description: Beim programmgesteuerten arbeiten mit einem InfoPath-Formular, können Sie Code schreiben, um die Fenster des Formulars zuzugreifen, und passen Sie anschließend einige Elemente, die darin enthaltenen. Das InfoPath 2003-kompatible Objektmodell unterstützt den Zugriff auf die Fenster eines Formulars mithilfe der WindowObject-Schnittstelle im Zusammenhang mit der WindowsCollection-Schnittstelle.
ms.openlocfilehash: 4ca0fb53fd8502773d3e770814a5a24c40b2d79f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790762"
---
# <a name="work-with-form-windows-using-the-infopath-2003-object-model"></a>Arbeiten Sie mit Formularfenstern mithilfe des InfoPath 2003-Objektmodells

Beim programmgesteuerten arbeiten mit einem InfoPath-Formular, können Sie Code schreiben, um die Fenster des Formulars zuzugreifen, und passen Sie anschließend einige Elemente, die darin enthaltenen. Das InfoPath 2003-kompatible Objektmodell unterstützt den Zugriff auf die Fenster eines Formulars mithilfe der [WindowObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) -Schnittstelle im Zusammenhang mit der [WindowsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowsCollection.aspx) -Schnittstelle. 
  
In InfoPath gibt es zwei verschiedene Arten von Fenstern:
  
- Das Bearbeitungsfenster, das verwendet wird, wenn ein Benutzer ein Formular ausfüllt.
    
- Das Entwurfsfenster, das verwendet wird, wenn ein Benutzer eine Formularvorlage entwirft.
    
Beim Schreiben von Code in einer Formularvorlage ist es im Bearbeitungsfenster, der die nützlichste Funktionen bereitstellt, da Sie eine **WindowObject** -Instanz verwenden können, die verweist darauf, um den Zugriff auf eine Vielzahl von Eigenschaften und Methoden, mit denen das Formular angepasst werden können Bearbeiten Oberfläche. 
  
## <a name="overview-of-the-windowscollection-interface"></a>Übersicht über die WindowsCollection-Schnittstelle

Die **WindowsCollection** -Schnittstelle bietet die folgenden Eigenschaften, die Vorlage Formularentwickler verwenden können, um die darin enthaltenen **WindowObject** -Instanzen verwalten. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Windows.Count.aspx)-Eigenschaft  <br/> |Gibt die Anzahl der **Window** -Objekte, die in der Auflistung enthalten sind.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Windows.Item.aspx)-Eigenschaft  <br/> |Gibt einen Verweis auf das angegebene **Window** -Objekt zurück.  <br/> **Hinweis**: Visual C#-greift auf Sammlungen mit einem Indexer anstelle die **Item** -Eigenschaft aufrufen. Beispielsweise `thisApplication.Windows[0].Caption`.           |
   
## <a name="overview-of-the-window-object"></a>Übersicht über das Window-Objekt

Die **WindowObject** -Schnittstelle bietet die folgenden Methoden und Eigenschaften, die Formularentwickler für die Interaktion mit einem InfoPath-Fenster verwenden können. Unterstützung für diese Methoden und Eigenschaften unterscheiden sich je nach den Typ des Fensters ( [XdWindowType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowType.aspx) ) mit dem Sie arbeiten. Einige Methoden und Eigenschaften können nur mit den Typ des Fensters Editor (**XdWindowType.xdEditorWindow**). Die verbleibenden Methoden und Eigenschaften arbeiten mit den Typ des Fensters Editor und den Typ des Designers Fensters (**XdWindowType.xdDesignerWindow**). Darüber hinaus kann wie alle InfoPath-Objektmodellmember, beim Aufruf aus einer Formularvorlage Unterstützung für Methoden und Eigenschaften variieren je nach der Sicherheitsstufe und wie das Formular bereitgestellt wird.
  
|**Name**|**Beschreibung**|**Unterstützung von Eigenschaftstypen**|
|:-----|:-----|:-----|
|[Activate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Activate.aspx) -Methode  <br/> |Legt das Fenster als derzeit aktives Fenster fest.   <br/> |Sowohl der **Xddesignwindow-** als auch die **Typ** -Typen  <br/> |
|[Active](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Active.aspx) -Eigenschaft  <br/> |Gibt einen **Boolean** -Wert zurück, der angibt, ob das Fenster das derzeit aktive Fenster ist.  <br/> |Sowohl der **Xddesignwindow-** als auch die **Typ** -Typen  <br/> |
|[Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Caption.aspx) -Eigenschaft  <br/> |Eine Eigenschaft mit Lese-/Schreibzugriff, die zurückgeben oder Festlegen des Titeltextes für das durch das **Window** -Objekt dargestellte Fenster.  <br/> |Nur der **XdEditorWindow** -Typ  <br/> |
|[Close](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Close.aspx)-Methode  <br/> |Schließt ein Fenster.  <br/> |Nur der **XdEditorWindow** -Typ  <br/> |
|[CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.CommandBars.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf die Microsoft Office- **CommandBars** -Objekt zurück.  <br/> |Sowohl der **Xddesignwindow-** als auch die **Typ** -Typen  <br/> |
|[Height](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Height.aspx) -Eigenschaft  <br/> |Eine Eigenschaft Lese-/Schreibzugriff des Typs long Integer, der die Höhe des durch das **Window** -Objekt dargestellten Fensters angibt, gemessen in Punkten.  <br/> |Sowohl der **Xddesignwindow-** als auch die **Typ** -Typen  <br/> |
|[Left](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Left.aspx) -Eigenschaft  <br/> |Eine Eigenschaft Lese-/Schreibzugriff des Typs long Integer, der die horizontale Position des durch das **Window** -Objekt dargestellten Fensters angibt, gemessen in Punkten.  <br/> |Sowohl der **Xddesignwindow-** als auch die **Typ** -Typen  <br/> |
|[MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.MailEnvelope.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf das [MailEnvelopeObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.MailEnvelopeObject.aspx) -Objekt zurück.  <br/> |Nur der **XdEditorWindow** -Typ  <br/> |
|[TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.TaskPanes.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf die [TaskPanesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.TaskPanesCollection.aspx) -Auflistung zurück.  <br/> |Sowohl der **Xddesignwindow-** als auch die **Typ** -Typen  <br/> |
|[Top](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Top.aspx) -Eigenschaft  <br/> |Eine Eigenschaft Lese-/Schreibzugriff des Typs long Integer, der die vertikale Position des durch das **Window** -Objekt dargestellten Fensters angibt, gemessen in Punkten.  <br/> |Sowohl der **Xddesignwindow-** als auch die **Typ** -Typen  <br/> |
|[WindowType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.WindowType.aspx) -Eigenschaft  <br/> |Gibt eine Zahl zurück, die den Typ des Fensters, basierend auf der [XdWindowType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowType.aspx) -Enumeration zurück.  <br/> |Sowohl der **Xddesignwindow-** als auch die **Typ** -Typen  <br/> |
|[Width](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Width.aspx) -Eigenschaft  <br/> |Eine Eigenschaft Lese-/Schreibzugriff des Typs long Integer, der die Breite des durch das **Window** -Objekt dargestellten Fensters angibt, gemessen in Punkten.  <br/> |Sowohl der **Xddesignwindow-** als auch die **Typ** -Typen  <br/> |
|[WindowState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.WindowState.aspx) -Eigenschaft  <br/> |Eine Eigenschaft Lese-/Schreibzugriff des Typs [XdWindowState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowState.aspx) , die den Status des durch das **Window** -Objekt dargestellten Fensters zurückgibt oder festlegt.  <br/> |Sowohl der **Xddesignwindow-** als auch die **Typ** -Typen  <br/> |
|[XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.XDocument.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf das dem Fenster zugeordnete [_XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument.aspx) -Objekt zurück.  <br/> |Nur der **XdEditorWindow** -Typ  <br/> |
   
## <a name="using-the-windowscollection-and-window-interfaces"></a>Verwenden der WindowsCollection- und Window-Schnittstellen

Die **WindowsCollection** -Schnittstelle kann über die [Windows](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Windows.aspx) -Eigenschaft der [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) -Schnittstelle zugegriffen werden. Wenn die **WindowsCollection** -Schnittstelle zum Fenster eines Formulars zuzugreifen, Sie verwenden einen Indexer (Visual c#) oder übergeben Sie eine lange ganze Zahl an die **Item** -Eigenschaft (für Visual Basic), um einen Verweis auf eine Instanz der **WindowObject** -Schnittstelle zurückzugeben. Beispielsweise wird mit dem folgende Code ein Verweis auf die erste in der **WindowsCollection**enthaltenen **WindowObject** .
  
```cs
WindowObject objWindow = thisApplication.Windows[0];
```

```vb
Dim objWindow As WindowObject = thisApplication.Windows(0)
```

Sie können jedoch das derzeit geöffnete Fenster zugreifen, direkt über die [ActiveWindow](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.ActiveWindow.aspx) -Eigenschaft der **Application** -Schnittstelle, ohne Umweg über die ** WindowsCollection **, wie der folgende Code veranschaulicht.
  
```cs
WindowObject objWindow = thisApplication.ActiveWindow;
```

```vb
Dim objWindow As WindowObject = thisApplication.ActiveWindow
```

> [!NOTE]
> Wenn Sie ein Projekt mit verwaltetem Code InfoPath Debuggen, gibt die **ActiveWindow** -Eigenschaft immer **null** zurück, da das Debugfenster aktiv ist. 
  
Ein **WindowObject** kann auch mithilfe der [Window](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx) -Eigenschaft des [View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.aspx) -Schnittstelle, die dem Formular zugrunde liegenden XML-Dokument zugeordnet ist, zugegriffen werden. Die **View** -Eigenschaft des **XDocument** -Schnittstelle wird verwendet, um auf das **View** -Objekt zuzugreifen. Beispielsweise wird mit dem folgende Code ein Verweis auf die **WindowObject** , die Ansicht einem Formular zugrunde liegenden XML-Dokument zugeordnet ist. 
  
```cs
WindowObject objWindow = thisXDocument.View.Window;
```

```vb
Dim objWindow As WindowObject = thisXDocument.View.Window
```

> [!NOTE]
> Einige der Eigenschaften und Methoden des **Window** -Objekts sind nur für Bearbeitungsfenster. Bei Verwendung mit dem Entwerfen geben, sie einen Fehler zurück. In der Tabelle dargestellt, die weiter oben in diesem Thema werden die Eigenschaften und Methoden, die für die einzelnen Fenster unterstützt werden aufgeführt. Sie können die **WindowType** -Eigenschaft in Ihrem Code verwenden, um zu bestimmen, welche Fenster Sie arbeiten. 
  

