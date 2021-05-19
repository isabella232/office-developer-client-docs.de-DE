---
title: Verwenden des Dialogfelds „Namen auswählen“ zum Abrufen und Zuweisen von Empfängern zu einem Termin
TOCTitle: Use the Select Names dialog box to obtain and assign recipients to an appointment
ms:assetid: b9bcb341-1912-425c-8d75-ed5be233145a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184636(v=office.15)
ms:contentKeyID: 55119878
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 408d2fbdc3c89b7f2bad1fe9c2c76c1f47ae05ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335378"
---
# <a name="use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment"></a><span data-ttu-id="a9c1f-102">Verwenden des Dialogfelds „Namen auswählen“ zum Abrufen und Zuweisen von Empfängern zu einem Termin</span><span class="sxs-lookup"><span data-stu-id="a9c1f-102">Use the Select Names dialog box to obtain and assign recipients to an appointment</span></span>

<span data-ttu-id="a9c1f-103">In diesem Beispiel wird gezeigt, wie das Dialogfeld **Namen auswählen** zum Abrufen und Zuweisen von Empfängern zu einem Termin verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a9c1f-103">This example shows how to use the **Select Names** dialog box to obtain and assign recipients to an appointment item.</span></span>

## <a name="example"></a><span data-ttu-id="a9c1f-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a9c1f-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="a9c1f-105">Das folgende Codebeispiel ist ein Auszug aus [Programming Applications für Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="a9c1f-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="a9c1f-p101">Zum Anzeigen des Dialogfelds **Namen auswählen** rufen Sie die [Display()](https://msdn.microsoft.com/library/bb646086\(v=office.15\)) -Methode des [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) -Objekts auf. Nachdem das Dialogfeld **Namen auswählen** angezeigt wurde, wird die Codeausführung angehalten, bis der Benutzer auf **OK** klickt oder das Dialogfeld schließt. Verwenden Sie die [Recipients](https://msdn.microsoft.com/library/bb652601\(v=office.15\)) -Eigenschaft des **SelectNamesDialog**-Objekts, um anfänglich im Dialogfeld angezeigte Empfänger festzulegen oder die im Dialogfeld ausgewählten Empfänger abzurufen. Die Eigenschaft gibt eine [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) -Auflistung zurück, die **SelectNamesDialog** zugeordnet ist. Zum Hinzufügen eines [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) -Objekts zur **Recipients**-Auflistung für **SelectNamesDialog** verwenden Sie die [Add](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) -Methode für die Auflistung und geben die [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) -Eigenschaft des **Recipient**-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="a9c1f-p101">To display the **Select Names** dialog box, call the [Display()](https://msdn.microsoft.com/library/bb646086\(v=office.15\)) method of the [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) object. Once the **Select Names** dialog box is displayed to the user, code execution halts until the user clicks **OK** or closes the dialog box. To set initial recipients to display in the dialog box, or to get the recipients selected in the dialog box, use the [Recipients](https://msdn.microsoft.com/library/bb652601\(v=office.15\)) property of the **SelectNamesDialog** object. This returns a [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection that is associated with the **SelectNamesDialog**. To add a [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object to the **Recipients** collection for the **SelectNamesDialog**, use the [Add](https://msdn.microsoft.com/library/bb612668\(v=office.15\)) method for the collection and specify the [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) property of the **Recipient** object.</span></span>

<span data-ttu-id="a9c1f-111">Im folgenden Codebeispiel erstellt DemoSelectNamesDialogRecipients ein [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\))-Objekt und legt einige seiner Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="a9c1f-111">In the following code example, DemoSelectNamesDialogRecipients creates an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object and sets some of its properties.</span></span> <span data-ttu-id="a9c1f-112">Anschließend wird ein **SelectNamesDialog**-Objekt erstellt und mit der [SetDefaultDisplayMode(OlDefaultSelectNamesDisplayMode)](https://msdn.microsoft.com/library/bb623783\(v=office.15\)) -Methode ein Besprechungsanzeigemodus für das Dialogfeld **Namen auswählen** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a9c1f-112">It then creates a **SelectNamesDialog** and uses the [SetDefaultDisplayMode(OlDefaultSelectNamesDisplayMode)](https://msdn.microsoft.com/library/bb623783\(v=office.15\)) method to set a meeting display mode for the **Select Names** dialog box.</span></span> <span data-ttu-id="a9c1f-113">Im Beispiel wird die **Resource**-Empfängerauswahl mit der Zeichenfolge "Conf Room 36/2739" aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="a9c1f-113">The example populates the **Resource** recipient selector with the string "Conf Room 36/2739".</span></span> <span data-ttu-id="a9c1f-114">Nachdem das Dialogfeld dem Benutzer angezeigt wurde, zählt der Code die **Recipients**-Auflistung auf, die dieser Instanz von **SelectNamesDialog** zugeordnet ist, und fügt diese Empfänger dem erstellten Termin hinzu.</span><span class="sxs-lookup"><span data-stu-id="a9c1f-114">Once the dialog box is displayed to the user, the code enumerates the **Recipients** collection that is associated with this instance of **SelectNamesDialog** and adds those recipients to the appointment that was created.</span></span> <span data-ttu-id="a9c1f-115">Schließlich wird in dem Beispiel die Besprechungsanfrage für den Benutzer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a9c1f-115">Finally, the example displays the meeting request to the user.</span></span>

<span data-ttu-id="a9c1f-116">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="a9c1f-116">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="a9c1f-117">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a9c1f-117">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="a9c1f-118">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="a9c1f-118">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoSelectNamesDialogRecipients()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.MeetingStatus = Outlook.OlMeetingStatus.olMeeting;
    appt.Subject = "Team Morale Event";
    appt.Start = DateTime.Parse("5/17/2007 11:00 AM");
    appt.End = DateTime.Parse("5/17/2007 12:00 PM");
    Outlook.SelectNamesDialog snd =
        Application.Session.GetSelectNamesDialog();
    snd.SetDefaultDisplayMode(
        Outlook.OlDefaultSelectNamesDisplayMode.olDefaultMeeting);
    Outlook.Recipient confRoom =
        snd.Recipients.Add("Conf Room 36/2739");
    // Explicitly specify Recipient.Type.
    confRoom.Type = (int)Outlook.OlMeetingRecipientType.olResource;
    snd.Recipients.ResolveAll();
    snd.Display();
    // Add Recipients to meeting request.
    Outlook.Recipients recips = snd.Recipients;
    if (recips.Count > 0)
    {
        foreach (Outlook.Recipient recip in recips)
        {
            appt.Recipients.Add(recip.Name);
        }
    }
    appt.Recipients.ResolveAll();
    appt.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="a9c1f-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9c1f-119">See also</span></span>

- [<span data-ttu-id="a9c1f-120">Empfänger</span><span class="sxs-lookup"><span data-stu-id="a9c1f-120">Recipients</span></span>](recipients.md)

