---
title: Arbeiten mit Formularfenstern
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- WindowsCollection [InfoPath 2007], Formularfenster [InfoPath 2007], Fensterklasse [InfoPath 2007]
localization_priority: Normal
ms.assetid: 32ae2427-882b-45f8-8754-0e8c27fc23ba
description: Sie können bei der Programmierarbeit mit einem InfoPath-Formular Code schreiben, mit dem auf die Fenster eines Formulars zugegriffen wird, und dann einige der häufig enthaltenen Elemente anpassen. Das vom Microsoft. Office. InfoPath-Namespace bereitgestellte InfoPath-Objektmodell unterstützt den Zugriff auf die Fenster eines Formulars durch die Verwendung der Window-Klasse in Verbindung mit der WindowCollection-Klasse.
ms.openlocfilehash: 018357519e27629c29b2611bd0a88b8d64f0a1eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431064"
---
# <a name="work-with-form-windows"></a>Arbeiten mit Formularfenstern

Sie können bei der Programmierarbeit mit einem InfoPath-Formular Code schreiben, mit dem auf die Fenster eines Formulars zugegriffen wird, und dann einige der häufig enthaltenen Elemente anpassen. Das vom [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellte InfoPath-Objektmodell unterstützt den Zugriff auf die Fenster eines Formulars durch die Verwendung der [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Klasse in Verbindung mit der [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) -Klasse. 
  
> [!NOTE]
> Die Klassen zum Arbeiten mit den Fenstern eines Formulars sind nur dann verfügbar, wenn ein **InfoPath Editor-Formular** verwendet wird. Wenn die Einstellung **Kompatibilität** einer Formularvorlage **Webbrowserformular** lautet, sind diese Klassen nicht verfügbar. 
  
In InfoPath gibt es zwei Fenstertypen: 
  
- Das Bearbeitungsfenster, das verwendet wird, wenn ein Benutzer ein Formular ausfüllt.
    
- Das Entwurfsfenster, das verwendet wird, wenn ein Benutzer eine Formularvorlage entwirft.
    
Beim Schreiben von Code in einer Formularvorlage ist es das Bearbeitungsfenster, das die nützlichsten Funktionen bereitstellt, da Sie ein [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Objekt, das das aktuelle Fenster darstellt, verwenden können, um auf eine Vielzahl von Eigenschaften und Methoden zuzugreifen, die zum Anpassen der Formularbearbeitungsumgebung. 
  
## <a name="overview-of-the-windowscollection-class"></a>Übersicht über die "WindowsCollection"-Klasse

Die [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) -Klasse stellt die folgenden Eigenschaften bereit, die Formularvorlagenentwickler verwenden können, um die darin enthaltenen [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Objekte zu verwalten. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Count.aspx)-Eigenschaft  <br/> |Ruft die Anzahl der [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Objekte ab, die in der Auflistung enthalten sind.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Item.aspx)-Eigenschaft  <br/> |Ruft einen Verweis auf das angegebene [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Objekt ab.  <br/> |
   
## <a name="overview-of-the-window-class"></a>Übersicht über die "Window"-Klasse

Die [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Klasse stellt die folgenden Methoden und Eigenschaften bereit, die Formularentwickler für die Interaktion mit einem InfoPath-Fenster verwenden können. Die Unterstützung für diese Methoden und Eigenschaften hängt vom Typ des Fensters ( [WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) ) ab, mit dem Sie arbeiten. Manche Methoden und Eigenschaften funktionieren nur mit dem Bearbeitungsfenstertyp (**WindowType.Editor**). Die übrigen Methoden und Eigenschaften funktionieren sowohl mit dem Bearbeitungsfenstertyp als auch mit dem Entwurfsfenstertyp (**WindowType.Designer**). Darüber hinaus kann die Unterstützung für Methoden und Eigenschaften wie bei allen InfoPath-Objektmodellmembern je nach der Sicherheitsebene und der Bereitstellungsart des Formulars variieren.
  
|**Name**|**Beschreibung**|**Unterstützung des Fenstertyps**|
|:-----|:-----|:-----|
|[Activate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Activate.aspx) -Methode  <br/> |Aktiviert das Fenster (erteilt ihm den Fokus).  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[Active](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Active.aspx) -Eigenschaft  <br/> |Ruft einen Wert vom Typ **Boolean** ab, der angibt, ob es sich bei dem Fenster um das zurzeit aktive Fenster handelt.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[Caption](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Caption.aspx) -Eigenschaft  <br/> |Dient zum Abrufen oder Festlegen des Beschriftungstexts für das Fenster, das durch das [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Objekt dargestellt wird.  <br/> |Nur Typ **Editor**  <br/> |
|[Schließ ()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx) -Methode  <br/> |Schließt das Fenster mit der Aufforderung, Änderungen an ungespeicherten Formularen oder Formularen mit nicht gespeicherten Änderungen zu speichern.  <br/> |Nur Typ **Editor**  <br/> |
|[Schließ (Boolean)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx) -Methode  <br/> |Schließt das Fenster und erzwingt optional das Schließen eines ungespeicherten Formulars oder eines Formulars mit ungespeicherten Änderungen ohne Speichern.  <br/> |Nur Typ **Editor**  <br/> |
|[CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf die Microsoft Office **CommandBars**-Auflistung ab, die dem Fenster zugeordnet ist.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[Height](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Height.aspx) -Eigenschaft  <br/> |Ruft die Höhe des Fensters gemessen in Punkten ab oder legt sie fest.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[Left](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Left.aspx) -Eigenschaft  <br/> |Ruft die horizontale Position des Fensters gemessen in Punkten ab oder legt sie fest.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.MailEnvelope.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf die [MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.aspx) -Klasse ab.  <br/> |Nur Typ **Editor**  <br/> |
|[TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.TaskPanes.aspx) -Eigenschaft  <br/> |Ruft einen Verweis auf die [TaskPaneCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) -Auflistung ab.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[Top](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Top.aspx) -Eigenschaft  <br/> |Ruft die vertikale Position des Fensters gemessen in Punkten ab oder legt sie fest.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[Width](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Width.aspx) -Eigenschaft  <br/> |Ruft die Breite des Fensters gemessen in Punkten ab oder legt sie fest.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[WindowState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowState.aspx) -Eigenschaft  <br/> |Dient zum Abrufen oder Festlegen des Status des Fensters als [WindowState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.aspx) -Wert.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowType.aspx) -Eigenschaft  <br/> |Ruft den Typ des Fensters als Wert der [WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) -Enumeration ab.  <br/> |Sowohl Typ **Designer** als auch **Editor**  <br/> |
|[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.XmlForm.aspx) -Eigenschaft  <br/> |Gibt einen Verweis auf das [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Objekt zurück, das dem Fenster zugeordnet ist.  <br/> |Nur Typ **Editor**  <br/> |
   
## <a name="using-the-windowscollection-and-window-classes"></a>Verwenden der Klassen "WindowsCollection" und "Window"

Auf [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) die WindowCollection-Klasse kann über die [Windows](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Windows.aspx) -Eigenschaft der [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) -Klasse zugegriffen werden. Wenn Sie die [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) -Klasse verwenden, um auf die Fenster eines Formulars zuzugreifen, verwenden Sie einen Indexer (für Visual C#) oder eine lange ganze Zahl an die **Item** -Eigenschaft (für Visual Basic), um einen Verweis auf eine [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Objektinstanz zurückzugeben. Mit dem folgenden Code wird beispielsweise ein Verweis auf das erste [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Objekt festgelegt [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) , das in der WindowCollection für die aktuelle InfoPath-Sitzung enthalten ist. 
  
```cs
Window myWindow = this.Application.Windows[0];
```

```vb
Dim myWindow As Window = Me.Application.Windows(0)
```

Sie können direkt auf das derzeit geöffnete Fenster zugreifen, indem Sie die [ActiveWindow](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.ActiveWindow.aspx) -Eigenschaft der [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) -Klasse verwenden, ohne die [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) zu durchlaufen, wie in der folgenden Codezeile dargestellt. 
  
```cs
Window myWindow = this.Application.ActiveWindow;
```

```vb
Dim myWindow As Window = Me.Application.ActiveWindow
```

Auf ein [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Objekt kann auch mithilfe der [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) -Eigenschaft der [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Klasse zugegriffen werden, die die aktuelle Ansicht darstellt, die verwendet wird, um mit dem dem Formular zugrunde liegenden XML-Dokument zu arbeiten. Die [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) -Eigenschaft der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse wird verwendet, um auf ein [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) -Objekt zuzugreifen, das die aktuelle Ansicht darstellt. Mit dem folgenden Code wird beispielsweise ein Verweis auf das [Fenster](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) festgelegt, das der aktuellen Ansicht zugeordnet ist. 
  
```cs
Window myWindow = this.CurrentView.Window;
```

```vb
Dim myWindow As Window = Me.CurrentView.Window
```

> [!NOTE]
> Einige der Eigenschaften und Methoden der [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Klasse sind nur für den Bearbeitungsfenstertyp; Wenn Sie mit dem Entwurfs Fenstertyp verwendet wird, wird ein Fehler zurückgegeben. Die für jeden Fenstertyp unterstützten Eigenschaften und Methoden werden in der Tabelle weiter oben in diesem Thema aufgelistet. Sie können die [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) -Eigenschaft im Code verwenden, um zu bestimmen, mit welchem Fenstertyp Sie arbeiten. 
  

