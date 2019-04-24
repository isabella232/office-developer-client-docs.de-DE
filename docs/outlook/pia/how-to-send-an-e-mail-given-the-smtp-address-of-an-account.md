---
title: Senden einer E-Mail-Nachricht mithilfe der SMTP-Adresse eines Kontos
TOCTitle: Send an email given the SMTP address of an account
ms:assetid: 4ff4aaac-54ba-45c7-8b2e-aeba35af1e56
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462095(v=office.15)
ms:contentKeyID: 55119865
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0771941581d0edaab1660790582cfb22bef48dc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332095"
---
# <a name="send-an-email-given-the-smtp-address-of-an-account"></a>Senden einer E-Mail-Nachricht mithilfe der SMTP-Adresse eines Kontos

In diesem Thema wird erklärt, wie Sie eine E-Mail erstellen und mit einem Microsoft Outlook-Konto bei vorgegebener SMTP-Adresse (Simple Mail Transfer Protocol) dieses Kontos senden.

## <a name="example"></a>Beispiel

> [!NOTE] 
> Helmut Obertanner hat das folgende Codebeispiel bereitgestellt. Helmut verfügt über Fachwissen zu Office Developer Tools für Visual Studio und Outlook. 


Das folgende Codebeispiel enthält die Methoden „SendEmailFromAccount“ und „GetAccountForEmailAddress“ der Sample-Klasse, die als Teil eines Outlook-Add-In-Projekts implementiert werden. Jedes Projekt fügt einen Verweis auf die primäre Interopassembly für Outlook hinzu, der auf dem [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\))-Namespace basiert. Die SendEmailFromAccount-Methode akzeptiert als Eingabe ein vertrauenswürdiges [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\))-Objekt sowie Zeichenfolgen, die den Betreff, Text, eine durch Semikolons getrennte Liste von Empfängern und die E-Mail-Adresse eines E-Mail-Kontos darstellen. SendEmailFromAccount erstellt ein [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\))-Objekt und initialisiert die Eigenschaften [To](https://msdn.microsoft.com/library/bb624372\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) und [Body](https://msdn.microsoft.com/library/bb646600\(v=office.15\)) mit den angegebenen Argumenten. Zum Bestimmen des [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\))-Objekts, das die E-Mail senden soll, ruft SendEmailFromAccount die GetAccountForEmailAddress-Methode auf, die die angegebene SMTP-Adresse mit der [SmtpAddress](https://msdn.microsoft.com/library/bb623516\(v=office.15\))-Eigenschaft jedes Kontos für das aktuelle Profil abgleicht. Das übereinstimmende **Account**-Objekt wird an das SendEmailFromAccount-Objekt zurückgegeben, das anschließend die [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\))-Eigenschaft des **MailItem**-Objekts mit dem **Account**-Objekt initialisiert und das **MailItem**-Objekt sendet.

Es folgen das Visual Basic-Codebeispiel und anschließend das C\#-Codebeispiel.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die Anweisung **Imports** oder **using** darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgenden Codezeilen zeigen, wie Sie den Import und die Zuweisung in Visual Basic und C\# vornehmen.

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook

Namespace OutlookAddIn2
    Class Sample
        
        Shared Sub SendEmailFromAccount(ByVal application As Outlook.Application, _
            ByVal subject As String, ByVal body As String, ByVal recipients As String, ByVal smtpAddress As String)

            ' Create a new MailItem and set the To, Subject, and Body properties.
            Dim newMail As Outlook.MailItem = DirectCast(application.CreateItem(Outlook.OlItemType.olMailItem), Outlook.MailItem)
            newMail.To = recipients
            newMail.Subject = subject
            newMail.Body = body

            ' Retrieve the account that has the specific SMTP address.
            Dim account As Outlook.Account = GetAccountForEmailAddress(application, smtpAddress)
            ' Use this account to send the email.
            newMail.SendUsingAccount = account
            newMail.Send()
        End Sub

        Shared Function GetAccountForEmailAddress(ByVal application As Outlook.Application, ByVal smtpAddress As String) As Outlook.Account

            ' Loop over the Accounts collection of the current Outlook session.
            Dim accounts As Outlook.Accounts = application.Session.Accounts
            Dim account As Outlook.Account
            For Each account In accounts
                ' When the email address matches, return the account.
                If account.SmtpAddress = smtpAddress Then
                    Return account
                End If
            Next
            Throw New System.Exception(String.Format("No Account with SmtpAddress: {0} exists!", smtpAddress))
        End Function

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
        public static void SendEmailFromAccount(Outlook.Application application, string subject, string body, string to, string smtpAddress)
        {

            // Create a new MailItem and set the To, Subject, and Body properties.
            Outlook.MailItem newMail = (Outlook.MailItem)application.CreateItem(Outlook.OlItemType.olMailItem);
            newMail.To = to;
            newMail.Subject = subject;
            newMail.Body = body;

            // Retrieve the account that has the specific SMTP address.
            Outlook.Account account = GetAccountForEmailAddress(application, smtpAddress);
            // Use this account to send the email.
            newMail.SendUsingAccount = account;
            newMail.Send();
        }


        public static Outlook.Account GetAccountForEmailAddress(Outlook.Application application, string smtpAddress)
        {

            // Loop over the Accounts collection of the current Outlook session.
            Outlook.Accounts accounts = application.Session.Accounts;
            foreach (Outlook.Account account in accounts)
            {
                // When the email address matches, return the account.
                if (account.SmtpAddress == smtpAddress)
                {
                    return account;
                }
            }
            throw new System.Exception(string.Format("No Account with SmtpAddress: {0} exists!", smtpAddress));
        }

    }
}
```

## <a name="see-also"></a>Siehe auch

- [Mail](mail.md)

