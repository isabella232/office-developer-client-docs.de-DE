---
title: 'Exemplarische vorGehensWeise: Erstellen und Debuggen einer einfachen Formularvorlage mit dem InfoPath-Objektmodell'
manager: soliver
ms.date: 01/13/2015
ms.audience: Developer
keywords:
- Formularvorlagen [InfoPath 2007], Exemplarische Vorgehensweisen, Formularvorlagen [InfoPath 2007], Erstellen von InfoPath 2003-kompatiblen, InfoPath 2003-kompatiblen Formularvorlagen, Exemplarische Vorgehensweisen
localization_priority: Normal
ms.assetid: 7658705f-c062-49a1-bea6-837737df2425
description: Dieses Thema bietet eine exemplarische Vorgehensweise zum Erstellen einer einfachen InfoPath-Formularvorlage mit verwaltetem Code, die mit dem InfoPath 2003-kompatiblen Objektmodell verwendet wird, das vom Microsoft. Office. Interop. InfoPath. SemiTrust-Namespace bereitgestellt wird.
ms.openlocfilehash: c559aedad5c62134c796196c63c1a84f70c4dc3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414340"
---
# <a name="walkthrough-create-and-debug-a-basic-form-template-using-the-infopath-object-model"></a>Exemplarische vorGehensWeise: Erstellen und Debuggen einer einfachen Formularvorlage mit dem InfoPath-Objektmodell

Dieses Thema bietet eine exemplarische Vorgehensweise zum Erstellen einer einfachen InfoPath-Formularvorlage mit verwaltetem Code, die mit dem InfoPath 2003-kompatiblen Objektmodell verwendet wird, das vom [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace bereitgestellt wird. 
  
## <a name="hello-world"></a>Hello World

Im folgenden Beispiel erfahren Sie, wie Sie mithilfe der [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) -Methode des InfoPath 2003-kompatiblen Objektmodells ein einfaches Warnungsdialogfeld anzeigen. 
  
### <a name="create-a-new-infopath-form-template-that-works-with-the-infopath-2003-compatible-object-model"></a>Erstellen einer neuen InfoPath-Formularvorlage, die das InfoPath 2003-kompatible Objektmodell verwendet

1. Erstellen Sie eine neue Formularvorlage, die mit dem InfoPath 2003-kompatiblen Objektmodell verwendet werden kann, wie unter [Erstellen einer Formularvorlage mit dem infopath 2003-Objektmodell](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)beschrieben.
    
2. Geben Sie dem Formularvorlagenprojekt den Namen HelloWorld, und speichern Sie es. 
    
   Das Projektsystem erstellt Code- und Projektdateien und öffnet dann eine leere Formularvorlage im InfoPath-Entwurfsmodus. Jetzt können Sie Ereignishandler hinzufügen.
    
### <a name="add-a-button-with-an-onclick-event-handler"></a>Hinzufügen einer Schaltfläche mit einem OnClick-Ereignishandler

1. Klicken Sie auf der Registerkarte **Start** im Abschnitt **Steuerelemente** auf das Steuerelement **Schaltfläche**, um dieses in die Ansicht einzufügen. 
    
2. Klicken Sie mit der rechten Maustaste auf das Steuerelement, und klicken Sie dann auf **Schaltflächeneigenschaften**.
    
3. Ändern Sie die **Bezeichnung** in Alert.
    
4. Ändern Sie die ID in die Warnungs **Kennung** .
    
5. Klicken Sie auf **Formularcode bearbeiten**.
    
   Ein Ereignishandler-Skelett für [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) das OnClick-Ereignis wird erstellt, und der Fokus wechselt zum Code-Editor in Visual Studio 2012. Weitere Informationen zum Arbeiten mit Ereignishandlern finden Sie unter [Hinzufügen eines Ereignishandlers mit dem InfoPath-Objektmodell 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md). 
    
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
   > Alternativ zur Verwendung der **Alert**-Methode können Sie die **MessageBox.Show**-Methode des **System.Windows.Forms**-Namespace verwenden, um ein Meldungsfeld anzuzeigen. Zu diesem Zweck müssen Sie einen Verweis auf die System. Windows. Forms-Assembly, hinzufügen `using System.Windows.Forms;` oder `Imports System.Windows.Forms` zu den Direktiven am Anfang der Codedatei hinzufügen und dann eine Codezeile wie die folgende eingeben:`MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`
  
2. Wechseln Sie zum InfoPath-Entwurfsmodusfenster, und klicken Sie dann auf der Registerkarte **Start** auf die Schaltfläche **Vorschau**. 
    
3. Klicken Sie im**** Vorschaufenster auf die Schaltfläche **Alert**. 
    
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
    
3. Klicken Sie im**** Vorschaufenster von InfoPath auf die Schaltfläche **Alert**. 
    
   Der Fokus wechselt zum Code-Editor, und die Haltepunktlinie wird hervorgehoben.
    
4. Klicken Sie im Menü **Debuggen** auf **Prozedurschritt** (oder drücken Sie UMSCHALT+F8), um das schrittweise Durchlaufen des Codes fortzusetzen. 
    
   Der Code der **Warnungs** Methode wird ausgeführt, und die "Hello World!" Alert wird im InfoPath- **Vorschaufenster** angezeigt. 
    
## <a name="getting-the-current-users-name"></a>Abrufen des aktuellen Benutzernamens

Mithilfe der .NET Framework-Klassen können Sie auf Funktionalität zugreifen, die in Skripts nicht ohne weiteres verfügbar war. In diesem Beispiel erfahren Sie, wie der Name des aktuellen Benutzers über die .NET Framework-Klassen abgerufen werden kann.
  
### <a name="add-an-onload-event-handler"></a>Hinzufügen eines OnLoad-Ereignishandlers

1. Öffnen Sie das InfoPath-Projekt "HelloWorld", das Sie zuvor erstellt haben.
    
2. Klicken Sie auf der Registerkarte **Ansicht** auf **Felder anzeigen**.
    
3. Klicken Sie mit der rechten Maustaste auf den Knoten **myFields**, und klicken Sie dann auf **Hinzufügen**.
    
4. Geben Sie **employee** im Feld **Name** ein, und klicken Sie dann auf **OK**.
    
5. Ziehen Sie den Knoten **employee** in die Ansicht. 
    
6. Klicken Sie auf der Registerkarte **Entwicklertools** auf **On Load-Ereignis**.
    
   Dadurch wird ein Ereignishandler für das [Onlade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) -Ereignis erstellt, und der Fokus wechselt zum Code-Editor. Der Code in diesem Ereignishandler wird bei jedem Laden des Formulars aufgerufen. Im nächsten Verfahren wird gezeigt, wie dem Ereignishandler Formularcode zum Abrufen des Benutzernamens hinzugefügt wird. 
    
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
    
Informationen zum Bereitstelleneiner Formularvorlage mit verwaltetem Code finden Sie unter [Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md). Informationen zum InfoPath-Objektmodell und zu allgemeinen Programmieraufgaben in Formularvorlagen mit verwaltetem Code, die mit dem InfoPath 2003-kompatiblen Objektmodell arbeiten, finden Sie unter [Understanding the infopath 2003 Object Model](understanding-the-infopath-2003-object-model.md). 
  
## <a name="see-also"></a>Siehe auch

- [Initialisierungs- und Bereinigungscode mit dem InfoPath 2003-Objektmodell](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
- [InfoPath 2003-kompatible Objektmodelle](infopath-2003-compatible-object-models.md)
- [Hinzufügen eines Ereignishandlers mit dem InfoPath-Objektmodell 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

