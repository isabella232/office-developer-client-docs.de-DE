---
title: Konfigurieren von RDS unter Windows 2000
TOCTitle: Configuring RDS on Windows 2000
ms:assetid: eb2d4c1d-8b3b-07ac-258f-edb0b1a3daba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250193(v=office.15)
ms:contentKeyID: 48548482
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 80ce29ed129035dcb6799844a4b78509b976f0ee
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862940"
---
# <a name="configuring-rds-on-windows-2000"></a><span data-ttu-id="2347d-102">Konfigurieren von RDS unter Windows 2000</span><span class="sxs-lookup"><span data-stu-id="2347d-102">Configuring RDS on Windows 2000</span></span>


<span data-ttu-id="2347d-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2347d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2347d-104">Wenn es sich für Sie schwierig erweist, die Funktionsfähigkeit von RDS (Remote Data Service) nach eine Update auf Windows 2000 herzustellen, befolgen Sie die unten aufgeführten Schritte, um das Problem zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="2347d-104">If you experience difficulties getting RDS to function properly after upgrading to Windows 2000, follow the steps below to troubleshoot the issue.</span></span>

1.  <span data-ttu-id="2347d-105">Stellen Sie sicher, dass der WWW-Publishingdienst ersten ausgeführt wird, navigieren Sie zur https://*Server* mithilfe von Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="2347d-105">Make sure that the World Wide Web Publishing Service is running first by navigating to https://*server* using Internet Explorer.</span></span> <span data-ttu-id="2347d-106">Wenn Sie nicht auf den Webserver auf diese Weise zugreifen können, rufen Sie ein Eingabeaufforderungsfenster, und geben Sie den folgenden Befehl, "NET START W3SVC".</span><span class="sxs-lookup"><span data-stu-id="2347d-106">If you are unable to access the web server this way, go to a command prompt and enter the following command, "NET START W3SVC".</span></span>

2.  <span data-ttu-id="2347d-107">Wählen Sie im Startmenü ausführen aus.</span><span class="sxs-lookup"><span data-stu-id="2347d-107">From the Start menu, select Run.</span></span> <span data-ttu-id="2347d-108">Geben Sie msdfmap.ini, und klicken Sie auf OK, um die Datei "Msdfmap.ini" im Editor zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2347d-108">Type msdfmap.ini and click OK to open the msdfmap.ini file in Notepad.</span></span> <span data-ttu-id="2347d-109">Überprüfen Sie die \[CONNECT DEFAULT\] Abschnitt, und wenn der Parameter Zugriff auf NOACCESS festgelegt ist, ändern Sie ihn auf READONLY.</span><span class="sxs-lookup"><span data-stu-id="2347d-109">Check the \[CONNECT DEFAULT\] section, and if the ACCESS parameter is set to NOACCESS, change it to READONLY.</span></span>

3.  <span data-ttu-id="2347d-110">Navigieren Sie mithilfe des Dienstprogramms RegEdit zu "HKEY\_lokale\_Computer\\SOFTWARE\\Microsoft\\DataFactory\\HandlerInfo", und stellen Sie sicher, dass **DefaultHandler** auf 0 festgelegt ist und **HandlerRequired** "" (Null String).</span><span class="sxs-lookup"><span data-stu-id="2347d-110">Using the RegEdit utility, navigate to "HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\DataFactory\\HandlerInfo" and make sure **HandlerRequired** is set to 0 and **DefaultHandler** is "" (Null string).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="2347d-111">Wenn Sie diesen Abschnitt der Registrierung ändern, müssen Sie den WWW-Publishingdienst beenden und neu starten, indem Sie die folgenden Befehle an der Eingabeaufforderung eingeben: NET STOP W3SVC und NET START W3SVC.</span><span class="sxs-lookup"><span data-stu-id="2347d-111">If you make any changes to this section of the registry, you must stop and restart the World Wide Web Publishing Service by entering the following commands at a command prompt: "NET STOP W3SVC" and "NET START W3SVC".</span></span>

4.  <span data-ttu-id="2347d-112">Navigieren Sie mithilfe des Dienstprogramms RegEdit in der Registrierung auf "HKEY\_lokale\_Computer\\SYSTEM\\CurrentControlSet\\Services\\W3SVC\\Parameter\\ADCLaunch" und stellen Sie sicher, dass eine wichtige gewählte **vorhanden ist RDSServer.Datafactory**.</span><span class="sxs-lookup"><span data-stu-id="2347d-112">Using the RegEdit utility, navigate in the registry to "HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\W3SVC\\Parameters\\ADCLaunch" and verify that there is a key called **RDSServer.Datafactory**.</span></span> <span data-ttu-id="2347d-113">Wenn dies nicht der Fall ist, erstellen Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="2347d-113">If not, create it.</span></span>

<span data-ttu-id="2347d-114"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="2347d-114"><<<<<<< HEAD</span></span>
5.  <span data-ttu-id="2347d-115">Mithilfe des Internetdienste-Managers, wechseln Sie auf der Standardwebsite, und zeigen Sie die Eigenschaften des virtuellen Stammverzeichnisses MSADC.</span><span class="sxs-lookup"><span data-stu-id="2347d-115">Using Internet Services Manager, go to the Default Web Site and view the properties of the MSADC virtual root.</span></span> <span data-ttu-id="2347d-116">Untersuchen Sie die Directory Security-IP-Adresse und der Domäne Name Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="2347d-116">Inspect the Directory Security/IP Address and Domain Name Restrictions.</span></span> <span data-ttu-id="2347d-117">Wenn die "Zugriff verweigert" überprüft wird wählen Sie dann "Gewährt" aus.</span><span class="sxs-lookup"><span data-stu-id="2347d-117">If the "Access is Denied" is checked then select "Granted".</span></span>
=======
5.  <span data-ttu-id="2347d-118">Internetdienste-Manager verwenden, wechseln Sie zu der Standardwebsite, und zeigen Sie die Eigenschaften des virtuellen Stammverzeichnisses MSADC.</span><span class="sxs-lookup"><span data-stu-id="2347d-118">Using Internet Services Manager, go to the default website and view the properties of the MSADC virtual root.</span></span> <span data-ttu-id="2347d-119">Untersuchen Sie die Directory Security-IP-Adresse und der Domäne Name Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="2347d-119">Inspect the Directory Security/IP Address and Domain Name Restrictions.</span></span> <span data-ttu-id="2347d-120">Wenn die "Zugriff verweigert" überprüft wird wählen Sie dann "Gewährt" aus.</span><span class="sxs-lookup"><span data-stu-id="2347d-120">If the "Access is Denied" is checked then select "Granted".</span></span>
>>>>>>> <span data-ttu-id="2347d-121">master</span><span class="sxs-lookup"><span data-stu-id="2347d-121">master</span></span>

<span data-ttu-id="2347d-122">Sie sollten den Server neu starten, wenn es zunächst den Anschein hat, dass das Problem durch die Änderungen nicht gelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="2347d-122">Be sure to try rebooting the server if the changes to do not appear to solve the problem at first.</span></span>

