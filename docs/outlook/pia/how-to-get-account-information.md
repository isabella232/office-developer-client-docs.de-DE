---
title: Abrufen von Kontoinformationen
TOCTitle: Get account information
ms:assetid: 02825449-50eb-42d0-8e45-361db5f473df
ms:contentKeyID: 55119795
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b80a6c47373842437b9944ea25c212810a9de107
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722732"
---
# <a name="get-account-information"></a><span data-ttu-id="57cb5-102">Abrufen von Kontoinformationen</span><span class="sxs-lookup"><span data-stu-id="57cb5-102">Get account information</span></span>

<span data-ttu-id="57cb5-103">Dieses Beispiel verwendet als Eingabeargument ein vertrauenswürdiges [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\))-Objekt von Outlook und zeigt mithilfe des **Account**-Objekts die Details aller Konten an, die für das aktuelle Outlook-Profil zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="57cb5-103">This topic takes as an input argument a trusted Outlook [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object, and uses the **Account** object to display the details of each account that is available for the current Outlook profile.</span></span>

## <a name="example"></a><span data-ttu-id="57cb5-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="57cb5-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="57cb5-105">Helmut Obertanner hat das folgende Codebeispiel bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="57cb5-105">Helmut Obertanner provided the following code examples.</span></span> <span data-ttu-id="57cb5-106">Helmut verfügt über Fachwissen zu Office Developer Tools für Visual Studio und Outlook.</span><span class="sxs-lookup"><span data-stu-id="57cb5-106">Helmut's expertise is in Office Developer Tools for Visual Studio and Outlook.</span></span> 

<span data-ttu-id="57cb5-107">Die folgenden Codebeispiele enthalten die DisplayAccountInformation-Methode der Sample-Klasse, die als Teil eines Outlook-Add-In-Projekts implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="57cb5-107">The following code examples contain the DisplayAccountInformation method of the Sample class, implemented as part of an Outlook add-in project.</span></span> <span data-ttu-id="57cb5-108">Jedes Projekt fügt einen Verweis auf die primäre Interopassembly für Outlook hinzu, der auf dem [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\))-Namespace basiert.</span><span class="sxs-lookup"><span data-stu-id="57cb5-108">Each project adds a reference to the Outlook Primary Interop Assembly, which is based on the [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)) namespace.</span></span>

<span data-ttu-id="57cb5-109">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="57cb5-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="57cb5-110">Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="57cb5-110">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="57cb5-111">Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="57cb5-111">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

<span data-ttu-id="57cb5-112">Es folgen das Visual Basic-Codebeispiel und anschließend das C\#-Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="57cb5-112">The following is the Visual Basic code example, followed by the C\# code example.</span></span>


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook

Namespace OutlookAddIn2
    Class Sample
        Shared Sub DisplayAccountInformation(ByVal application As Outlook.Application)

            ' The Namespace Object (Session) has a collection of accounts.
            Dim accounts As Outlook.Accounts = application.Session.Accounts

            ' Concatenate a message with information about all accounts.
            Dim builder As StringBuilder = New StringBuilder()

            ' Loop over all accounts and print detail account information.
            ' All properties of the Account object are read-only.
            Dim account As Outlook.Account
            For Each account In accounts

                ' The DisplayName property represents the friendly name of the account.
                builder.AppendFormat("DisplayName: {0}" & vbNewLine, account.DisplayName)

                ' The UserName property provides an account-based context to determine identity.
                builder.AppendFormat("UserName: {0}" & vbNewLine, account.UserName)

                ' The SmtpAddress property provides the SMTP address for the account.
                builder.AppendFormat("SmtpAddress: {0}" & vbNewLine, account.SmtpAddress)

                ' The AccountType property indicates the type of the account.
                builder.Append("AccountType: ")
                Select Case (account.AccountType)

                    Case Outlook.OlAccountType.olExchange
                        builder.AppendLine("Exchange")


                    Case Outlook.OlAccountType.olHttp
                        builder.AppendLine("Http")


                    Case Outlook.OlAccountType.olImap
                        builder.AppendLine("Imap")


                    Case Outlook.OlAccountType.olOtherAccount
                        builder.AppendLine("Other")


                    Case Outlook.OlAccountType.olPop3
                        builder.AppendLine("Pop3")


                End Select

                builder.AppendLine()
            Next


            ' Display the account information.
            Windows.Forms.MessageBox.Show(builder.ToString())
        End Sub


    End Class
End Namespace
```



```csharp
using System;
using System.Text;
using Outlook = Microsoft.Office.Interop.Outlook;

namespace OutlookAddIn1
{
    class Sample
    {
        public static void DisplayAccountInformation(Outlook.Application application)
        {

            // The Namespace Object (Session) has a collection of accounts.
            Outlook.Accounts accounts = application.Session.Accounts;

            // Concatenate a message with information about all accounts.
            StringBuilder builder = new StringBuilder();

            // Loop over all accounts and print detail account information.
            // All properties of the Account object are read-only.
            foreach (Outlook.Account account in accounts)
            {

                // The DisplayName property represents the friendly name of the account.
                builder.AppendFormat("DisplayName: {0}\n", account.DisplayName);

                // The UserName property provides an account-based context to determine identity.
                builder.AppendFormat("UserName: {0}\n", account.UserName);

                // The SmtpAddress property provides the SMTP address for the account.
                builder.AppendFormat("SmtpAddress: {0}\n", account.SmtpAddress);

                // The AccountType property indicates the type of the account.
                builder.Append("AccountType: ");
                switch (account.AccountType)
                {

                    case Outlook.OlAccountType.olExchange:
                        builder.AppendLine("Exchange");
                        break;

                    case Outlook.OlAccountType.olHttp:
                        builder.AppendLine("Http");
                        break;

                    case Outlook.OlAccountType.olImap:
                        builder.AppendLine("Imap");
                        break;

                    case Outlook.OlAccountType.olOtherAccount:
                        builder.AppendLine("Other");
                        break;

                    case Outlook.OlAccountType.olPop3:
                        builder.AppendLine("Pop3");
                        break;
                }

                builder.AppendLine();
            }

            // Display the account information.
            System.Windows.Forms.MessageBox.Show(builder.ToString());
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="57cb5-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57cb5-113">See also</span></span>

- [<span data-ttu-id="57cb5-114">Konten</span><span class="sxs-lookup"><span data-stu-id="57cb5-114">Accounts</span></span>](accounts.md)

