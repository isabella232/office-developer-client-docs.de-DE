---
title: 'Exemplarische Vorgehensweise: Erstellen und Debuggen einer einfachen Formularvorlage mithilfe des InfoPath-Objektmodells'
manager: soliver
ms.date: 01/13/2015
ms.audience: Developer
keywords:
- Formularvorlagen [infopath 2007], exemplarische Vorgehensweisen,Formularvorlagen [InfoPath 2007], Erstellen von InfoPath 2003-kompatiblen,InfoPath 2003-kompatiblen Formularvorlagen, exemplarische Vorgehensweisen
localization_priority: Normal
ms.assetid: 7658705f-c062-49a1-bea6-837737df2425
description: Dieses Thema enthält eine exemplarische Vorgehensweise zum Erstellen einer grundlegenden Formularvorlage für verwalteten InfoPath-Code, die mit dem infoPath 2003-kompatiblen Objektmodell von Microsoft funktioniert. Office.Interop.InfoPath.SemiTrust-Namespace.
ms.openlocfilehash: c559aedad5c62134c796196c63c1a84f70c4dc3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414340"
---
# <a name="walkthrough-create-and-debug-a-basic-form-template-using-the-infopath-object-model"></a>Exemplarische Vorgehensweise: Erstellen und Debuggen einer einfachen Formularvorlage mithilfe des InfoPath-Objektmodells

In diesem Thema wird eine exemplarische Vorgehensweise zum Erstellen einer einfachen Formularvorlage für verwalteten InfoPath-Code bereitgestellt, die mit dem InfoPath 2003-kompatiblen Objektmodell arbeitet, das vom [Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) bereitgestellt wird. 
  
## <a name="hello-world"></a>Hello World

Im folgenden Beispiel erfahren Sie, wie Sie mithilfe der [Alert-Methode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) des InfoPath 2003-kompatiblen Objektmodells ein einfaches Warnungsdialogfeld anzeigen. 
  
### <a name="create-a-new-infopath-form-template-that-works-with-the-infopath-2003-compatible-object-model"></a>Erstellen einer neuen InfoPath-Formularvorlage, die das InfoPath 2003-kompatible Objektmodell verwendet

1. Erstellen Sie eine neue Formularvorlage, die mit dem InfoPath 2003-kompatiblen Objektmodell funktioniert, wie unter [Create a Form Template Using the InfoPath 2003 Object Model beschrieben.](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)
    
2. Geben Sie dem Formularvorlagenprojekt den Namen HelloWorld, und speichern Sie es. 
    
   Das Projektsystem erstellt Code- und Projektdateien und öffnet dann eine leere Formularvorlage im InfoPath-Entwurfsmodus. Jetzt können Sie Ereignishandler hinzufügen.
    
### <a name="add-a-button-with-an-onclick-event-handler"></a>Hinzufügen einer Schaltfläche mit einem OnClick-Ereignishandler

1. Klicken Sie auf der Registerkarte **Start** im Abschnitt **Steuerelemente** auf das Steuerelement **Schaltfläche**, um dieses in die Ansicht einzufügen. 
    
2. Klicken Sie mit der rechten Maustaste auf das Steuerelement, und klicken Sie dann auf **Schaltflächeneigenschaften**.
    
3. Ändern Sie **die Bezeichnung** in Warnung.
    
4. Ändern Sie die **ID** in AlertID.
    
5. Klicken Sie auf **Formularcode bearbeiten**.
    
   Ein Ereignishandlergerüst für das [OnClick-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) wird erstellt, und der Fokus wird in Visual Studio 2012 in den Code-Editor verlagert. Weitere Informationen zum Arbeiten mit Ereignishandlern finden Sie unter [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md). 
    
   Jetzt können Sie dem Ereignishandler für die Schaltfläche Formularcode hinzufügen.
    
### <a name="add-form-code-to-the-event-handler"></a>Hinzufügen von Formularcode zum Ereignishandler

1. Geben Sie im **OnClick**-Ereignishandler den folgenden Code ein: 
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   Beachten Sie, dass nach der Eingabe jedes Punktes in der Codezeile eine Microsoft IntelliSense-Dropdownliste angezeigt wird. Der gesamte Ereignishandler sollte wie folgt aussehen:
    
   ```cs
    [InfoPathEventHandler(MatchPath="AlertID", EventType=InfoPathEventType.OnClick)]
    public void AlertID_OnClick(DocActionEvent e)
    {
        thisXDocument.UI.Alert("Hello World!");
    }
   ```

   ```vb
    <InfoPathEventHandler(MatchPath:="AlertID", EventType:=InfoPathEventType.OnClick)>
    Public Sub AlertID_OnClick(ByVal e As DocActionEvent)
        thisXDocument.UI.Alert("Hello World!")
    End Sub
   ```

   > [!NOTE]
   > Alternativ zur Verwendung der **Alert**-Methode können Sie die **MessageBox.Show**-Methode des **System.Windows.Forms**-Namespace verwenden, um ein Meldungsfeld anzuzeigen. Dazu müssen Sie einen Verweis auf das System hinzufügen. Windows. Formular assembly, hinzufügen oder zu den Direktiven am Anfang der Codedatei, und geben Sie dann eine Codezeile wie `using System.Windows.Forms;` `Imports System.Windows.Forms` die folgende ein:`MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`
  
2. Wechseln Sie zum InfoPath-Entwurfsmodusfenster, und klicken Sie dann auf der Registerkarte **Start** auf die Schaltfläche **Vorschau**. 
    
3. Klicken Sie imVorschaufenster auf die Schaltfläche **Alert**. 
    
   Ein Meldungsfeld mit dem Text "Hello World!" wird angezeigt.
    
   Im nächsten Verfahren wird gezeigt, wie Sie dem Formularcode Haltepunkte für das Debuggen hinzufügen können.
    
### <a name="debug-form-code"></a>Debuggen von Formularcode

1. Klicken Sie im Code-Editor auf die graue Leiste links neben der Zeile:
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   Ein roter Kreis wird angezeigt, und die Codezeile wird hervorgehoben, um darauf hinzuweisen, dass die Laufzeit an diesem Haltepunkt im Formularcode angehalten wird.
    
2. Klicken Sie im Menü **Debuggen** auf **Debuggen starten** (oder drücken Sie F5). 
    
3. Klicken Sie imVorschaufenster von InfoPath auf die Schaltfläche **Alert**. 
    
   Der Fokus wechselt zum Code-Editor, und die Haltepunktlinie wird hervorgehoben.
    
4. Klicken Sie im Menü **Debuggen** auf **Prozedurschritt** (oder drücken Sie UMSCHALT+F8), um das schrittweise Durchlaufen des Codes fortzusetzen. 
    
   Der Code der **Alert-Methode** wird ausgeführt, und die "Hello World!" warnung wird im InfoPath **Preview-Fenster** angezeigt. 
    
## <a name="getting-the-current-users-name"></a>Abrufen des aktuellen Benutzernamens

Mithilfe der .NET Framework-Klassen können Sie auf Funktionalität zugreifen, die in Skripts nicht ohne weiteres verfügbar war. In diesem Beispiel erfahren Sie, wie der Name des aktuellen Benutzers über die .NET Framework-Klassen abgerufen werden kann.
  
### <a name="add-an-onload-event-handler"></a>Hinzufügen eines OnLoad-Ereignishandlers

1. Öffnen Sie das InfoPath-Projekt "HelloWorld", das Sie zuvor erstellt haben.
    
2. Klicken Sie auf der Registerkarte **Ansicht** auf **Felder anzeigen**.
    
3. Klicken Sie mit der rechten Maustaste auf den Knoten **myFields**, und klicken Sie dann auf **Hinzufügen**.
    
4. Geben Sie **employee** im Feld **Name** ein, und klicken Sie dann auf **OK**.
    
5. Ziehen Sie den Knoten **employee** in die Ansicht. 
    
6. Klicken Sie auf der Registerkarte **Entwicklertools** auf **On Load-Ereignis**.
    
   Dadurch wird ein Ereignishandler für das [OnLoad-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) erstellt, und der Fokus wird in den Code-Editor verlagert. Der Code in diesem Ereignishandler wird bei jedem Laden des Formulars aufgerufen. Im nächsten Verfahren wird gezeigt, wie dem Ereignishandler Formularcode zum Abrufen des Benutzernamens hinzugefügt wird. 
    
### <a name="add-form-code"></a>Hinzufügen von Formularcode 

1. Geben Sie im **OnLoad**-Ereignishandler den folgenden Code ein: 
    
   ```cs
    // Store an XML DOM node as a local variable.
    IXMLDOMNode nodeEmployee = thisXDocument.DOM.selectSingleNode("my:myFields/my:employee");
    if(nodeEmployee != null)
    {
        if(nodeEmployee.text == "")
        {
        // If the employee name is blank when the form is loaded, 
        // populate the employee node with the current user name.
        nodeEmployee.text = System.Environment.UserName;
        }
    }
   ```

   ```vb
    // Store an XML DOM node as a local variable.
    Dim nodeEmployee As IXMLDOMNode
    nodeEmployee = thisXDocument.DOM.selectSingleNode("my:myFields/my:employee");
    If Not(nodeEmployee Is Nothing) Then
        If(nodeEmployee.text = "") Then
        // If the employee name is blank when the form is loaded, 
        // populate the employee node with the current user name.
        nodeEmployee.text = System.Environment.UserName
        End If
    End If
   ```

2. Kompilieren Sie das Formular, und zeigen Sie eine Vorschau davon an.
    
   Das Textfeld employee sollte jetzt mit Ihrem Benutzername aufgefüllt sein. 
    
Informationen zum Bereitstellen einer Formularvorlage für verwalteten Code finden Sie unter [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md). Informationen zum InfoPath-Objektmodell und zu allgemeinen Programmieraufgaben in Formularvorlagen für verwalteten Code, die mit dem InfoPath 2003-kompatiblen Objektmodell funktionieren, finden Sie unter [Understanding the InfoPath 2003 Object Model](understanding-the-infopath-2003-object-model.md). 
  
## <a name="see-also"></a>Siehe auch

- [Initialisierungs- und Bereinigungscode mit dem InfoPath 2003-Objektmodell](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
- [InfoPath 2003-kompatible Objektmodelle](infopath-2003-compatible-object-models.md)
- [Hinzufügen eines Ereignishandlers mithilfe des InfoPath 2003-Objektmodells](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

