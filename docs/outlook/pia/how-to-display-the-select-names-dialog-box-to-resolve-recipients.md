---
title: Anzeigen des Dialogfelds „Namen auswählen“ zum Auflösen von Empfängern
TOCTitle: Display the Select Names dialog box to resolve recipients
ms:assetid: 841dd4cd-6d69-46d5-8c83-e28c95b631a9
ms:mtpsurl: https://msdn.microsoft.com/library/Bb646055(v=office.15)
ms:contentKeyID: 55119876
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f92891188e7c317465ce70fede1dedca7f6344fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316065"
---
# <a name="display-the-select-names-dialog-box-to-resolve-recipients"></a><span data-ttu-id="adcd6-102">Anzeigen des Dialogfelds „Namen auswählen“ zum Auflösen von Empfängern</span><span class="sxs-lookup"><span data-stu-id="adcd6-102">Display the Select Names dialog box to resolve recipients</span></span>

<span data-ttu-id="adcd6-103">In diesem Beispiel wird versucht, die im *recips*-Parameter angegebenen Empfänger aufzulösen. Für jeden mehrdeutigen Empfänger, der nicht aufgelöst werden kann, wird das Outlook-Dialogfeld **Namen auswählen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="adcd6-103">This example attempts to resolve the recipients provided by the *recips* parameter, and displays the Outlook **Select Names** dialog box for each recipient that is ambiguous and cannot be resolved.</span></span>

## <a name="example"></a><span data-ttu-id="adcd6-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="adcd6-104">Example</span></span>

<span data-ttu-id="adcd6-105">In dem Codebeispiel wird das [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) -Objekt aufgerufen, um das Dialogfeld **Namen auswählen** anzuzeigen, das das Outlook-Adressbuch enthält.</span><span class="sxs-lookup"><span data-stu-id="adcd6-105">This code sample calls the [SelectNamesDialog](https://msdn.microsoft.com/library/bb609866\(v=office.15\)) object to display the **Select Names** dialog box which shows the Outlook address book.</span></span> <span data-ttu-id="adcd6-106">In diesem Dialogfeld kann der Benutzer einen Namen aus dem Adressbuch auswählen.</span><span class="sxs-lookup"><span data-stu-id="adcd6-106">Through this dialog box, the user can select a name from the address book.</span></span> <span data-ttu-id="adcd6-107">Wird der Name nicht aufgelöst, wird der Empfänger aus recips entfernt.</span><span class="sxs-lookup"><span data-stu-id="adcd6-107">If the name is not resolved, the recipient will be removed from recips.</span></span> <span data-ttu-id="adcd6-108">Wird der Name aufgelöst, wird das [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\))-Objekt des Empfängers an recips zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="adcd6-108">If the name is resolved, then the code sample will return the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object of the recipient to recips.</span></span>

<span data-ttu-id="adcd6-109">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="adcd6-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="adcd6-110">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="adcd6-110">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="adcd6-111">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="adcd6-111">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub ResolveRecipients(ByVal recips As Outlook.Recipients)
    If recips Is Nothing Then
        Throw New ArgumentNullException()
    End If
    If recips.ResolveAll() Then
        Return
    Else
        For i As Integer = recips.Count To 1 Step -1
            If Not (recips(i).Resolve()) Then
                Dim snd As Outlook.SelectNamesDialog = _
                    Application.Session.GetSelectNamesDialog()
                snd.Recipients.Add(recips(i).Name)
                snd.NumberOfRecipientSelectors = _
                    Outlook.OlRecipientSelectors.olShowTo
                snd.AllowMultipleSelection = False
                snd.Display()
                If Not (snd.Recipients.ResolveAll()) Then
                    recips.Remove(i)
                Else
                    recips.Remove(i)
                    recips.Add(snd.Recipients(1).Address)
                End If
                snd = Nothing
            End If
        Next
    End If
End Sub
```


```csharp
private void ResolveRecipients(Outlook.Recipients recips)
{
    if (recips == null)
    {
        throw new ArgumentNullException();
    }
    if (recips.ResolveAll())
    {
        return;
    }
    else
    {
        for (int i = recips.Count; i > 0; i--)
        {
            if (!recips[i].Resolve())
            {
                Outlook.SelectNamesDialog snd =
                    Application.Session.
                    GetSelectNamesDialog();
                snd.Recipients.Add(recips[i].Name);
                snd.NumberOfRecipientSelectors =
                    Outlook.OlRecipientSelectors.olShowTo;
                snd.AllowMultipleSelection = false;
                snd.Display();
                if (!snd.Recipients.ResolveAll())
                {
                    recips.Remove(i);
                }
                else
                {
                    recips.Remove(i);
                    recips.Add(snd.Recipients[1].Address);
                }
                snd = null;
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="adcd6-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="adcd6-112">See also</span></span>

- [<span data-ttu-id="adcd6-113">Empfänger</span><span class="sxs-lookup"><span data-stu-id="adcd6-113">Recipients</span></span>](recipients.md)

