---
title: Protokollieren von Werten in einem Feld für das Debugging
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5874dc28-1b10-48a3-8287-9474db0b7435
description: Beim Debuggen einer InfoPath-Formularvorlage ist es häufig sinnvoll, Werte direkt in einem Feld des Formulars zu protokollieren, um im Verlauf einer Sitzung zum Testen des Formulars eine Aufzeichnung der Daten zum Debugging zu erstellen. Nachfolgend wird erklärt, wie Sie ein mehrzeiliges Feld erstellen und anschließend dem Formularcode Hilfsfunktionen hinzufügen können, um das Protokollieren von Daten für das Debugging zu ermöglichen.
ms.openlocfilehash: 28f2a1ad3c13aefd9f898bdf397c9103df98d3c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303577"
---
# <a name="log-values-to-a-field-for-debugging"></a>Protokollieren von Werten in einem Feld für das Debugging

Beim Debuggen einer InfoPath-Formularvorlage ist es häufig sinnvoll, Werte direkt in einem Feld des Formulars zu protokollieren, um im Verlauf einer Sitzung zum Testen des Formulars eine Aufzeichnung der Daten zum Debugging zu erstellen. Nachfolgend wird erklärt, wie Sie ein mehrzeiliges Feld erstellen und anschließend dem Formularcode Hilfsfunktionen hinzufügen können, um das Protokollieren von Daten für das Debugging zu ermöglichen.
  
## <a name="create-a-multi-line-text-field"></a>Erstellen eines mehrzeiligen Textfelds

1. Fügen Sie dem Formular ein Steuerelement vom Typ **Textfeld** hinzu, und ändern Sie dessen Größe so, dass mehrere Zeilen angezeigt werden. 
    
2. Klicken Sie mit der rechten Maustaste auf **Textfeldeigenschaften**, und aktivieren Sie anschließend auf der Registerkarte **Anzeige** das Kontrollkästchen **Mehrzeilig**. 
    
## <a name="add-helper-functions-to-log-debug-information-to-the-field"></a>Hinzufügen von Hilfsfunktionen zum Protokollieren von Debuginformationen für das Feld

1. Klicken Sie auf der Registerkarte **Entwicklertools** auf **Code-Editor**, und speichern Sie anschließend nach Aufforderung die Formularvorlage.
    
2. Fügen Sie im Code-Editor der öffentlichen Klasse in der Formularcodedatei die folgenden drei Hilfsfunktionen hinzu.
    
   > [!IMPORTANT]
   > Stellen Sie sicher, dass Sie den Wert, der `debugFieldXpath` für die Variable `AddToDebugField` in der-Funktion festgelegt ist, auf den korrekten XPath-Ausdruck für das Feld aktualisieren, das an das Steuerelement gebunden ist, das Sie im ersten Verfahren erstellt haben. 
  
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
> Bei Verwendung von Visual Basic fügen `Imports Microsoft.VisualBasic.Constants` Sie den Direktiven am Anfang der Formular Codedatei hinzu. 
  
## <a name="test-the-addtodebugfield-function"></a>Testen der AddToDebugField-Funktion

1. Klicken Sie auf der Registerkarte **Entwicklertools** auf **Loading-Ereignis**, und fügen Sie anschließend dem Ereignishandler die folgende Codezeile hinzu.
    
   ```cs
    AddToDebugField("Form loaded");
   ```

   ```vb
    AddToDebugField("Form loaded")
   ```

2. Klicken Sie auf der Registerkarte **Entwicklertools** auf **View Switched-Ereignis**, und fügen Sie anschließend dem Ereignishandler die folgende Codezeile hinzu.
    
   ```cs
    AddToDebugField("View switched: " + this.CurrentView.ViewInfo.Name);
   ```

   ```vb
    AddToDebugField("View switched: " &amp; Me.CurrentView.ViewInfo.Name)
   ```

3. Klicken Sie auf der Registerkarte **Start** auf **Vorschau**.
    
   Im Feld für das Debugging müssen zwei Einträge angezeigt werden: einer zur Angabe, dass das Formular geladen wurde, und ein zweiter zur Angabe des Namens der Ansicht. In diesen Beispielen werden Ereignishandler für Ereignisse verwendet, die beim Öffnen des Formulars erfolgen. Nachdem das Formular geladen wurde, können Sie die `AddToDebugField` Funktion zusätzlich zu anderen Code, der im Kontext des Formulars läuft, auch von anderen Ereignishandlern aufrufen. 
  

