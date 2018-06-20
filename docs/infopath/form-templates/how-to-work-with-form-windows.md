---
title: Arbeiten mit Formularfenstern
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- Windowscollection [Infopath 2007] Formularfenster [InfoPath 2007], Window-Klasse [InfoPath 2007]
localization_priority: Normal
ms.assetid: 32ae2427-882b-45f8-8754-0e8c27fc23ba
description: Beim programmgesteuerten arbeiten mit einem InfoPath-Formular, können Sie Code schreiben, um die Fenster des Formulars zuzugreifen, und passen Sie anschließend einige Elemente, die darin enthaltenen. Das InfoPath-Objektmodell zur Verfügung gestellt, durch die Microsoft.Office.InfoPath-Namespace unterstützt den Zugriff auf die Fenster eines Formulars mithilfe der Window-Klasse in Verbindung mit der WindowCollection-Klasse.
ms.openlocfilehash: 5b24798e92849a2d79bf836e12dd91845ee58942
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790764"
---
# <a name="work-with-form-windows"></a>Arbeiten mit Formularfenstern

Beim programmgesteuerten arbeiten mit einem InfoPath-Formular, können Sie Code schreiben, um die Fenster des Formulars zuzugreifen, und passen Sie anschließend einige Elemente, die darin enthaltenen. Das InfoPath-Objektmodell zur Verfügung gestellt, durch die [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace unterstützt den Zugriff auf die Fenster eines Formulars mithilfe der [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Klasse in Verbindung mit der [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) -Klasse. 
  
> [!NOTE]
> Die Klassen für die Arbeit mit einem Formular zugrunde Windows stehen nur beim Arbeiten mit einer **InfoPath-Editor-Formular**. Wenn eine Formularvorlage **Kompatibilität** Einstellung **Webbrowserformular**ist, sind diese Klassen nicht verfügbar. 
  
In InfoPath gibt es zwei Fenstertypen:  
  
- Das Bearbeitungsfenster, das verwendet wird, wenn ein Benutzer ein Formular ausfüllt.
    
- Das Entwurfsfenster, das verwendet wird, wenn ein Benutzer eine Formularvorlage entwirft.
    
Beim Schreiben von Code in einer Formularvorlage ist es im Bearbeitungsfenster, die die nützlichste Funktionen bereitstellt, da Sie ein [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Objekt verwenden können, die eine Vielzahl von Eigenschaften und Methoden, mit denen angepasst werden können Zugriff auf das aktuelle Fenster darstellt der bilden Sie Bearbeitungsfunktionalität. 
  
## <a name="overview-of-the-windowscollection-class"></a>Übersicht über die "WindowsCollection"-Klasse

Die [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) -Klasse stellt die folgenden Eigenschaften, die Vorlage Formularentwickler verwenden können, um die darin enthaltenen [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Objekte zu verwalten. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Count.aspx)-Eigenschaft  <br/> |Ruft die Anzahl der [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Objekte, die in der Auflistung enthalten sind.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Item.aspx)-Eigenschaft  <br/> |Ruft einen Verweis auf das angegebene [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Objekt ab.  <br/> |
   
## <a name="overview-of-the-window-class"></a>Übersicht über die "Window"-Klasse

[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Klasse bietet die folgenden Methoden und Eigenschaften, die Formularentwickler für die Interaktion mit einem InfoPath-Fenster verwenden können. Unterstützung für diese Methoden und Eigenschaften unterscheiden sich je nach den Typ des Fensters ( [WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) ) mit dem Sie arbeiten. Einige Methoden und Eigenschaften können nur mit den Typ des Fensters Editor (**WindowType.Editor**). Die verbleibenden Methoden und Eigenschaften arbeiten mit den Typ des Fensters Editor und den Typ des Designers Fensters (**WindowType.Designer**). Darüber hinaus kann wie alle InfoPath-Objektmodellmember, beim Aufruf aus einer Formularvorlage Unterstützung für Methoden und Eigenschaften variieren je nach der Sicherheitsstufe und wie das Formular bereitgestellt wird.
  
|**Name**|**Beschreibung**|**Unterstützung von Eigenschaftstypen**|
|:-----|:-----|:-----|
|[Activate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Activate.aspx) -Methode  <br/> |Aktiviert das Fenster (erteilt ihm den Fokus).   <br/> |Geben Sie **Designer** und **-Editor**  <br/> |
|[Active](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Active.aspx) -Eigenschaft  <br/> |Ruft einen **booleschen** Wert zurück, der angibt, ob das Fenster das derzeit aktive Fenster ist.  <br/> |Geben Sie **Designer** und **-Editor**  <br/> |
|[Caption](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Caption.aspx) -Eigenschaft  <br/> |Dient zum Abrufen oder Festlegen des Titeltextes für das durch das [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Objekt dargestellte Fenster.  <br/> |Nur Typ **Editor**  <br/> |
|[Close()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx) -Methode  <br/> |Schließt das Fenster mit der Aufforderung, Änderungen an ungespeicherten Formularen oder Formularen mit nicht gespeicherten Änderungen zu speichern.  <br/> |Nur Typ **Editor**  <br/> |
|[Close(Boolean)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx) -Methode  <br/> |Schließt das Fenster und erzwingt optional das Schließen eines ungespeicherten Formulars oder eines Formulars mit ungespeicherten Änderungen ohne Speichern.   <br/> |Nur Typ **Editor**  <br/> |
|[CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf die Microsoft Office- **CommandBars** -Auflistung, die dem Fenster zugeordnet ist.  <br/> |Geben Sie **Designer** und **-Editor**  <br/> |
|[Height](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Height.aspx) -Eigenschaft  <br/> |Ruft die Höhe des Fensters gemessen in Punkten ab oder legt sie fest.  <br/> |Geben Sie **Designer** und **-Editor**  <br/> |
|[Left](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Left.aspx) -Eigenschaft  <br/> |Ruft die horizontale Position des Fensters gemessen in Punkten ab oder legt sie fest.  <br/> |Geben Sie **Designer** und **-Editor**  <br/> |
|[MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.MailEnvelope.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf die [MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.aspx) -Klasse.  <br/> |Nur Typ **Editor**  <br/> |
|[TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.TaskPanes.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf die [TaskPaneCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) -Auflistung ab.  <br/> |Geben Sie **Designer** und **-Editor**  <br/> |
|[Top](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Top.aspx) -Eigenschaft  <br/> |Ruft die vertikale Position des Fensters gemessen in Punkten ab oder legt sie fest.  <br/> |Geben Sie **Designer** und **-Editor**  <br/> |
|[Width](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Width.aspx) -Eigenschaft  <br/> |Ruft die Breite des Fensters gemessen in Punkten ab oder legt sie fest.  <br/> |Geben Sie **Designer** und **-Editor**  <br/> |
|[WindowState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowState.aspx) -Eigenschaft  <br/> |Dient zum Abrufen oder Festlegen des Status des Fensters als [WindowState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.aspx) -Wert.  <br/> |Geben Sie **Designer** und **-Editor**  <br/> |
|[WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowType.aspx) -Eigenschaft  <br/> |Ruft den Typ des Fensters als einen [WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) -Enumerationswert ab.  <br/> |Geben Sie **Designer** und **-Editor**  <br/> |
|[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.XmlForm.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf das dem Fenster zugeordnete [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Objekt zurück.  <br/> |Nur Typ **Editor**  <br/> |
   
## <a name="using-the-windowscollection-and-window-classes"></a>Verwenden der Klassen "WindowsCollection" und "Window"

Die [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) -Klasse kann über die [Windows](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Windows.aspx) -Eigenschaft des [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) -Klasse zugegriffen werden. Wenn die [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) -Klasse zum Fenster eines Formulars zuzugreifen, Sie verwenden einen Indexer (Visual c#) oder übergeben Sie eine lange ganze Zahl an die **Item** -Eigenschaft (für Visual Basic), um einen Verweis auf eine Instanz des [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Objekt zurückzugeben. Mit dem folgende Code wird beispielsweise einen Verweis auf das erste [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Objekt für die aktuelle InfoPath-Sitzung in der [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) enthalten sind. 
  
```cs
Window myWindow = this.Application.Windows[0];
```

```vb
Dim myWindow As Window = Me.Application.Windows(0)
```

Sie können das derzeit geöffnete Fenster direkt und ohne Umweg über die [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) , wie in der folgenden Codezeile gezeigt mit der [ActiveWindow](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.ActiveWindow.aspx) -Eigenschaft der [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) -Klasse zugreifen. 
  
```cs
Window myWindow = this.Application.ActiveWindow;
```

```vb
Dim myWindow As Window = Me.Application.ActiveWindow
```

Ein [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Objekt kann auch mithilfe der [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) -Eigenschaft des [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Klasse, die die aktuelle Ansicht, die verwendet wird darstellt, um die Arbeit mit dem Formular zugrunde liegenden XML-Dokument zugegriffen werden. Die [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) -Eigenschaft der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse wird verwendet, um ein [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Objekt zuzugreifen, die aktuelle Ansicht darstellt. Beispielsweise wird mit dem folgende Code ein Verweis auf das [Fenster](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) , das der aktuellen Ansicht zugeordnet ist. 
  
```cs
Window myWindow = this.CurrentView.Window;
```

```vb
Dim myWindow As Window = Me.CurrentView.Window
```

> [!NOTE]
> Einige der Eigenschaften und Methoden des [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Klasse sind nur für Bearbeitungsfenster. Bei Verwendung mit dem Entwerfen geben, sie einen Fehler zurück. Welche Eigenschaften und Methoden für die einzelnen Fenster unterstützt werden, werden in der Tabelle weiter oben in diesem Thema aufgeführt. Sie können die [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Eigenschaft in Ihrem Code verwenden, um zu bestimmen, welche Fenster Sie arbeiten. 
  

