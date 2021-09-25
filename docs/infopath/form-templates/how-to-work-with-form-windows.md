---
title: Arbeiten mit formular Windows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- windowscollection [infopath 2007],form windows [InfoPath 2007],Window class [InfoPath 2007]
ms.localizationpriority: medium
ms.assetid: 32ae2427-882b-45f8-8754-0e8c27fc23ba
description: Sie können bei der Programmierarbeit mit einem InfoPath-Formular Code schreiben, mit dem auf die Fenster eines Formulars zugegriffen wird, und dann einige der häufig enthaltenen Elemente anpassen. Das von Microsoft bereitgestellte InfoPath-Objektmodell. Office. Der InfoPath-Namespace unterstützt den Zugriff auf die Fenster eines Formulars durch die Verwendung der Window-Klasse in Verbindung mit der WindowCollection-Klasse.
ms.openlocfilehash: 7edb5f4e1530b64251ea89f0f41ad6926a11f2ad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568103"
---
# <a name="work-with-form-windows"></a>Arbeiten mit formular Windows

Sie können bei der Programmierarbeit mit einem InfoPath-Formular Code schreiben, mit dem auf die Fenster eines Formulars zugegriffen wird, und dann einige der häufig enthaltenen Elemente anpassen. Das von Microsoft.Office bereitgestellte InfoPath-Objektmodell. [ Der InfoPath-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) unterstützt den Zugriff auf die Fenster eines Formulars durch die Verwendung der [Window-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) in Verbindung mit der [WindowCollection-Klasse.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) 
  
> [!NOTE]
> Die Klassen zum Arbeiten mit den Fenstern eines Formulars sind nur dann verfügbar, wenn ein **InfoPath Editor-Formular** verwendet wird. Wenn die Einstellung **Kompatibilität** einer Formularvorlage **Webbrowserformular** lautet, sind diese Klassen nicht verfügbar. 
  
In InfoPath gibt es zwei Fenstertypen: 
  
- Das Bearbeitungsfenster, das verwendet wird, wenn ein Benutzer ein Formular ausfüllt.
    
- Das Entwurfsfenster, das verwendet wird, wenn ein Benutzer eine Formularvorlage entwirft.
    
Beim Schreiben von Code in einer Formularvorlage stellt das Bearbeitungsfenster die nützlichste Funktionalität bereit, da Sie ein [Window-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) verwenden können, das das aktuelle Fenster darstellt, um auf eine Vielzahl von Eigenschaften und Methoden zuzugreifen, die zum Anpassen der Formularbearbeitung verwendet werden können. 
  
## <a name="overview-of-the-windowscollection-class"></a>Übersicht über die "WindowsCollection"-Klasse

Die [WindowCollection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) stellt die folgenden Eigenschaften bereit, mit denen Entwickler von Formularvorlagen die darin enthaltenen [Window-Objekte](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) verwalten können. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Count.aspx)-Eigenschaft  <br/> |Ruft die Anzahl der in der Auflistung enthaltenen [Window-Objekte](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) ab.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Item.aspx)-Eigenschaft  <br/> |Ruft einen Verweis auf das angegebene [Window -Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) ab.  <br/> |
   
## <a name="overview-of-the-window-class"></a>Übersicht über die "Window"-Klasse

Die [Window-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) stellt die folgenden Methoden und Eigenschaften bereit, die Formularentwickler für die Interaktion mit einem InfoPath-Fenster verwenden können. Die Unterstützung für diese Methoden und Eigenschaften hängt vom Typ des Fensters ( [WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) ) ab, mit dem Sie arbeiten. Manche Methoden und Eigenschaften funktionieren nur mit dem Bearbeitungsfenstertyp (**WindowType.Editor**). Die übrigen Methoden und Eigenschaften funktionieren sowohl mit dem Bearbeitungsfenstertyp als auch mit dem Entwurfsfenstertyp (**WindowType.Designer**). Darüber hinaus kann die Unterstützung für Methoden und Eigenschaften wie bei allen InfoPath-Objektmodellmembern je nach der Sicherheitsebene und der Bereitstellungsart des Formulars variieren.
  
|**Name**|**Beschreibung**|**Unterstützung des Fenstertyps**|
|:-----|:-----|:-----|
|[Activate-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Activate.aspx)  <br/> |Aktiviert das Fenster (erteilt ihm den Fokus).  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[Active-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Active.aspx)  <br/> |Ruft einen Wert vom Typ **Boolean** ab, der angibt, ob es sich bei dem Fenster um das zurzeit aktive Fenster handelt.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[Caption-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Caption.aspx)  <br/> |Ruft den Beschriftungstext für das durch das [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Objekt dargestellte Fenster ab oder legt den Text fest.  <br/> |Nur Typ **Editor**  <br/> |
|[Close()-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx)  <br/> |Schließt das Fenster mit der Aufforderung, Änderungen an ungespeicherten Formularen oder Formularen mit nicht gespeicherten Änderungen zu speichern.  <br/> |Nur Typ **Editor**  <br/> |
|[Close(Boolean)-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx)  <br/> |Schließt das Fenster und erzwingt optional das Schließen eines ungespeicherten Formulars oder eines Formulars mit ungespeicherten Änderungen ohne Speichern.  <br/> |Nur Typ **Editor**  <br/> |
|[CommandBars-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx)  <br/> |Ruft einen Verweis auf die Microsoft Office **CommandBars**-Auflistung ab, die dem Fenster zugeordnet ist.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[Height-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Height.aspx)  <br/> |Ruft die Höhe des Fensters gemessen in Punkten ab oder legt sie fest.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[Left-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Left.aspx)  <br/> |Ruft die horizontale Position des Fensters gemessen in Punkten ab oder legt sie fest.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[MailEnvelope-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.MailEnvelope.aspx)  <br/> |Ruft einen Verweis auf die [MailEnvelope-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.aspx) ab.  <br/> |Nur Typ **Editor**  <br/> |
|[TaskPanes-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.TaskPanes.aspx)  <br/> |Ruft einen Verweis auf die [TaskPaneCollection -Auflistung](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) ab.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[Top-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Top.aspx)  <br/> |Ruft die vertikale Position des Fensters gemessen in Punkten ab oder legt sie fest.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[Width-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Width.aspx)  <br/> |Ruft die Breite des Fensters gemessen in Punkten ab oder legt sie fest.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[WindowState-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowState.aspx)  <br/> |Ruft den Status des Fensters als [WindowState-Wert](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.aspx) ab oder legt diesen fest.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[WindowType-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowType.aspx)  <br/> |Ruft den Typ des Fensters als [WindowType-Enumerationswert](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) ab.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[XmlForm-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.XmlForm.aspx)  <br/> |Gibt einen Verweis auf das [xmlForm -Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) zurück, das dem Fenster zugeordnet ist.  <br/> |Nur Typ **Editor**  <br/> |
   
## <a name="using-the-windowscollection-and-window-classes"></a>Verwenden der Klassen "WindowsCollection" und "Window"

Auf die [WindowCollection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) kann über die [Windows](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Windows.aspx) Eigenschaft der [Application-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) zugegriffen werden. Wenn Sie die [WindowCollection-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) verwenden, um auf die Fenster eines Formulars zuzugreifen, verwenden Sie einen Indexer (für Visual C#) oder übergeben eine lange ganze Zahl an die **Item-Eigenschaft** (für Visual Basic), um einen Verweis auf eine [Window-Objektinstanz](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) zurückzugeben. Der folgende Code legt beispielsweise einen Verweis auf das erste [Window-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) fest, das in der [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) für die aktuelle InfoPath-Sitzung enthalten ist. 
  
```cs
Window myWindow = this.Application.Windows[0];
```

```vb
Dim myWindow As Window = Me.Application.Windows(0)
```

Sie können direkt mithilfe der [ActiveWindow-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.ActiveWindow.aspx) der [Application-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) auf das aktuell geöffnete Fenster zugreifen, ohne die [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) zu durchlaufen, wie in der folgenden Codezeile dargestellt. 
  
```cs
Window myWindow = this.Application.ActiveWindow;
```

```vb
Dim myWindow As Window = Me.Application.ActiveWindow
```

Auf ein [Window-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) kann auch mithilfe der [Window-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) der [View-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) zugegriffen werden, die die aktuelle Ansicht darstellt, die zum Arbeiten mit dem dem Formular zugrunde liegenden XML-Dokument verwendet wird. Die [CurrentView-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) der [XmlForm-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) wird verwendet, um auf ein [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Objekt zuzugreifen, das die aktuelle Ansicht darstellt. Der folgende Code legt beispielsweise einen Verweis auf das [Fenster](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) fest, das der aktuellen Ansicht zugeordnet ist. 
  
```cs
Window myWindow = this.CurrentView.Window;
```

```vb
Dim myWindow As Window = Me.CurrentView.Window
```

> [!NOTE]
> Einige der Eigenschaften und Methoden der [Window-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) gelten nur für den Bearbeitungsfenstertyp. wenn sie mit dem Entwurfsfenstertyp verwendet werden, wird ein Fehler zurückgegeben. Die für jeden Fenstertyp unterstützten Eigenschaften und Methoden werden in der Tabelle weiter oben in diesem Thema aufgelistet. Sie können die [Window-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) in Ihrem Code verwenden, um zu bestimmen, mit welchem Fenstertyp Sie arbeiten. 
  

