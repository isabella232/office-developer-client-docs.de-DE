---
title: Abrufen von Informationen über mehrere Konten
TOCTitle: Get information about multiple accounts
ms:assetid: 363f4058-3069-4ddc-b3ff-113a4dfd58c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184599(v=office.15)
ms:contentKeyID: 55119794
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d065761b9296f1c0eb3043e9b9778e438790f94e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703209"
---
# <a name="get-information-about-multiple-accounts"></a><span data-ttu-id="b34cf-102">Abrufen von Informationen über mehrere Konten</span><span class="sxs-lookup"><span data-stu-id="b34cf-102">Get information about multiple accounts</span></span>

<span data-ttu-id="b34cf-103">Outlook unterstützt Profile mit mindestens einem Konto, das mit einem Exchange-Server verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="b34cf-103">Outlook supports a profile that contains one or more accounts that are connected to an Exchange Server.</span></span> <span data-ttu-id="b34cf-104">In diesem Beispiel wird gezeigt, wie verschiedene Informationen zu jedem Konto im aktuellen Profil abgerufen und angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b34cf-104">This example shows how to obtain and display miscellaneous information about each account in the current profile.</span></span>

## <a name="example"></a><span data-ttu-id="b34cf-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b34cf-105">Example</span></span>

<span data-ttu-id="b34cf-p102">Die folgende Methode, EnumerateAccounts, zeigt den Kontonamen, den Benutzernamen und die SMTP-Adresse (Simple Mail Transfer Protocol) für jedes Konto an, das im aktuellen Profil definiert ist. Wenn das Konto mit einem Servercomputer mit Exchange verbunden ist, zeigt EnumerateAccounts den Namen des Servercomputers mit Exchange and sowie die Versionsinformationen. Wenn sich das Konto ferner in einem Zustellungsspeicher befindet, zeigt EnumerateAccounts den Namen des Standardzustellungsspeichers für das Konto an.</span><span class="sxs-lookup"><span data-stu-id="b34cf-p102">The following method, EnumerateAccounts, displays the account name, user name, and Simple Mail Transfer Protocol (SMTP) address for each account that is defined in the current profile. If the account is connected to an Exchange server, EnumerateAccounts displays the Exchange server name and version information. And if the account resides on a delivery store, EnumerateAccounts displays the name of the default delivery store for the account.</span></span>

<span data-ttu-id="b34cf-109">EnumerateAccounts greift auf die meisten dieser Informationen über das [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\))-Objekt zu, es sei denn das **Account**-Objekt enthält keinerlei Informationen über den Benutzernamen und die SMTP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="b34cf-109">EnumerateAccounts accesses most of this information from the [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) object, except when the **Account** object does not contain information about the user name and SMTP address.</span></span> <span data-ttu-id="b34cf-110">In dem Fall verwendet EnumerateAccounts das [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\))- und das [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\))-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b34cf-110">In that case, EnumerateAccounts uses the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) and [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) objects.</span></span> 

<span data-ttu-id="b34cf-111">EnumerateAccounts ruft das **AddressEntry**-Objekt mithilfe der [AddressEntry](https://msdn.microsoft.com/library/bb644359\(v=office.15\))-Eigenschaft des [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\))-Objekts ab, das von der [CurrentUser](https://msdn.microsoft.com/library/ff184864\(v=office.15\))-Eigenschaft abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="b34cf-111">EnumerateAccounts obtains the **AddressEntry** object by using the [AddressEntry](https://msdn.microsoft.com/library/bb644359\(v=office.15\)) property of the [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object obtained from the [CurrentUser](https://msdn.microsoft.com/library/ff184864\(v=office.15\)) property.</span></span> <span data-ttu-id="b34cf-112">EnumerateAccounts ruft das **ExchangeUser**-Objekt mithilfe der [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\))-Methode des **AddressEntry**-Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="b34cf-112">EnumerateAccounts obtains the **ExchangeUser** object by using the [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) method of the **AddressEntry** object.</span></span> 

<span data-ttu-id="b34cf-113">Nachfolgend finden Sie den Algorithmus zum Abrufen verschiedener Informationen mithilfe der Account-, AddressEntry- und ExchangeUser-Objekte:</span><span class="sxs-lookup"><span data-stu-id="b34cf-113">The following is the algorithm to obtain various information by using the Account, AddressEntry, and ExchangeUser objects:</span></span>

- <span data-ttu-id="b34cf-114">Enthält das **Account**-Objekt Informationen zu Benutzernamen und SMTP-Adresse, wird das **Account**-Objekt zum Anzeigen des Konto- und Benutzernamens, sowie der SMTP-Adresse und des Exchange-Servernamens und der Versionsinformationen verwendet, sofern es sich um ein Exchange-Konto handelt.</span><span class="sxs-lookup"><span data-stu-id="b34cf-114">If the **Account** object contains information about the user name and SMTP address, use the **Account** object to display the account name, user name, SMTP address, and Exchange server name and version information if the account is an Exchange account.</span></span>

- <span data-ttu-id="b34cf-115">Gehen Sie wie folgt vor, wenn das **Account**-Objekt keine Informationen zum Benutzernamen und der SMTP-Adresse enthält:</span><span class="sxs-lookup"><span data-stu-id="b34cf-115">If the **Account** object does not contain information about the user name and SMTP address, proceed as follows:</span></span>
    
  - <span data-ttu-id="b34cf-116">Wenn es sich bei dem Konto nicht um ein Exchange-Konto handelt, verwenden Sie das **AddressEntry**-Objekt zum Anzeigen des Benutzernamens und der SMTP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="b34cf-116">If the account is not an Exchange account, use the **AddressEntry** object to display the user name and SMTP address.</span></span>
    
  - <span data-ttu-id="b34cf-117">Wenn es sich bei dem Konto um ein Exchange-Konto handelt, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="b34cf-117">If the account is an Exchange account, proceed as follows:</span></span>
        
    1.  <span data-ttu-id="b34cf-118">Verwenden Sie das **Account**-Objekt zum Anzeigen von Kontoname, Exchange-Servername und Exchange-Versionsinformationen.</span><span class="sxs-lookup"><span data-stu-id="b34cf-118">Use the **Account** object to display the account name, Exchange server name, and Exchange version information.</span></span>
        
    2.  <span data-ttu-id="b34cf-119">Verwenden Sie das **ExchangeUser**-Objekt, um den Benutzernamen und die SMTP-Adresse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b34cf-119">Use the **ExchangeUser** object to display the user name and SMTP address.</span></span>

<span data-ttu-id="b34cf-120">Wenn Sie Visual Studio verwenden, um dieses Codebeispiel zu testen, müssen Sie der Microsoft Outlook 15.0-Objektbibliothekkomponente zuerst einen Verweis hinzufügen und die Outlook-Variable angeben, wenn Sie den **Microsoft.Office.Interop.Outlook**-Namespace importieren.</span><span class="sxs-lookup"><span data-stu-id="b34cf-120">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="b34cf-121">Die **using**-Anweisung darf im Codebeispiel nicht direkt vor den Funktionen stehen, sondern muss vor der öffentlichen Class-Deklaration hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b34cf-121">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="b34cf-122">Die folgende Codezeile zeigt, wie Sie den Import und die Zuweisung in C\# vornehmen.</span><span class="sxs-lookup"><span data-stu-id="b34cf-122">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="b34cf-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b34cf-123">See also</span></span>

- [<span data-ttu-id="b34cf-124">Konten</span><span class="sxs-lookup"><span data-stu-id="b34cf-124">Accounts</span></span>](accounts.md)

