---
title: Konfigurieren von RDS unter Windows 2000
TOCTitle: Configuring RDS on Windows 2000
ms:assetid: eb2d4c1d-8b3b-07ac-258f-edb0b1a3daba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250193(v=office.15)
ms:contentKeyID: 48548482
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8482df5ca2fab110e5b1a77fe227c5f0c583d893
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296017"
---
# <a name="configuring-rds-on-windows-2000"></a><span data-ttu-id="7e900-102">Konfigurieren von RDS unter Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7e900-102">Configuring RDS on Windows 2000</span></span>


<span data-ttu-id="7e900-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7e900-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7e900-104">Wenn es sich für Sie schwierig erweist, die Funktionsfähigkeit von RDS (Remote Data Service) nach eine Update auf Windows 2000 herzustellen, befolgen Sie die unten aufgeführten Schritte, um das Problem zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="7e900-104">If you experience difficulties getting RDS to function properly after upgrading to Windows 2000, follow the steps below to troubleshoot the issue.</span></span>

1.  <span data-ttu-id="7e900-105">Stellen Sie sicher, dass der www-VeröffentlichungsDienst zuerst durch Navigieren zum https://-*Server* mit Internet Explorer gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="7e900-105">Make sure that the World Wide Web Publishing Service is running first by navigating to https://*server* using Internet Explorer.</span></span> <span data-ttu-id="7e900-106">If you are unable to access the web server this way, go to a command prompt and enter the following command, "NET START W3SVC".</span><span class="sxs-lookup"><span data-stu-id="7e900-106">If you are unable to access the web server this way, go to a command prompt and enter the following command, "NET START W3SVC".</span></span>

2.  <span data-ttu-id="7e900-107">From the Start menu, select Run.</span><span class="sxs-lookup"><span data-stu-id="7e900-107">From the Start menu, select Run.</span></span> <span data-ttu-id="7e900-108">Type msdfmap.ini and click OK to open the msdfmap.ini file in Notepad.</span><span class="sxs-lookup"><span data-stu-id="7e900-108">Type msdfmap.ini and click OK to open the msdfmap.ini file in Notepad.</span></span> <span data-ttu-id="7e900-109">Überprüfen \[Sie den\] Abschnitt Connect Default, und wenn der Parameter Access auf NoAccess festgelegt ist, ändern Sie ihn in ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="7e900-109">Check the \[CONNECT DEFAULT\] section, and if the ACCESS parameter is set to NOACCESS, change it to READONLY.</span></span>

3.  <span data-ttu-id="7e900-110">Navigieren Sie mit dem Dienstprogramm RegEdit zu "\_HKEY\_-\\lokale\\Computer\\Software Microsoft\\DataFactory HandlerInfo", und stellen Sie sicher, dass **HandlerRequired** auf 0 und **DefaultHandler** ist "" (null Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="7e900-110">Using the RegEdit utility, navigate to "HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\DataFactory\\HandlerInfo" and make sure **HandlerRequired** is set to 0 and **DefaultHandler** is "" (Null string).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="7e900-111">Wenn Sie diesen Abschnitt der Registrierung ändern, müssen Sie den WWW-Publishingdienst beenden und neu starten, indem Sie die folgenden Befehle an der Eingabeaufforderung eingeben: NET STOP W3SVC und NET START W3SVC.</span><span class="sxs-lookup"><span data-stu-id="7e900-111">If you make any changes to this section of the registry, you must stop and restart the World Wide Web Publishing Service by entering the following commands at a command prompt: "NET STOP W3SVC" and "NET START W3SVC".</span></span>

4.  <span data-ttu-id="7e900-112">Navigieren Sie mit dem Dienstprogramm RegEdit in der Registrierung zu "\_HKEY\_local\\Machine\\System\\CurrentControlSet\\Services\\W3SVC\\Parameters ADCLaunch", und überprüfen Sie, ob ein Schlüssel namens \*\* RDSServer. DataFactory\*\*.</span><span class="sxs-lookup"><span data-stu-id="7e900-112">Using the RegEdit utility, navigate in the registry to "HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\W3SVC\\Parameters\\ADCLaunch" and verify that there is a key called **RDSServer.Datafactory**.</span></span> <span data-ttu-id="7e900-113">If not, create it.</span><span class="sxs-lookup"><span data-stu-id="7e900-113">If not, create it.</span></span>

5.  <span data-ttu-id="7e900-114">Wechseln Sie mit dem Internet Dienste-Manager zur Standardwebsite, und zeigen Sie die Eigenschaften des virtuellen MSADC-Stammverzeichnisses an.</span><span class="sxs-lookup"><span data-stu-id="7e900-114">Using Internet Services Manager, go to the default website and view the properties of the MSADC virtual root.</span></span> <span data-ttu-id="7e900-115">Überprüfen Sie die Einschränkungen für Verzeichnissicherheit, IP-Adressen und Domänennamen.</span><span class="sxs-lookup"><span data-stu-id="7e900-115">Inspect the Directory Security/IP Address and Domain Name Restrictions.</span></span> <span data-ttu-id="7e900-116">Wenn Zugriff verweigert aktiviert ist, aktivieren Gewährt.</span><span class="sxs-lookup"><span data-stu-id="7e900-116">If the "Access is Denied" is checked then select "Granted".</span></span>

<span data-ttu-id="7e900-117">Sie sollten den Server neu starten, wenn es zunächst den Anschein hat, dass das Problem durch die Änderungen nicht gelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="7e900-117">Be sure to try rebooting the server if the changes to do not appear to solve the problem at first.</span></span>

