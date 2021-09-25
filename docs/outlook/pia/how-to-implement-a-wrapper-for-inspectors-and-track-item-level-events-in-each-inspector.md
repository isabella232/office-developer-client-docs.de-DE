---
title: Implementieren eines Wrappers für Prüfungen und Nachverfolgung von Ereignissen auf Elementebene in jedem Inspektor
TOCTitle: Implement a wrapper for inspectors and track item-level events in each inspector
ms:assetid: 8021dd2b-c36c-492b-b281-783e85140ad8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184620(v=office.15)
ms:contentKeyID: 55119854
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7d311b6a119704d8ae0c9f23a2c35498f2c7d594
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616292"
---
# <a name="implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector"></a>Implementieren eines Wrappers für Prüfungen und Nachverfolgung von Ereignissen auf Elementebene in jedem Inspektor

Dieses Thema enthält zwei Codebeispiele, die zeigen, wie ein Wrapper für eine [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) -Auflistung implementiert und dieser Wrapper zur Nachverfolgung von Ereignissen auf Elementebene in jedem [Inspector](https://msdn.microsoft.com/library/bb647744\(v=office.15\)) -Objekt in der Auflistung verwendet wird.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

In den folgenden beiden Codebeispielen werden die Connect- und OutlookInspector-Klassen implementiert. Das erste Codebeispiel betrifft Methoden und Ereignishandler, die Sie in die Connect-Klasse einschließen, um einen Wrapper für eine **Inspectors**-Auflistung zu implementieren. Das zweite Codebeispiel betrifft eine einfache Implementierung der **OutlookInspector**-Klasse.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

Im folgenden Codebeispiel tritt ein [NewInspector(Inspector)](https://msdn.microsoft.com/library/bb610594\(v=office.15\))-Ereignis auf, nachdem ein neues Inspektorfenster erstellt wurde und bevor es angezeigt wird. Mit einer Benutzeraktion wird auch möglicherweise ein neues Inspektorfenster erstellt. Es wird eine Instanzvariable auf Klassenebene namens „Inspectors“ in der **Connect**-Klasse deklariert, und ein **NewInspector**-Ereignis wird angebunden. 

In der inspectors\_NewInspector-Methode prüft die **FindOutlookInspector**-Methode, ob ein neues Inspektorfenster bereits in der InspectorWindows-Liste enthalten. Wenn FindOutlookInspector das **Inspector**-Objekt im inspectorWindows nicht findet, fügt die **AddInspector**-Methode eine Instanz der **OutlookInspector**-Klasse zu inspectorWindows hinzu. Sie können die **OutlookInspector**-Klasse verwenden, um Ereignisse für dieses spezielle Inspektorfenster auszulösen. Die Implementierung der **OutlookInspector**-Klasse wird im zweiten Codebeispiel gezeigt.

```csharp
class Connect
{
    // Connect class-level Instance Variables
    // Outlook inspectors collection
    private Outlook.Inspectors inspectors;

    // Collection of tracked inspector windows              
    private List<OutlookInspector> inspectorWindows;    

    // Hook up NewInspector event
    inspectors.NewInspector += new 
        Outlook.InspectorsEvents_NewInspectorEventHandler(
        inspectors_NewInspector);

    // NewInspector event creates new instance of OutlookInspector
    void inspectors_NewInspector(Outlook.Inspector Inspector)
    {
        // Check to see if this is a new window you don't
        // already track
        OutlookInspector existingWindow = 
            FindOutlookInspector(Inspector);
        if (existingWindow == null)
        {
            AddInspector(Inspector);
        }
    }

    // Adds an instance of **OutlookInspector** class
    private void AddInspector(Outlook.Inspector inspector)
    {
        OutlookInspector window = new OutlookInspector(inspector);
        window.Close +=
            new EventHandler(WrappedInspectorWindow_Close);
    }

    // Looks up the window wrapper for a given Inspector 
    // window object
    private OutlookInspector FindOutlookInspector(object window)
    {
        foreach (OutlookInspector inspector in inspectorWindows)
        {
            if (inspector.Window == window)
            {
                return inspector;
            }
        }
        return null;
    }
}
```

Das folgende Codebeispiel stellt eine Implementierung der **OutlookInspector**-Klasse dar. Diese Klasse dient zum Auslösen von Ereignissen für das Inspektorfenster aus dem vorherigen Beispiel. Es können mehrere Inspektorfenster gleichzeitig geöffnet sein. Ereignisse auf Elementebene wie [Open](https://msdn.microsoft.com/library/bb644296\(v=office.15\)), [PropertyChange](https://msdn.microsoft.com/library/bb647794\(v=office.15\)) und [CustomPropertyChange](https://msdn.microsoft.com/library/bb645015\(v=office.15\)) werden durch Einbinden in diesen Klassenkonstruktor nachverfolgt. Ein [Close](https://msdn.microsoft.com/library/bb645009\(v=office.15\))-Ereignis für ein [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\))-Objekt ist auch in diesen Klassenkonstruktor eingebunden. Sie können bei Bedarf andere Elementinstanzvariablen auf Klassenebene definieren. Alle in den OutlookInspector-Konstruktor eingebundenen Ereignisse werden im OutlookInspectorWindow\_Close-Ereignishandler wieder getrennt.

Beachten Sie, dass auf Objektmodellebene ein **Outlook-Inspektor**-Objekt nicht für einen Outlook-Elementtyp spezifisch ist. In diesem Codebeispiel wird die OutlookItem-Hilfsklasse verwendet, die unter [Erstellen einer Hilfsklasse zum Zugriff auf allgemeine Member von Outlook-Elementen](how-to-create-a-helper-class-to-access-common-outlook-item-members.md) definiert ist, um die OutlookItem.Class-Eigenschaft aufzurufen, um die Nachrichtenklasse des aktuellen Elements im Inspector zu prüfen, ohne anzunehmen, dass es sich bei dem Element um ein Kontaktelement handelt.

```csharp
// This class tracks the state of an Outlook Inspector window 
// and ensures that what happens in this window is handled correctly.
class OutlookInspector
{
    // OutlookInspector class-level instance variables 
    // wrapped window object
    private Outlook.Inspector m_Window;             

    // Use these instance variables to handle item-level events
    // wrapped MailItem
    private Outlook.MailItem m_Mail;    
    // wrapped AppointmentItem        
    private Outlook.AppointmentItem m_Appointment;  
    // wrapped ContactItem
    private Outlook.ContactItem m_Contact;
    // wrapped TaskItem      
    private Outlook.TaskItem m_Task;             

    // OutlookInspector constructor
    public OutlookInspector(Outlook.Inspector inspector)
    {
        m_Window = inspector;

        // Hook up the close event
        ((Outlook.InspectorEvents_Event)inspector).Close +=
            new Outlook.InspectorEvents_CloseEventHandler(
            OutlookInspectorWindow_Close);

        // Hook up item-level events as needed
        OutlookItem olItem = new OutlookItem(inspector.CurrentItem);
        if(olItem.Class==Outlook.OlObjectClass.olContact)
        {
            m_Contact = olItem.InnerObject as Outlook.ContactItem;
            m_Contact.Open +=
                new Outlook.ItemEvents_10_OpenEventHandler(
                m_Contact_Open);
            m_Contact.PropertyChange +=
                new Outlook.ItemEvents_10_PropertyChangeEventHandler(
                m_Contact_PropertyChange);
            m_Contact.CustomPropertyChange +=
                new Outlook.ItemEvents_10_CustomPropertyChangeEventHandler(
                m_Contact_CustomPropertyChange);
        }
    }

    // Event Handler for the inspector close event.
    private void OutlookInspectorWindow_Close()
    {
        // Unhook events from any item-level instance variables
        m_Contact.Open -= 
            Outlook.ItemEvents_10_OpenEventHandler(
            m_Contact_Open);
        m_Contact.PropertyChange -= 
            Outlook.ItemEvents_10_PropertyChangeEventHandler(
            m_Contact_PropertyChange);
        m_Contact.CustomPropertyChange -= 
            Outlook.ItemEvents_10_CustomPropertyChangeEventHandler(
            m_Contact_CustomPropertyChange);
        ((Outlook.ItemEvents_Event)m_Contact).Close -= 
            Outlook.ItemEvents_CloseEventHandler(
            m_Contact_Close);

        // Unhook events from the window
        ((Outlook.InspectorEvents_Event)m_Window).Close -=
            new Outlook.InspectorEvents_CloseEventHandler(
            OutlookInspectorWindow_Close);

        // Raise the OutlookInspector close event
        if (Close != null)
        {
            Close(this, EventArgs.Empty);
        }
        // Release item-level instance variables
        m_Mail = null;
        m_Appointment = null;
        m_Contact = null;
        m_Task = null;
        m_Window = null;
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Beispielaufgaben mit Outlook-Ereignissen](sample-tasks-using-outlook-events.md)

