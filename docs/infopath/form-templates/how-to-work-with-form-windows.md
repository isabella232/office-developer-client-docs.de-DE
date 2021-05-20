---
title: Arbeiten mit formular Windows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- windowscollection [infopath 2007],form windows [InfoPath 2007],Window class [InfoPath 2007]
localization_priority: Normal
ms.assetid: 32ae2427-882b-45f8-8754-0e8c27fc23ba
description: Sie können bei der Programmierarbeit mit einem InfoPath-Formular Code schreiben, mit dem auf die Fenster eines Formulars zugegriffen wird, und dann einige der häufig enthaltenen Elemente anpassen. Das von Microsoft bereitgestellte InfoPath-Objektmodell. Office. Der InfoPath-Namespace unterstützt den Zugriff auf die Fenster eines Formulars mithilfe der Window-Klasse in Verbindung mit der WindowCollection-Klasse.
ms.openlocfilehash: 018357519e27629c29b2611bd0a88b8d64f0a1eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431064"
---
# <a name="work-with-form-windows"></a>Arbeiten mit formular Windows

Sie können bei der Programmierarbeit mit einem InfoPath-Formular Code schreiben, mit dem auf die Fenster eines Formulars zugegriffen wird, und dann einige der häufig enthaltenen Elemente anpassen. Das infoPath-Objektmodell, das von [Microsoft.Office. Der InfoPath-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) unterstützt den Zugriff auf die Fenster eines Formulars mithilfe der [Window-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) in Verbindung mit der [WindowCollection-Klasse.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) 
  
> [!NOTE]
> Die Klassen zum Arbeiten mit den Fenstern eines Formulars sind nur dann verfügbar, wenn ein **InfoPath Editor-Formular** verwendet wird. Wenn die Einstellung **Kompatibilität** einer Formularvorlage **Webbrowserformular** lautet, sind diese Klassen nicht verfügbar. 
  
In InfoPath gibt es zwei Fenstertypen: 
  
- Das Bearbeitungsfenster, das verwendet wird, wenn ein Benutzer ein Formular ausfüllt.
    
- Das Entwurfsfenster, das verwendet wird, wenn ein Benutzer eine Formularvorlage entwirft.
    
Beim Schreiben von Code in einer Formularvorlage bietet das Bearbeitungsfenster die nützlichsten Funktionen, da Sie ein [Window-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) verwenden können, das das aktuelle Fenster darstellt, um auf eine Vielzahl von Eigenschaften und Methoden zu zugreifen, die zum Anpassen der Formularbearbeitungserfahrung verwendet werden können. 
  
## <a name="overview-of-the-windowscollection-class"></a>Übersicht über die "WindowsCollection"-Klasse

Die [WindowCollection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) stellt die folgenden Eigenschaften zur Verfügung, mit denen Entwickler von Formularvorlagen die [window-Objekte](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) verwalten können, die sie enthält. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Count.aspx)-Eigenschaft  <br/> |Ruft eine Anzahl der [Window-Objekte](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) ab, die in der Auflistung enthalten sind.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Item.aspx)-Eigenschaft  <br/> |Ruft einen Verweis auf das angegebene [Window-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) ab.  <br/> |
   
## <a name="overview-of-the-window-class"></a>Übersicht über die "Window"-Klasse

Die [Window-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) bietet die folgenden Methoden und Eigenschaften, mit denen Formularentwickler mit einem InfoPath-Fenster interagieren können. Die Unterstützung für diese Methoden und Eigenschaften hängt vom Typ des Fensters ( [WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) ) ab, mit dem Sie arbeiten. Manche Methoden und Eigenschaften funktionieren nur mit dem Bearbeitungsfenstertyp (**WindowType.Editor**). Die übrigen Methoden und Eigenschaften funktionieren sowohl mit dem Bearbeitungsfenstertyp als auch mit dem Entwurfsfenstertyp (**WindowType.Designer**). Darüber hinaus kann die Unterstützung für Methoden und Eigenschaften wie bei allen InfoPath-Objektmodellmembern je nach der Sicherheitsebene und der Bereitstellungsart des Formulars variieren.
  
|**Name**|**Beschreibung**|**Unterstützung des Fenstertyps**|
|:-----|:-----|:-----|
|[Activate-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Activate.aspx)  <br/> |Aktiviert das Fenster (erteilt ihm den Fokus).  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[Active-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Active.aspx)  <br/> |Ruft einen Wert vom Typ **Boolean** ab, der angibt, ob es sich bei dem Fenster um das zurzeit aktive Fenster handelt.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[Caption-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Caption.aspx)  <br/> |Ruft den Beschriftungstext für das Fenster ab, das durch das Window-Objekt dargestellt wird, oder legt [den Text](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) fest.  <br/> |Nur Typ **Editor**  <br/> |
|[Close()-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx)  <br/> |Schließt das Fenster mit der Aufforderung, Änderungen an ungespeicherten Formularen oder Formularen mit nicht gespeicherten Änderungen zu speichern.  <br/> |Nur Typ **Editor**  <br/> |
|[Close(Boolean)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx)  <br/> |Schließt das Fenster und erzwingt optional das Schließen eines ungespeicherten Formulars oder eines Formulars mit ungespeicherten Änderungen ohne Speichern.  <br/> |Nur Typ **Editor**  <br/> |
|[CommandBars-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx)  <br/> |Ruft einen Verweis auf die Microsoft Office **CommandBars**-Auflistung ab, die dem Fenster zugeordnet ist.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[Height-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Height.aspx)  <br/> |Ruft die Höhe des Fensters gemessen in Punkten ab oder legt sie fest.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[Left-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Left.aspx)  <br/> |Ruft die horizontale Position des Fensters gemessen in Punkten ab oder legt sie fest.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[MailEnvelope-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.MailEnvelope.aspx)  <br/> |Ruft einen Verweis auf die [MailEnvelope-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.aspx) ab.  <br/> |Nur Typ **Editor**  <br/> |
|[TaskPanes-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.TaskPanes.aspx)  <br/> |Ruft einen Verweis auf die [TaskPaneCollection-Auflistung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) ab.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[Top-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Top.aspx)  <br/> |Ruft die vertikale Position des Fensters gemessen in Punkten ab oder legt sie fest.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[Width-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Width.aspx)  <br/> |Ruft die Breite des Fensters gemessen in Punkten ab oder legt sie fest.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[WindowState-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowState.aspx)  <br/> |Ruft den Zustand des Fensters als WindowState-Wert ab oder legt [den Zustand fest.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.aspx)  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[WindowType-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowType.aspx)  <br/> |Ruft den Typ des Fensters als [WindowType-Enumerationswert](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) ab.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[XmlForm-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.XmlForm.aspx)  <br/> |Gibt einen Verweis auf das [dem Fenster zugeordnete XmlForm-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) zurück.  <br/> |Nur Typ **Editor**  <br/> |
   
## <a name="using-the-windowscollection-and-window-classes"></a>Verwenden der Klassen "WindowsCollection" und "Window"

Auf [die WindowCollection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) kann über die [Windows](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Windows.aspx) der [Application-Klasse zugegriffen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) werden. Wenn Sie die [WindowCollection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) für den Zugriff auf die Fenster eines Formulars verwenden, verwenden Sie einen Indexer (für Visual C#) oder übergeben eine lange ganze Zahl an die **Item-Eigenschaft** (für Visual Basic), um einen Verweis auf eine [Window-Objektinstanz](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) zurück zu geben. Der folgende Code legt beispielsweise einen Verweis auf das erste [Window-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) fest, das in [windowCollection für](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) die aktuelle InfoPath-Sitzung enthalten ist. 
  
```cs
Window myWindow = this.Application.Windows[0];
```

```vb
Dim myWindow As Window = Me.Application.Windows(0)
```

Sie können direkt mit der [ActiveWindow-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.ActiveWindow.aspx) der [Application-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) auf das derzeit geöffnete Fenster zugreifen, ohne die [WindowCollection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) zu durchlaufen, wie in der folgenden Codezeile gezeigt. 
  
```cs
Window myWindow = this.Application.ActiveWindow;
```

```vb
Dim myWindow As Window = Me.Application.ActiveWindow
```

Auf [ein Window-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) kann auch mithilfe der [Window-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) der [View-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) zugegriffen werden, die die aktuelle Ansicht darstellt, die für die Arbeit mit dem dem Formular zugrunde liegenden XML-Dokument verwendet wird. Die [CurrentView-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) der [XmlForm-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) wird für den Zugriff auf ein [View-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) verwendet, das die aktuelle Ansicht darstellt. Der folgende Code legt beispielsweise einen Verweis auf das [Fenster](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) fest, das der aktuellen Ansicht zugeordnet ist. 
  
```cs
Window myWindow = this.CurrentView.Window;
```

```vb
Dim myWindow As Window = Me.CurrentView.Window
```

> [!NOTE]
> Einige der Eigenschaften und Methoden der [Window-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) sind nur für den Bearbeitungsfenstertyp. Wenn sie mit dem Designfenstertyp verwendet werden, wird ein Fehler zurückgegeben. Die für jeden Fenstertyp unterstützten Eigenschaften und Methoden werden in der Tabelle weiter oben in diesem Thema aufgelistet. Sie können die [Window-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) in Ihrem Code verwenden, um zu bestimmen, mit welchem Fenstertyp Sie arbeiten. 
  

