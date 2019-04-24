---
title: Implementieren eines Wrappers für Prüfungen und Nachverfolgung von Ereignissen auf Elementebene in jedem Inspektor
TOCTitle: Implement a wrapper for inspectors and track item-level events in each inspector
ms:assetid: 8021dd2b-c36c-492b-b281-783e85140ad8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184620(v=office.15)
ms:contentKeyID: 55119854
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a70aedf9a8803a2c990f07a77d4fc730f7263aae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320125"
---
# <a name="implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector"></a><span data-ttu-id="44e43-102">Implementieren eines Wrappers für Prüfungen und Nachverfolgung von Ereignissen auf Elementebene in jedem Inspektor</span><span class="sxs-lookup"><span data-stu-id="44e43-102">Implement a wrapper for inspectors and track item-level events in each inspector</span></span>

<span data-ttu-id="44e43-103">Dieses Thema enthält zwei Codebeispiele, die zeigen, wie ein Wrapper für eine [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) -Auflistung implementiert und dieser Wrapper zur Nachverfolgung von Ereignissen auf Elementebene in jedem [Inspector](https://msdn.microsoft.com/library/bb647744\(v=office.15\)) -Objekt in der Auflistung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="44e43-103">This topic contains two code examples that show how to implement a wrapper for an [Inspectors](https://msdn.microsoft.com/library/bb623458\(v=office.15\)) collection and to use that wrapper to track item-level events in each [Inspector](https://msdn.microsoft.com/library/bb647744\(v=office.15\)) object in the collection.</span></span>

## <a name="example"></a><span data-ttu-id="44e43-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="44e43-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="44e43-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="44e43-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="44e43-106">In den folgenden beiden Codebeispielen werden die Connect- und OutlookInspector-Klassen implementiert.</span><span class="sxs-lookup"><span data-stu-id="44e43-106">The following two code examples implement the Connect and OutlookInspector classes.</span></span> <span data-ttu-id="44e43-107">Das erste Codebeispiel betrifft Methoden und Ereignishandler, die Sie in die Connect-Klasse einschließen, um einen Wrapper für eine **Inspectors**-Auflistung zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="44e43-107">The first code example involves methods and event handlers you include in the Connect class to implement a wrapper for an **Inspectors** collection.</span></span> <span data-ttu-id="44e43-108">Das zweite Codebeispiel betrifft eine einfache Implementierung der **OutlookInspector**-Klasse.</span><span class="sxs-lookup"><span data-stu-id="44e43-108">The second code example involves a simple implementation of the **OutlookInspector** class.</span></span>

<span data-ttu-id="44e43-109">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="44e43-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="44e43-110">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="44e43-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="44e43-111">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="44e43-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

<span data-ttu-id="44e43-112">Im folgenden Codebeispiel tritt ein [NewInspector(Inspector)](https://msdn.microsoft.com/library/bb610594\(v=office.15\))-Ereignis auf, nachdem ein neues Inspektorfenster erstellt wurde und bevor es angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="44e43-112">In the following code example, a [NewInspector(Inspector)](https://msdn.microsoft.com/library/bb610594\(v=office.15\)) event occurs after a new inspector window has been created and before it is displayed.</span></span> <span data-ttu-id="44e43-113">Mit einer Benutzeraktion wird auch möglicherweise ein neues Inspektorfenster erstellt.</span><span class="sxs-lookup"><span data-stu-id="44e43-113">A user action may also create a new inspector window.</span></span> <span data-ttu-id="44e43-114">Es wird eine Instanzvariable auf Klassenebene namens „Inspectors“ in der **Connect**-Klasse deklariert, und ein **NewInspector**-Ereignis wird angebunden.</span><span class="sxs-lookup"><span data-stu-id="44e43-114">A class-level instance variable named inspectors in the **Connect** class is declared, and a **NewInspector** event is hooked up.</span></span> 

<span data-ttu-id="44e43-115">In der inspectors\_NewInspector-Methode prüft die **FindOutlookInspector**-Methode, ob ein neues Inspektorfenster bereits in der InspectorWindows-Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="44e43-115">In the inspectors\_NewInspector method, the **FindOutlookInspector** method checks whether the new inspector window is already in the inspectorWindows list.</span></span> <span data-ttu-id="44e43-116">Wenn FindOutlookInspector das **Inspector**-Objekt im inspectorWindows nicht findet, fügt die **AddInspector**-Methode eine Instanz der **OutlookInspector**-Klasse zu inspectorWindows hinzu.</span><span class="sxs-lookup"><span data-stu-id="44e43-116">If FindOutlookInspector does not find the **Inspector** object in inspectorWindows, the **AddInspector** method adds an instance of the **OutlookInspector** class to inspectorWindows.</span></span> <span data-ttu-id="44e43-117">Sie können die **OutlookInspector**-Klasse verwenden, um Ereignisse für dieses spezielle Inspektorfenster auszulösen.</span><span class="sxs-lookup"><span data-stu-id="44e43-117">You can use the **OutlookInspector** class to raise events for this particular inspector window.</span></span> <span data-ttu-id="44e43-118">Die Implementierung der **OutlookInspector**-Klasse wird im zweiten Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="44e43-118">The implementation of the **OutlookInspector** class is shown in the second code example.</span></span>

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

<span data-ttu-id="44e43-119">Das folgende Codebeispiel stellt eine Implementierung der **OutlookInspector**-Klasse dar.</span><span class="sxs-lookup"><span data-stu-id="44e43-119">The following code example is an implementation of the **OutlookInspector** class.</span></span> <span data-ttu-id="44e43-120">Diese Klasse dient zum Auslösen von Ereignissen für das Inspektorfenster aus dem vorherigen Beispiel.</span><span class="sxs-lookup"><span data-stu-id="44e43-120">This class is used to raise events for the inspector window from the preceding code example.</span></span> <span data-ttu-id="44e43-121">Es können mehrere Inspektorfenster gleichzeitig geöffnet sein.</span><span class="sxs-lookup"><span data-stu-id="44e43-121">Multiple inspector windows can be open simultaneously.</span></span> <span data-ttu-id="44e43-122">Ereignisse auf Elementebene wie [Open](https://msdn.microsoft.com/library/bb644296\(v=office.15\)), [PropertyChange](https://msdn.microsoft.com/library/bb647794\(v=office.15\)) und [CustomPropertyChange](https://msdn.microsoft.com/library/bb645015\(v=office.15\)) werden durch Einbinden in diesen Klassenkonstruktor nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="44e43-122">Item-level events such as [Open](https://msdn.microsoft.com/library/bb644296\(v=office.15\)), [PropertyChange](https://msdn.microsoft.com/library/bb647794\(v=office.15\)), and [CustomPropertyChange](https://msdn.microsoft.com/library/bb645015\(v=office.15\)) are tracked by hooking them up in this class constructor.</span></span> <span data-ttu-id="44e43-123">Ein [Close](https://msdn.microsoft.com/library/bb645009\(v=office.15\))-Ereignis für ein [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\))-Objekt ist auch in diesen Klassenkonstruktor eingebunden.</span><span class="sxs-lookup"><span data-stu-id="44e43-123">A [Close](https://msdn.microsoft.com/library/bb645009\(v=office.15\)) event for a [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) object is also hooked up in this class constructor.</span></span> <span data-ttu-id="44e43-124">Sie können bei Bedarf andere Elementinstanzvariablen auf Klassenebene definieren.</span><span class="sxs-lookup"><span data-stu-id="44e43-124">You can define other class-level item instance variables as needed.</span></span> <span data-ttu-id="44e43-125">Alle in den OutlookInspector-Konstruktor eingebundenen Ereignisse werden im OutlookInspectorWindow\_Close-Ereignishandler wieder getrennt.</span><span class="sxs-lookup"><span data-stu-id="44e43-125">All the events that were hooked up in the OutlookInspector constructor are unhooked in the OutlookInspectorWindow\_Close event handler.</span></span>

<span data-ttu-id="44e43-126">Beachten Sie, dass auf Objektmodellebene ein **Outlook-Inspektor**-Objekt nicht für einen Outlook-Elementtyp spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="44e43-126">Note that at the object model level, an **Outlook inspector** object is not specific to any Outlook item type.</span></span> <span data-ttu-id="44e43-127">In diesem Codebeispiel wird die OutlookItem-Hilfsklasse verwendet, die unter [Erstellen einer Hilfsklasse zum Zugriff auf allgemeine Member von Outlook-Elementen](how-to-create-a-helper-class-to-access-common-outlook-item-members.md) definiert ist, um die OutlookItem.Class-Eigenschaft aufzurufen, um die Nachrichtenklasse des aktuellen Elements im Inspector zu prüfen, ohne anzunehmen, dass es sich bei dem Element um ein Kontaktelement handelt.</span><span class="sxs-lookup"><span data-stu-id="44e43-127">This code sample makes use of the OutlookItem helper class, defined in [Create a Helper Class to Access Common Outlook Item Members](how-to-create-a-helper-class-to-access-common-outlook-item-members.md), to conveniently call the OutlookItem.Class property to verify the message class of the current item in the inspector, before assuming the item is a contact item.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="44e43-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44e43-128">See also</span></span>

- [<span data-ttu-id="44e43-129">Beispielaufgaben mit Outlook-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="44e43-129">Sample tasks using Outlook events</span></span>](sample-tasks-using-outlook-events.md)

