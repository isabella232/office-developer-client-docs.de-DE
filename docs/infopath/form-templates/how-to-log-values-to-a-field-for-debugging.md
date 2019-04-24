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
# <a name="log-values-to-a-field-for-debugging"></a><span data-ttu-id="28337-104">Protokollieren von Werten in einem Feld für das Debugging</span><span class="sxs-lookup"><span data-stu-id="28337-104">Log values to a field for debugging</span></span>

<span data-ttu-id="28337-p102">Beim Debuggen einer InfoPath-Formularvorlage ist es häufig sinnvoll, Werte direkt in einem Feld des Formulars zu protokollieren, um im Verlauf einer Sitzung zum Testen des Formulars eine Aufzeichnung der Daten zum Debugging zu erstellen. Nachfolgend wird erklärt, wie Sie ein mehrzeiliges Feld erstellen und anschließend dem Formularcode Hilfsfunktionen hinzufügen können, um das Protokollieren von Daten für das Debugging zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="28337-p102">When debugging an InfoPath form template, it is often useful to log values directly into a field in the form to create a record of debug data during a session of testing the form. The following procedures show how to create a multi-line field, and then add helper functions to the form code that enable you log debug data into that field.</span></span>
  
## <a name="create-a-multi-line-text-field"></a><span data-ttu-id="28337-107">Erstellen eines mehrzeiligen Textfelds</span><span class="sxs-lookup"><span data-stu-id="28337-107">Create a multi-line text field</span></span>

1. <span data-ttu-id="28337-108">Fügen Sie dem Formular ein Steuerelement vom Typ **Textfeld** hinzu, und ändern Sie dessen Größe so, dass mehrere Zeilen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="28337-108">Add a **Text Box** control to the form, and then resize it so that it can display multiple lines.</span></span> 
    
2. <span data-ttu-id="28337-109">Klicken Sie mit der rechten Maustaste auf **Textfeldeigenschaften**, und aktivieren Sie anschließend auf der Registerkarte **Anzeige** das Kontrollkästchen **Mehrzeilig**.</span><span class="sxs-lookup"><span data-stu-id="28337-109">Right-click the text box, click **Text Box Properties**, and then click the **Multi-line** check box on the **Display** tab.</span></span> 
    
## <a name="add-helper-functions-to-log-debug-information-to-the-field"></a><span data-ttu-id="28337-110">Hinzufügen von Hilfsfunktionen zum Protokollieren von Debuginformationen für das Feld</span><span class="sxs-lookup"><span data-stu-id="28337-110">Add helper functions to log debug information to the field</span></span>

1. <span data-ttu-id="28337-111">Klicken Sie auf der Registerkarte **Entwicklertools** auf **Code-Editor**, und speichern Sie anschließend nach Aufforderung die Formularvorlage.</span><span class="sxs-lookup"><span data-stu-id="28337-111">On the **Developer** tab, click **Code Editor**, and then save the form template if you are prompted.</span></span>
    
2. <span data-ttu-id="28337-112">Fügen Sie im Code-Editor der öffentlichen Klasse in der Formularcodedatei die folgenden drei Hilfsfunktionen hinzu.</span><span class="sxs-lookup"><span data-stu-id="28337-112">In the Code Editor, add the following three helper functions to the public class in the form code file.</span></span>
    
   > [!IMPORTANT]
   > <span data-ttu-id="28337-113">Stellen Sie sicher, dass Sie den Wert, der `debugFieldXpath` für die Variable `AddToDebugField` in der-Funktion festgelegt ist, auf den korrekten XPath-Ausdruck für das Feld aktualisieren, das an das Steuerelement gebunden ist, das Sie im ersten Verfahren erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="28337-113">Make sure that you update the value set for the  `debugFieldXpath` variable in the  `AddToDebugField` function to the correct XPath expression for the field bound to the control that you created in the first procedure.</span></span> 
  
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
> <span data-ttu-id="28337-114">Bei Verwendung von Visual Basic fügen `Imports Microsoft.VisualBasic.Constants` Sie den Direktiven am Anfang der Formular Codedatei hinzu.</span><span class="sxs-lookup"><span data-stu-id="28337-114">When using Visual Basic, add  `Imports Microsoft.VisualBasic.Constants` to the directives at the top of the form code file.</span></span> 
  
## <a name="test-the-addtodebugfield-function"></a><span data-ttu-id="28337-115">Testen der AddToDebugField-Funktion</span><span class="sxs-lookup"><span data-stu-id="28337-115">Test the AddToDebugField function</span></span>

1. <span data-ttu-id="28337-116">Klicken Sie auf der Registerkarte **Entwicklertools** auf **Loading-Ereignis**, und fügen Sie anschließend dem Ereignishandler die folgende Codezeile hinzu.</span><span class="sxs-lookup"><span data-stu-id="28337-116">On the **Developer** tab, click **Loading Event**, and then add the following line of code to the event handler.</span></span>
    
   ```cs
    AddToDebugField("Form loaded");
   ```

   ```vb
    AddToDebugField("Form loaded")
   ```

2. <span data-ttu-id="28337-117">Klicken Sie auf der Registerkarte **Entwicklertools** auf **View Switched-Ereignis**, und fügen Sie anschließend dem Ereignishandler die folgende Codezeile hinzu.</span><span class="sxs-lookup"><span data-stu-id="28337-117">On the **Developer** tab, click **View Switched Event**, and then add the following line of code to the event handler.</span></span>
    
   ```cs
    AddToDebugField("View switched: " + this.CurrentView.ViewInfo.Name);
   ```

   ```vb
    AddToDebugField("View switched: " &amp; Me.CurrentView.ViewInfo.Name)
   ```

3. <span data-ttu-id="28337-118">Klicken Sie auf der Registerkarte **Start** auf **Vorschau**.</span><span class="sxs-lookup"><span data-stu-id="28337-118">On the **Home** tab, click **Preview**.</span></span>
    
   <span data-ttu-id="28337-119">Im Feld für das Debugging müssen zwei Einträge angezeigt werden: einer zur Angabe, dass das Formular geladen wurde, und ein zweiter zur Angabe des Namens der Ansicht.</span><span class="sxs-lookup"><span data-stu-id="28337-119">The debug field should display two entries: one indicating that the form is loaded, and another indicating the name of the view.</span></span> <span data-ttu-id="28337-120">In diesen Beispielen werden Ereignishandler für Ereignisse verwendet, die beim Öffnen des Formulars erfolgen.</span><span class="sxs-lookup"><span data-stu-id="28337-120">These examples use event handlers for events that occur as the form is opened.</span></span> <span data-ttu-id="28337-121">Nachdem das Formular geladen wurde, können Sie die `AddToDebugField` Funktion zusätzlich zu anderen Code, der im Kontext des Formulars läuft, auch von anderen Ereignishandlern aufrufen.</span><span class="sxs-lookup"><span data-stu-id="28337-121">However, after the form is loaded, you can call the  `AddToDebugField` function from other event handlers in addition to any other code running in the context of the form.</span></span> 
  

