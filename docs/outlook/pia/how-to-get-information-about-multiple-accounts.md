---
title: Abrufen von Informationen über mehrere Konten
TOCTitle: Get information about multiple accounts
ms:assetid: 363f4058-3069-4ddc-b3ff-113a4dfd58c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184599(v=office.15)
ms:contentKeyID: 55119794
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 179cf1e4fb54098c40ce2b080b4569b9392de90b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590653"
---
# <a name="get-information-about-multiple-accounts"></a>Abrufen von Informationen über mehrere Konten

Outlook unterstützt Profile mit mindestens einem Konto, das mit einem Exchange-Server verbunden ist. In diesem Beispiel wird gezeigt, wie verschiedene Informationen zu jedem Konto im aktuellen Profil abgerufen und angezeigt werden.

## <a name="example"></a>Beispiel

Die folgende Methode, EnumerateAccounts, zeigt den Kontonamen, den Benutzernamen und die SMTP-Adresse (Simple Mail Transfer Protocol) für jedes Konto an, das im aktuellen Profil definiert ist. Wenn das Konto mit einem Servercomputer mit Exchange verbunden ist, zeigt EnumerateAccounts den Namen des Servercomputers mit Exchange and sowie die Versionsinformationen. Wenn sich das Konto ferner in einem Zustellungsspeicher befindet, zeigt EnumerateAccounts den Namen des Standardzustellungsspeichers für das Konto an.

EnumerateAccounts greift auf die meisten dieser Informationen über das [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\))-Objekt zu, es sei denn das **Account**-Objekt enthält keinerlei Informationen über den Benutzernamen und die SMTP-Adresse. In dem Fall verwendet EnumerateAccounts das [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\))- und das [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\))-Objekt. 

EnumerateAccounts ruft das **AddressEntry**-Objekt mithilfe der [AddressEntry](https://msdn.microsoft.com/library/bb644359\(v=office.15\))-Eigenschaft des [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\))-Objekts ab, das von der [CurrentUser](https://msdn.microsoft.com/library/ff184864\(v=office.15\))-Eigenschaft abgerufen wurde. EnumerateAccounts ruft das **ExchangeUser**-Objekt mithilfe der [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\))-Methode des **AddressEntry**-Objekts ab. 

Nachfolgend finden Sie den Algorithmus zum Abrufen verschiedener Informationen mithilfe der Account-, AddressEntry- und ExchangeUser-Objekte:

- Enthält das **Account**-Objekt Informationen zu Benutzernamen und SMTP-Adresse, wird das **Account**-Objekt zum Anzeigen des Konto- und Benutzernamens, sowie der SMTP-Adresse und des Exchange-Servernamens und der Versionsinformationen verwendet, sofern es sich um ein Exchange-Konto handelt.

- Gehen Sie wie folgt vor, wenn das **Account**-Objekt keine Informationen zum Benutzernamen und der SMTP-Adresse enthält:
    
  - Wenn es sich bei dem Konto nicht um ein Exchange-Konto handelt, verwenden Sie das **AddressEntry**-Objekt zum Anzeigen des Benutzernamens und der SMTP-Adresse.
    
  - Wenn es sich bei dem Konto um ein Exchange-Konto handelt, gehen Sie wie folgt vor:
        
    1.  Verwenden Sie das **Account**-Objekt zum Anzeigen von Kontoname, Exchange-Servername und Exchange-Versionsinformationen.
        
    2.  Verwenden Sie das **ExchangeUser**-Objekt, um den Benutzernamen und die SMTP-Adresse anzuzeigen.

Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren. Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden. Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void EnumerateAccounts()
{
    Outlook.Accounts accounts =
        Application.Session.Accounts;
    foreach (Outlook.Account account in accounts)
    {
        try
        {
            StringBuilder sb = new StringBuilder();
            sb.AppendLine("Account: " + account.DisplayName);
            if (string.IsNullOrEmpty(account.SmtpAddress)
                || string.IsNullOrEmpty(account.UserName))
            {
                Outlook.AddressEntry oAE =
                    account.CurrentUser.AddressEntry
                    as Outlook.AddressEntry;
                if (oAE.Type == "EX")
                {
                    Outlook.ExchangeUser oEU =
                        oAE.GetExchangeUser()
                        as Outlook.ExchangeUser;
                    sb.AppendLine("UserName: " +
                        oEU.Name);
                    sb.AppendLine("SMTP: " +
                        oEU.PrimarySmtpAddress);
                    sb.AppendLine("Exchange Server: " +
                        account.ExchangeMailboxServerName);
                    sb.AppendLine("Exchange Server Version: " +
                        account.ExchangeMailboxServerVersion); 
                }
                else
                {
                    sb.AppendLine("UserName: " +
                        oAE.Name);
                    sb.AppendLine("SMTP: " +
                        oAE.Address);
                }
            }
            else
            {
                sb.AppendLine("UserName: " +
                    account.UserName);
                sb.AppendLine("SMTP: " +
                    account.SmtpAddress);
                if(account.AccountType == 
                    Outlook.OlAccountType.olExchange)
                {
                    sb.AppendLine("Exchange Server: " +
                        account.ExchangeMailboxServerName);
                    sb.AppendLine("Exchange Server Version: " +
                        account.ExchangeMailboxServerVersion); 
                }
            }
            if(account.DeliveryStore !=null)
            {
                sb.AppendLine("Delivery Store: " +
                    account.DeliveryStore.DisplayName);
            }
            sb.AppendLine("---------------------------------");
            Debug.Write(sb.ToString());
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a>Siehe auch

- [Accounts](accounts.md)

