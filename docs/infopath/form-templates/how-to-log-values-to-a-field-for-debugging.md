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
# <a name="log-values-to-a-field-for-debugging"></a><span data-ttu-id="f895f-104">Melden Sie sich Werte an ein Feld für das debugging</span><span class="sxs-lookup"><span data-stu-id="f895f-104">Log values to a field for debugging</span></span>

<span data-ttu-id="f895f-p102">Beim Debuggen einer InfoPath-Formularvorlage ist es häufig sinnvoll, Werte direkt in einem Feld des Formulars zu protokollieren, um im Verlauf einer Sitzung zum Testen des Formulars eine Aufzeichnung der Daten zum Debugging zu erstellen. Nachfolgend wird erklärt, wie Sie ein mehrzeiliges Feld erstellen und anschließend dem Formularcode Hilfsfunktionen hinzufügen können, um das Protokollieren von Daten für das Debugging zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f895f-p102">When debugging an InfoPath form template, it is often useful to log values directly into a field in the form to create a record of debug data during a session of testing the form. The following procedures show how to create a multi-line field, and then add helper functions to the form code that enable you log debug data into that field.</span></span>
  
## <a name="create-a-multi-line-text-field"></a><span data-ttu-id="f895f-107">Erstellen eines mehrzeiligen Textfelds</span><span class="sxs-lookup"><span data-stu-id="f895f-107">Create a multi-line text field</span></span>

1. <span data-ttu-id="f895f-108">Das Formular ein **Textfeld** -Steuerelement hinzu, und Ändern der Größe, damit es mehrere Zeilen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f895f-108">Add a **Text Box** control to the form, and then resize it so that it can display multiple lines.</span></span> 
    
2. <span data-ttu-id="f895f-109">Mit der rechten Maustaste in des Textfelds, klicken Sie auf **Textfeldeigenschaften**, und klicken Sie dann auf auf der Registerkarte **Anzeige** das Kontrollkästchen **Mehrzeilig** .</span><span class="sxs-lookup"><span data-stu-id="f895f-109">Right-click the text box, click **Text Box Properties**, and then click the **Multi-line** check box on the **Display** tab.</span></span> 
    
## <a name="add-helper-functions-to-log-debug-information-to-the-field"></a><span data-ttu-id="f895f-110">Hinzufügen von Hilfsfunktionen zum Protokollieren von Debug-Informationen in das Feld</span><span class="sxs-lookup"><span data-stu-id="f895f-110">Add helper functions to log debug information to the field</span></span>

1. <span data-ttu-id="f895f-111">Auf der Registerkarte **Entwicklertools** auf **Code-Editor**, und speichern Sie die Formularvorlage aus, wenn Sie dazu aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="f895f-111">On the **Developer** tab, click **Code Editor**, and then save the form template if you are prompted.</span></span>
    
2. <span data-ttu-id="f895f-112">Fügen Sie im Code-Editor der öffentlichen Klasse in der Formularcodedatei die folgenden drei Hilfsfunktionen hinzu.</span><span class="sxs-lookup"><span data-stu-id="f895f-112">In the Code Editor, add the following three helper functions to the public class in the form code file.</span></span>
    
   > [!IMPORTANT]
   > <span data-ttu-id="f895f-113">Stellen Sie sicher, dass Sie den Wert festlegen für aktualisieren die `debugFieldXpath` Variablen in der `AddToDebugField` Funktion an die richtige XPath-Ausdruck für das Feld gebunden, auf das Steuerelement, das Sie in der ersten Prozedur erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="f895f-113">Make sure that you update the value set for the  `debugFieldXpath` variable in the  `AddToDebugField` function to the correct XPath expression for the field bound to the control that you created in the first procedure.</span></span> 
  
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
> <span data-ttu-id="f895f-114">Bei der Verwendung von Visual Basic hinzufügen `Imports Microsoft.VisualBasic.Constants` auf die Richtlinien am oberen Rand der Formularcodedatei.</span><span class="sxs-lookup"><span data-stu-id="f895f-114">When using Visual Basic, add  `Imports Microsoft.VisualBasic.Constants` to the directives at the top of the form code file.</span></span> 
  
## <a name="test-the-addtodebugfield-function"></a><span data-ttu-id="f895f-115">Testen Sie die "addtodebugfield"-Funktion</span><span class="sxs-lookup"><span data-stu-id="f895f-115">Test the AddToDebugField function</span></span>

1. <span data-ttu-id="f895f-116">Klicken Sie auf der Registerkarte **Entwicklertools** klicken Sie auf **Loading-Ereignis**, und fügen Sie dem Ereignishandler die folgende Codezeile.</span><span class="sxs-lookup"><span data-stu-id="f895f-116">On the **Developer** tab, click **Loading Event**, and then add the following line of code to the event handler.</span></span>
    
   ```cs
    AddToDebugField("Form loaded");
   ```

   ```vb
    AddToDebugField("Form loaded")
   ```

2. <span data-ttu-id="f895f-117">Klicken Sie auf der Registerkarte **Entwicklertools** klicken Sie auf **View Switched-Ereignis**, und fügen Sie dem Ereignishandler die folgende Codezeile.</span><span class="sxs-lookup"><span data-stu-id="f895f-117">On the **Developer** tab, click **View Switched Event**, and then add the following line of code to the event handler.</span></span>
    
   ```cs
    AddToDebugField("View switched: " + this.CurrentView.ViewInfo.Name);
   ```

   ```vb
    AddToDebugField("View switched: " &amp; Me.CurrentView.ViewInfo.Name)
   ```

3. <span data-ttu-id="f895f-118">Klicken Sie auf der Registerkarte **Start** auf **Vorschau**.</span><span class="sxs-lookup"><span data-stu-id="f895f-118">On the **Home** tab, click **Preview**.</span></span>
    
   <span data-ttu-id="f895f-119">Das Feld Debug zwei Einträge sollte angezeigt werden: 1 zurück, der angibt, dass das Formular geladen wird und ein weiteres zurück, der den Namen der Ansicht angibt.</span><span class="sxs-lookup"><span data-stu-id="f895f-119">The debug field should display two entries: one indicating that the form is loaded, and another indicating the name of the view.</span></span> <span data-ttu-id="f895f-120">In diesen Beispielen verwenden von Ereignishandlern für Ereignisse, die auftreten, wie das Formular geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="f895f-120">These examples use event handlers for events that occur as the form is opened.</span></span> <span data-ttu-id="f895f-121">Nachdem das Formular geladen ist, Sie können jedoch Aufrufen der `AddToDebugField` -Funktion aus anderen Ereignishandler neben jedem anderen Code im Kontext des Formulars ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f895f-121">However, after the form is loaded, you can call the  `AddToDebugField` function from other event handlers in addition to any other code running in the context of the form.</span></span> 
  

