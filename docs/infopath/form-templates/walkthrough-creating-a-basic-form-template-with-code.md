---
title: 'Exemplarische Vorgehensweise: Erstellen einer einfachen Formularvorlage mit code'
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- 'Formularvorlagen [Infopath 2007], Erstellen von verwaltetem Code, verwalteten code von Formularvorlagen [InfoPath 2007], erstellen, Formularvorlagen [InfoPath 2007], exemplarische Vorgehensweisen, die InfoPath 2007: Erste Schritte'
localization_priority: Normal
ms.assetid: 0f55c8be-8641-476a-b0c8-c88adb2ac2b9
description: In Microsoft InfoPath können Sie Schreiben von Geschäftslogik in Visual Basic oder c# durch Öffnen einer Formularvorlage im InfoPath-Designer, und klicken Sie dann mit einer der den Befehlen der Benutzeroberfläche um einen Ereignishandler hinzuzufügen, der geöffnet wird, die Entwicklungsumgebung von Visual Studio 2012 für Schreiben des Codes.
ms.openlocfilehash: 8c98d71c26f8e56c532b2a4467218c366072b2ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790860"
---
# <a name="walkthrough-create-a-basic-form-template-with-code"></a>Exemplarische Vorgehensweise: Erstellen einer einfachen Formularvorlage mit code

In Microsoft InfoPath können Sie Schreiben von Geschäftslogik in Visual Basic oder c# durch Öffnen einer Formularvorlage im InfoPath-Designer, und klicken Sie dann mit einer der den Befehlen der Benutzeroberfläche um einen Ereignishandler hinzuzufügen, der geöffnet wird, die Entwicklungsumgebung von Visual Studio 2012 für Schreiben des Codes. Standardmäßig erstellt Formular Vorlagenprojekte mithilfe von Visual Studio 2012 funktionieren in Verbindung mit dem Objektmodell für verwalteten Code vom [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellt. 
  
Zuerst werden in dieser exemplarischen Vorgehensweise erstellen Sie eine einfache "Hello World"-Anwendung mit c# oder Visual Basic in der Entwicklungsumgebung von Visual Studio 2012 veranschaulicht. Die exemplarische Vorgehensweise endet mit dem ein Codebeispiel, in dem Sie zeigt, wie die [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) -Eigenschaft der [Benutzer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) -Klasse verwenden, um den aktuellen Namen des Benutzers abrufen, und füllen Sie ein **Textfeld** -Steuerelement mit diesem Wert. 
  
## <a name="prerequisites"></a>Voraussetzungen

Für die Durchführung dieser exemplarischen Vorgehensweise mithilfe der Visual Studio 2012-Entwicklungsumgebung benötigen Sie:
  
- Microsoft InfoPath mit Visual Studio 2012 installiert.
    
## <a name="hello-world-in-visual-studio-tools-for-applications"></a>Hello World in Visual Studio-Tools für Anwendungen

In der folgenden exemplarischen Vorgehensweise erfahren Sie, wie das Schreiben von Code in der Entwicklungsumgebung von Visual Studio 2012 um ein einfaches Warnungsdialogfeld anzeigen, indem Sie einen Ereignishandler für das [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) -Ereignis der [ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) -Klasse, die verbunden ist schreiben mit der **Schaltfläche** -Steuerelement. 
  
### <a name="create-a-new-project-and-specify-the-programming-language"></a>Erstellen eines neuen Projekts und Angeben der Programmiersprache

1. Starten Sie den InfoPath-Designer, und doppelklicken Sie dann auf die Formularvorlage **leer (InfoPath Editor)** . 
    
2. Um anzugeben, welche Programmiersprache verwenden, klicken Sie auf die **Office-Schaltfläche**, klicken Sie auf **Formularoptionen**, klicken Sie in der Liste **Kategorie** auf **Programmierung** , und wählen Sie dann aus der Formularvorlage **aus **Visual Basic** oder **Visual c#** Sprache Code** Dropdown-Listenfeld. 
    
   > [!NOTE]
   > Die anderen programming Language-Optionen in der Dropdownliste **Codesprache der Formularvorlage** bieten Kompatibilität mit früheren Versionen von InfoPath. Die Verfahren in diesem Thema werden die Optionen für **c# (kompatibel mit InfoPath 2007)** und **Visual Basic (kompatibel mit InfoPath 2007)** entwickelt. Um die Optionen für **c# (kompatibel mit InfoPath 2003)** und **Visual Basic (kompatibel mit InfoPath 2003)** verwenden, jedoch finden Sie unter [Exemplarische Vorgehensweise: Erstellen und Debuggen einer grundlegenden Formular Vorlage mithilfe des InfoPath 2003-Objektmodells](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md). 
  
    Sie sind jetzt bereit, die ein **Button** -Steuerelement hinzufügen und dessen Ereignishandler erstellen. 
    
### <a name="add-a-button-control-and-event-handler"></a>Hinzufügen eines Steuerelements vom Typ "Schaltfläche" und eines Ereignishandlers

1. Klicken Sie in der Gruppe **Steuerelemente** auf das **Schaltfläche** -Steuerelement, um dieses dem Formular hinzuzufügen. 
    
2. Doppelklicken Sie auf das **Button** -Steuerelement, geben Sie Hello für die **Label** -Eigenschaft auf der Registerkarte **Eigenschaften** des Menübands, und klicken Sie dann auf **Benutzerdefinierter Code**. Wenn Sie aufgefordert werden, speichern Sie das Formular, und nennen Sie sie "HelloWorld".
    
   Dadurch wird die **Visual Studio Tools for Applications** -Umgebung mit dem Mauszeiger geöffnet, in der Ereignisprozedur Handler für das [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) -Ereignis der **Schaltfläche** steuern. 
    
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
    
3. Klicken Sie auf die Schaltfläche **Vorschau** auf der Registerkarte **Start** . 
    
4. Klicken Sie auf die Schaltfläche Hallo auf dem Formular. 
    
   Ein Meldungsfeld mit dem Text "Hello World!" wird angezeigt.
    
   Im nächsten Verfahren wird gezeigt, wie Sie dem Formularcode Haltepunkte für das Debuggen hinzufügen können.
    
### <a name="debug-form-code"></a>Debuggen von Formularcode

1. Wechseln Sie in das Fenster des Visual Studio 2012.
    
2. Klicken Sie auf die graue Leiste links der Zeile:
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   Ein roter Kreis wird angezeigt, und die Codezeile wird hervorgehoben, um darauf hinzuweisen, dass die Laufzeit an diesem Haltepunkt im Formularcode angehalten wird.
    
3. Klicken Sie im Menü **Debuggen** auf **Debuggen starten,** klicken Sie auf (oder drücken Sie F5). 
    
4. Klicken Sie im InfoPath- **Vorschau** klicken Sie auf die Schaltfläche Hallo auf dem Formular. 
    
5. Im Code-Editor von Visual Studio 2012 erhält den Fokus, und die haltepunktlinie wird hervorgehoben.
    
6. Klicken Sie im Menü **Debuggen** auf **Prozedurschritt** (oder drücken Sie UMSCHALT + F8) um das schrittweise Durchlaufen des Codes fortzusetzen. 
    
7. Der Ereignishandlercode wird ausgeführt, und die Meldung "Hello World!" wird angezeigt.  
    
8. Klicken Sie auf **OK** , um zurück zum Code-Editor von Visual Studio 2012, und klicken Sie im Menü **Debuggen** auf **Debuggen beenden** (oder drücken Strg + Alt + UNTBR). 
    
## <a name="getting-the-current-users-name"></a>Abrufen des aktuellen Benutzers namens

Im folgenden Beispiel erfahren Sie, wie Sie die [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) -Eigenschaft der [Benutzer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) -Klasse verwenden, um den Namen des aktuellen Benutzers abrufen, und füllen Sie den Wert eines **Textfeld** -Steuerelements mit einem Ereignishandler für das [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) -Ereignis. 
  
Füllen das **Textfeld** -Steuerelement erfolgt mithilfe einer Instanz der [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) -Klasse zum Schreiben des aktuellen Benutzers Name in der XML-Knoten, das an das Steuerelement gebunden ist. 
  
Zunächst wird die [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) -Eigenschaft der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse aufgerufen, um eine Instanz der [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) -Klasse abrufen, die das zugrunde liegende XML-Dokument des Formulars darstellt. Das [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) -Objekt ruft dann die [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) -Methode, die das **XPathNavigator** -Objekt erstellt und am Stammknoten der Hauptdatenquelle des Formulars positioniert. 
  
Die [SelectSingleNode](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.selectsinglenode%28v=vs.100%29.aspx) -Methode der **XPathNavigator** -Klasse aufgerufen, um Wählen Sie im Feld Employee in die Datenquelle des Formulars. Abschließend wird die [SetValue](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.setvalue%28v=vs.100%29.aspx) -Methode aufgerufen, um den Wert des Felds mit der [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) -Eigenschaft festzulegen. 
  
Weitere Informationen zum Arbeiten mit **System.Xml** in Formularvorlagen mit verwaltetem Code finden Sie unter [Arbeiten mit dem XPathNavigator und XPathNodeIterator-Klassen](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
### <a name="add-a-loading-event-handler"></a>Hinzufügen eines Loading-Ereignishandlers 

1. Öffnen Sie die Formularvorlage "HelloWorld", die Sie in der vorherigen exemplarischen Vorgehensweise im InfoPath-Designer erstellt haben.
    
2. Wählen Sie auf der Registerkarte **Ansicht** **Felder anzeigen**.
    
3. Klicken Sie mit der rechten Maustaste auf den Ordner **MyFields** , und klicken Sie dann auf **Hinzufügen**.
    
4. Klicken Sie im Feld **Name**Geben Sie Mitarbeiter, und klicken Sie dann auf **OK**.
    
5. Ziehen Sie im Feld Employee in die Ansicht. 
    
6. Klicken Sie auf der Registerkarte **Entwicklertools** auf **Loading-Ereignis**.
    
   Erstellt einen Ereignishandler für das [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) -Ereignis, und verschieben Sie den Fokus auf diesen Ereignishandler im Code-Editor. 
    
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

8. Wechseln Sie in der InfoPath-Formularentwurfsfenster, und klicken Sie dann auf die Schaltfläche **Vorschau** auf der Registerkarte **Start** auf Vorschau des Formulars anzuzeigen. 
    
   Das Feld Employee sollte sich mit Ihrem Benutzernamen automatisch ausfüllen. 
    
## <a name="next-steps"></a>Nächste Schritte

- Informationen zum Arbeiten mit Ereignishandlern für andere Steuerelemente und Ereignisse finden Sie unter [Hinzufügen eines Ereignishandlers](how-to-add-an-event-handler.md).
    
- Weitere Informationen zum Anzeigen einer Vorschau und Debuggen von Code in Formularvorlagen finden Sie unter [Vorschau und Debuggen von InfoPath-Formularvorlagen mit Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).
    
- Informationen zum Bereitstellen einer Formularvorlage mit verwaltetem Code finden Sie unter [Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md).
    
- Informationen zu den InfoPath-Objektmodell und allgemeine Programmieraufgaben in Formularvorlagen mit verwaltetem Code finden Sie unter [Grundlegendes zum InfoPath-Objektmodell und zu allgemeinen Entwickleraufgaben](understanding-the-infopath-object-model-and-common-developer-tasks.md)
    
## <a name="see-also"></a>Siehe auch

- [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)

