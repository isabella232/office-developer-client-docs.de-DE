---
title: Melden Sie sich Werte an ein Feld für das debugging
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5874dc28-1b10-48a3-8287-9474db0b7435
description: Beim Debuggen einer InfoPath-Formularvorlage ist es häufig sinnvoll, Werte direkt in einem Feld des Formulars zu protokollieren, um im Verlauf einer Sitzung zum Testen des Formulars eine Aufzeichnung der Daten zum Debugging zu erstellen. Nachfolgend wird erklärt, wie Sie ein mehrzeiliges Feld erstellen und anschließend dem Formularcode Hilfsfunktionen hinzufügen können, um das Protokollieren von Daten für das Debugging zu ermöglichen.
ms.openlocfilehash: f763e6b5d14fe5a5b4d9218af4acd0bc05a242af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790752"
---
# <a name="log-values-to-a-field-for-debugging"></a>Melden Sie sich Werte an ein Feld für das debugging

Beim Debuggen einer InfoPath-Formularvorlage ist es häufig sinnvoll, Werte direkt in einem Feld des Formulars zu protokollieren, um im Verlauf einer Sitzung zum Testen des Formulars eine Aufzeichnung der Daten zum Debugging zu erstellen. Nachfolgend wird erklärt, wie Sie ein mehrzeiliges Feld erstellen und anschließend dem Formularcode Hilfsfunktionen hinzufügen können, um das Protokollieren von Daten für das Debugging zu ermöglichen.
  
## <a name="create-a-multi-line-text-field"></a>Erstellen eines mehrzeiligen Textfelds

1. Das Formular ein **Textfeld** -Steuerelement hinzu, und Ändern der Größe, damit es mehrere Zeilen angezeigt werden. 
    
2. Mit der rechten Maustaste in des Textfelds, klicken Sie auf **Textfeldeigenschaften**, und klicken Sie dann auf auf der Registerkarte **Anzeige** das Kontrollkästchen **Mehrzeilig** . 
    
## <a name="add-helper-functions-to-log-debug-information-to-the-field"></a>Hinzufügen von Hilfsfunktionen zum Protokollieren von Debug-Informationen in das Feld

1. Auf der Registerkarte **Entwicklertools** auf **Code-Editor**, und speichern Sie die Formularvorlage aus, wenn Sie dazu aufgefordert werden.
    
2. Fügen Sie im Code-Editor der öffentlichen Klasse in der Formularcodedatei die folgenden drei Hilfsfunktionen hinzu.
    
   > [!IMPORTANT]
   > Stellen Sie sicher, dass Sie den Wert festlegen für aktualisieren die `debugFieldXpath` Variablen in der `AddToDebugField` Funktion an die richtige XPath-Ausdruck für das Feld gebunden, auf das Steuerelement, das Sie in der ersten Prozedur erstellt haben. 
  
    ```cs
        private void AddToDebugField(string valueToAdd)
        {
            // Update the value of debugFieldXpath to the XPath of the
            // multi-line field where you want to log debug information.
            string debugFieldXpath = "/my:myFields/my:field1";
            string headerLine = "----------------- " + DateTime.Now + 
                " -----------------" + "\r\n";
            SetDebugFieldValue(debugFieldXpath, headerLine + valueToAdd + 
                "\r\n" + GetDebugFieldValue(debugFieldXpath));
        }
        private string GetDebugFieldValue(string xpath)
        {
            return this.CreateNavigator().SelectSingleNode(xpath, 
                this.NamespaceManager).Value;
        }
        private void SetDebugFieldValue(string xpath, string value)
        {
            this.CreateNavigator().SelectSingleNode(xpath, 
                this.NamespaceManager).SetValue(value);
        }
    ```

    ```vb
        Private Sub AddToDebugField(ByVal valueToAdd As String)
            ' Update the value of debugFieldXpath to the XPath of the 
            ' multi-line field where you want to log debug information.
            Dim debugFieldXpath As String = "/my:myFields/my:field1"
            Dim headerLine As String = "----------------- " _
                &amp; DateTime.Now &amp; " -----------------" &amp; vbCrLf
            SetDebugFieldValue(debugFieldXpath, (headerLine &amp; valueToAdd &amp; vbCrLf) _
                &amp; GetDebugFieldValue(debugFieldXpath))
        End Sub
        Private Function GetDebugFieldValue(ByVal xpath As String) As String
            Return Me.CreateNavigator().SelectSingleNode(xpath, _
                Me.NamespaceManager).Value
        End Function
        Private Sub SetDebugFieldValue(ByVal xpath As String, ByVal value As String)
            Me.CreateNavigator().SelectSingleNode(xpath, _
                Me.NamespaceManager).SetValue(value)
        End Sub
    ```

> [!NOTE] 
> Bei der Verwendung von Visual Basic hinzufügen `Imports Microsoft.VisualBasic.Constants` auf die Richtlinien am oberen Rand der Formularcodedatei. 
  
## <a name="test-the-addtodebugfield-function"></a>Testen Sie die "addtodebugfield"-Funktion

1. Klicken Sie auf der Registerkarte **Entwicklertools** klicken Sie auf **Loading-Ereignis**, und fügen Sie dem Ereignishandler die folgende Codezeile.
    
   ```cs
    AddToDebugField("Form loaded");
   ```

   ```vb
    AddToDebugField("Form loaded")
   ```

2. Klicken Sie auf der Registerkarte **Entwicklertools** klicken Sie auf **View Switched-Ereignis**, und fügen Sie dem Ereignishandler die folgende Codezeile.
    
   ```cs
    AddToDebugField("View switched: " + this.CurrentView.ViewInfo.Name);
   ```

   ```vb
    AddToDebugField("View switched: " &amp; Me.CurrentView.ViewInfo.Name)
   ```

3. Klicken Sie auf der Registerkarte **Start** auf **Vorschau**.
    
   Das Feld Debug zwei Einträge sollte angezeigt werden: 1 zurück, der angibt, dass das Formular geladen wird und ein weiteres zurück, der den Namen der Ansicht angibt. In diesen Beispielen verwenden von Ereignishandlern für Ereignisse, die auftreten, wie das Formular geöffnet wird. Nachdem das Formular geladen ist, Sie können jedoch Aufrufen der `AddToDebugField` -Funktion aus anderen Ereignishandler neben jedem anderen Code im Kontext des Formulars ausgeführt. 
  

