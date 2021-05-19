---
title: 'Exemplarische Vorgehensweise: Erstellen einer einfachen Formularvorlage mit Code'
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- Formularvorlagen [infopath 2007], Erstellen von verwalteten Code,Formularvorlagen mit verwalteten Code [InfoPath 2007], Erstellen,Formularvorlagen [InfoPath 2007], exemplarische Vorgehensweisen,InfoPath 2007, exemplarische Vorgehensweisen
localization_priority: Normal
ms.assetid: 0f55c8be-8641-476a-b0c8-c88adb2ac2b9
description: In Microsoft InfoPath können Sie Geschäftslogik in Visual Basic oder C# schreiben, indem Sie eine Formularvorlage im InfoPath-Designer öffnen und dann einen der Benutzeroberflächenbefehle verwenden, um einen Ereignishandler hinzuzufügen, der die Visual Studio 2012-Entwicklungsumgebung zum Schreiben ihres Codes öffnet.
ms.openlocfilehash: cc09856750ced28d35c8da172a08a31c4e3cd4a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420647"
---
# <a name="walkthrough-create-a-basic-form-template-with-code"></a>Exemplarische Vorgehensweise: Erstellen einer einfachen Formularvorlage mit Code

In Microsoft InfoPath können Sie Geschäftslogik in Visual Basic oder C# schreiben, indem Sie eine Formularvorlage im InfoPath-Designer öffnen und dann einen der Benutzeroberflächenbefehle verwenden, um einen Ereignishandler hinzuzufügen, der die Visual Studio 2012-Entwicklungsumgebung zum Schreiben ihres Codes öffnet. Standardmäßig funktionieren Formularvorlagenprojekte, die mit Visual Studio 2012 erstellt wurden, mit dem objektmodell für verwalteten Code, das von [Microsoft.Office. InfoPath-Namespace.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 
  
In dieser exemplarischen Vorgehensweise wird zunächst gezeigt, wie Sie eine einfache Hello World-Anwendung mithilfe von C# oder Visual Basic in der Visual Studio 2012-Entwicklungsumgebung erstellen. Die exemplarische Vorgehensweise endet mit einem Codebeispiel, das zeigt, wie Sie die [UserName-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) der [User-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) verwenden, um den Namen des aktuellen Benutzers abzurufen und ein **Textfeldsteuerelement** mit diesem Wert zu füllen. 
  
## <a name="prerequisites"></a>Voraussetzungen

Um diese exemplarische Vorgehensweise mithilfe der Visual Studio 2012-Entwicklungsumgebung abschließen zu können, benötigen Sie:
  
- Microsoft InfoPath mit Visual Studio 2012 installiert.
    
## <a name="hello-world-in-visual-studio-tools-for-applications"></a>Hello World in Visual Studio-Tools für Anwendungen

In der folgenden exemplarischen Vorgehensweise erfahren Sie, wie Sie Code in der Visual Studio 2012-Entwicklungsumgebung schreiben, um ein einfaches Warnungsdialogfeld anzuzeigen, indem Sie einen Ereignishandler für das [Clicked-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) der [ButtonEvent-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) schreiben, das dem **Button-Steuerelement** zugeordnet ist. 
  
### <a name="create-a-new-project-and-specify-the-programming-language"></a>Erstellen eines neuen Projekts und Angeben der Programmiersprache

1. Starten Sie den InfoPath-Designer, und doppelklicken Sie auf die Formularvorlage **Leer (InfoPath Editor)**. 
    
2. Klicken Sie zum Angeben der zu verwendenden Programmiersprache auf die Schaltfläche  **Office**, klicken Sie auf Formularoptionen,  **klicken** Sie  in der Liste Kategorie auf Programmierung, und wählen Sie dann **Visual Basic** **oder C#** in der Dropdownliste Formularvorlagencodesprache aus. 
    
   > [!NOTE]
   > Die anderen Optionen für die Programmiersprache in der Dropdownliste **Codesprache der Formularvorlage** dienen der Kompatibilität mit früheren Versionen von InfoPath. Die Optionen **C# (InfoPath 2007-kompatibel)** und **Visual Basic (InfoPath 2007-kompatibel)** können Sie für die Vorgehensweisen in diesem Thema verwenden. Wenn Sie die Optionen **C# (InfoPath 2003-kompatibel)** und **Visual Basic (InfoPath 2003-kompatibel)** verwenden möchten, lesen Sie bitte die Informationen unter [Exemplarische Vorgehensweise: Erstellen und Debuggen einer einfachen Formularvorlage mit dem InfoPath 2003-Objektmodell](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md). 
  
    Jetzt können Sie ein Steuerelement vom Typ **Schaltfläche** hinzufügen und dessen Ereignishandler erstellen. 
    
### <a name="add-a-button-control-and-event-handler"></a>Hinzufügen eines Steuerelements vom Typ "Schaltfläche" und eines Ereignishandlers

1. Klicken Sie in der Gruppe **Steuerelemente** auf das Steuerelement **Schaltfläche**, um dieses dem Formular hinzuzufügen. 
    
2. Doppelklicken Sie auf das Steuerelement **Schaltfläche**, geben Sie auf der Registerkarte Eigenschaften des Menübands den Text **Hallo** für die Eigenschaft **Etikett** ein, und klicken Sie dann auf **Benutzerdefinierter Code**. Speichern Sie das Formular bei entsprechender Aufforderung, und nennen Sie es HelloWorld.
    
   Dadurch wird die **Visual Studio-Tools für Anwendungen** mit dem Cursor im Ereignishandler für das [Clicked-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) des **Button-Steuerelements** geöffnet. 
    
   Jetzt können Sie dem Ereignishandler für die Schaltfläche Formularcode hinzufügen. 
    
### <a name="add-hello-world-code-to-the-event-handler-and-preview-the-form"></a>Hinzufügen von Code für "Hello World" zum Ereignishandler und Anzeigen einer Vorschau für das Formular

1. Geben Sie in die Ereignishandlervorlage Folgendes ein:
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   Der Code für die Formularvorlage sollte wie folgt aussehen:
    
   ```cs
    using Microsoft.Office.InfoPath;
    using System;
    using System.Windows.Forms;
    using System.Xml;
    using System.Xml.XPath;
    namespace HelloWorld
    {
        public partial class FormCode
        {
            public void InternalStartup()
            {
            ((ButtonEvent)EventManager.ControlEvents["CTRL1_5"]).Clicked += new ClickedEventHandler(CTRL1_5_Clicked);
            }
            public void CTRL1_5_Clicked(object sender, ClickedEventArgs e)
            {
            MessageBox.Show("Hello World!");
            }
        }
    }
   ```

   ```vb
    Imports Microsoft.Office.InfoPath
    Imports System
    Imports System.Windows.Forms
    Imports System.Xml
    Imports System.Xml.XPath
    Namespace HelloWorld
        Public Class FormCode
            Private Sub InternalStartup(ByVal sender As Object, ByVal e As EventArgs) Handles Me.Startup
            AddHandler DirectCast(EventManager.ControlEvents("CTRL1_5"), ButtonEvent).Clicked, AddressOf CTRL1_5_Clicked
            End Sub
            Public Sub CTRL1_5_Clicked(ByVal sender As Object, ByVal e As ClickedEventArgs)
            MessageBox.Show("Hello World!")
            End Sub
        End Class
    End Namespace
   ```

2. Wechseln Sie zum InfoPath-Designer-Fenster.
    
3. Klicken Sie auf der Registerkarte **Start** auf die Schaltfläche **Vorschau**. 
    
4. Klicken Sie auf dem Formular auf die Schaltfläche Hallo. 
    
   Ein Meldungsfeld mit dem Text "Hello World!" wird angezeigt.
    
   Im nächsten Verfahren wird gezeigt, wie Sie dem Formularcode Haltepunkte für das Debuggen hinzufügen können.
    
### <a name="debug-form-code"></a>Debuggen von Formularcode

1. Wechseln Sie zurück zum Visual Studio 2012-Fenster.
    
2. Klicken Sie auf die graue Leiste links der Zeile:
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   Ein roter Kreis wird angezeigt, und die Codezeile wird hervorgehoben, um darauf hinzuweisen, dass die Laufzeit an diesem Haltepunkt im Formularcode angehalten wird.
    
3. Klicken Sie im Menü **Debuggen** auf **Debuggen starten** (oder drücken Sie F5). 
    
4. Klicken Sie im Fenster **Vorschau** von InfoPath auf die Schaltfläche Hallo auf dem Formular.  
    
5. Der Visual Studio 2012-Code-Editor hat den Fokus, und die Haltepunktlinie wird hervorgehoben.
    
6. Klicken Sie im Menü **Debuggen** auf **Prozedurschritt** (oder drücken Sie UMSCHALT+F8), um das schrittweise Durchlaufen des Codes fortzusetzen. 
    
7. Der Ereignishandlercode wird ausgeführt, und die Meldung "Hello World!" wird angezeigt.  
    
8. Klicken **Sie auf OK,** um zum Visual Studio 2012-Code-Editor zurückzukehren, und klicken Sie dann im Menü Debuggen auf Debuggen beenden (oder drücken Sie STRG+Alt+Unterbrechung).   
    
## <a name="getting-the-current-users-name"></a>Abrufen des aktuellen Benutzernamens

Im folgenden Beispiel erfahren Sie, wie Sie die [UserName-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) der [User-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) verwenden, um den Namen des aktuellen Benutzers abzurufen und den Wert eines **Textfeldsteuerelements** mithilfe eines Ereignishandlers für das [Loading-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) auffüllen. 
  
Das Auffüllen des **Textfeldsteuerelements** erfolgt mithilfe einer Instanz der [XPathNavigator-Klasse,](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) um den Namen des aktuellen Benutzers in den XML-Knoten zu schreiben, an den das Steuerelement gebunden ist. 
  
Zunächst wird die [MainDataSource-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) der [XmlForm-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) aufgerufen, um eine Instanz der [DataSource-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) abzurufen, die das zugrunde liegende XML-Dokument des Formulars darstellt. Das [DataSource-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) ruft dann die [CreateNavigator-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) auf, die das **XPathNavigator-Objekt** erstellt und am Stammknoten der Hauptdatenquelle des Formulars positioniert. 
  
Die [SelectSingleNode-Methode](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.selectsinglenode%28v=vs.100%29.aspx) der **XPathNavigator-Klasse** wird aufgerufen, um das Mitarbeiterfeld in der Datenquelle des Formulars auszuwählen. Schließlich wird die [SetValue-Methode](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.setvalue%28v=vs.100%29.aspx) aufgerufen, um den Wert des Felds mit der [UserName-Eigenschaft zu](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) festlegen. 
  
Weitere Informationen zum Arbeiten mit **System.Xml** in Formularvorlagen für verwalteten Code finden Sie unter Arbeiten mit den [Klassen XPathNavigator und XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
### <a name="add-a-loading-event-handler"></a>Hinzufügen eines Loading-Ereignishandlers

1. Öffnen Sie die Formularvorlage "HelloWorld", die Sie in der vorherigen exemplarischen Vorgehensweise im InfoPath-Designer erstellt haben.
    
2. Klicken Sie auf der Registerkarte **Ansicht** auf **Felder anzeigen**.
    
3. Klicken Sie mit der rechten Maustaste auf den Ordner **myFields**, und klicken Sie dann auf **Hinzufügen**.
    
4. Geben **Sie unter Name** mitarbeiter ein, und klicken Sie dann auf **OK**.
    
5. Ziehen Sie das Feld employee in die Ansicht. 
    
6. Klicken Sie auf der Registerkarte **Entwickler** auf **Loading-Ereignis**.
    
   Dadurch wird ein Ereignishandler für das [Loading-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) erstellt und der Fokus auf diesen Ereignishandler im Code-Editor verschieben. 
    
7. Geben Sie im Code-Editor Folgendes ein:
    
   ```cs
    public void FormEvents_Loading(object sender, LoadingEventArgs e)
    {
        XPathNavigator dataSource;
        dataSource = this.MainDataSource.CreateNavigator();
        dataSource.SelectSingleNode(
            "/my:myFields/my:employee", NamespaceManager).SetValue(this.User.UserName);
    }
   ```
 
   ```vb
    Public Sub FormEvents_Loading(ByVal sender As Object, ByVal e As LoadingEventArgs)
        Dim dataSource As XPathNavigator
        dataSource = Me.MainDataSource.CreateNavigator
        dataSource.SelectSingleNode( _
            "/my:myFields/my:employee", NamespaceManager).SetValue(Me.User.UserName)
    End Sub
   ```

8. Wechseln Sie in das InfoPath-Formularentwurfsfenster, und klicken Sie auf der Registerkarte **Start** auf die Schaltfläche **Vorschau**, um eine Vorschau des Formulars anzuzeigen. 
    
   Im Feld employee sollte automatisch Ihr Benutzername eingelesen werden. 
    
## <a name="next-steps"></a>Nächste Schritte

- Informationen zum Arbeiten mit Ereignishandlern für andere Steuerelemente und Ereignisse finden Sie unter [Add an Event Handler](how-to-add-an-event-handler.md).
    
- Weitere Informationen zum Anzeigen und Debuggen von Code in Formularvorlagen finden Sie unter Vorschau und Debuggen von [InfoPath-Formularvorlagen mit Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).
    
- Informationen zum Bereitstellen einer Formularvorlage mit verwalteten Code finden Sie unter [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).
    
- Weitere Informationen zum InfoPath-Objektmodell sowie zu allgemeinen Programmieraufgaben in Formularvorlagen mit verwaltetem Code finden Sie unter [Grundlegendes zum InfoPath-Objektmodell und zu allgemeinen Entwickleraufgaben](understanding-the-infopath-object-model-and-common-developer-tasks.md).
    
## <a name="see-also"></a>Siehe auch

- [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)

