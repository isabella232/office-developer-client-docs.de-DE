---
title: Lösungen für Remotedatenzugriff
TOCTitle: Solutions for Remote Data Access
ms:assetid: ae84c05a-cf9b-2b4c-4d7a-e6c9dcd120c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249825(v=office.15)
ms:contentKeyID: 48547072
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c03a6495b6d95723469d14dc1c3d9d2972760865
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937169"
---
# <a name="solutions-for-remote-data-access"></a><span data-ttu-id="e335d-102">Lösungen für Remotedatenzugriff</span><span class="sxs-lookup"><span data-stu-id="e335d-102">Solutions for Remote Data Access</span></span>


<span data-ttu-id="e335d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e335d-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="the-issue"></a><span data-ttu-id="e335d-104">Das Problem</span><span class="sxs-lookup"><span data-stu-id="e335d-104">The Issue</span></span>

<span data-ttu-id="e335d-p101">Mit ADO ist es möglich, über die Anwendung direkt auf Datenquellen zuzugreifen und sie zu ändern (wird manchmal als zweistufiges System bezeichnet). Wenn die Verbindung z. B. mit der Datenquelle hergestellt wird, die die Daten enthält, handelt es sich um eine direkte Verbindung in einem zweistufigen System.</span><span class="sxs-lookup"><span data-stu-id="e335d-p101">ADO enables your application to directly gain access to and modify data sources (sometimes called a two-tier system). For example, if your connection is to the data source that contains your data, that is a direct connection in a two-tier system.</span></span>

<span data-ttu-id="e335d-107">Sie möchten jedoch indirekt Zugriff auf Datenquellen über die Vermittlung wie beispielsweise Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="e335d-107">However, you may want to access data sources indirectly through an intermediary such as Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="e335d-108">Diese Anordnung wird manchmal als dreistufiges System bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e335d-108">This arrangement is sometimes called a three-tier system.</span></span> <span data-ttu-id="e335d-109">IIS ist ein Client-/Server-System, durch das eine effiziente Möglichkeit bereitgestellt wird, mit einer lokalen Anwendung oder Clientanwendung ein Remoteprogramm oder Serverprogramm über das Internet oder ein Intranet aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="e335d-109">IIS is a client/server system that provides an efficient way for a local, or client, application to invoke a remote, or server, program across the Internet or an intranet.</span></span> <span data-ttu-id="e335d-110">Durch das Serverprogramm wird auf die Datenquelle zugegriffen, und optional werden die erfassten Daten verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e335d-110">The server program gains access to the data source and optionally processes the acquired data.</span></span>

<span data-ttu-id="e335d-111">Beispielsweise enthält Ihre Intranet-Webseite eine Anwendung in Microsoft Visual Basic Scripting Edition (VBScript), das mit IIS verbindet geschrieben.</span><span class="sxs-lookup"><span data-stu-id="e335d-111">For example, your intranet webpage contains an application written in Microsoft Visual Basic Scripting Edition (VBScript), which connects to IIS.</span></span> <span data-ttu-id="e335d-112">IIS wiederum eine Verbindung mit der tatsächlichen Datenquelle, ruft die Daten, auf irgendeine Weise verarbeitet und gibt dann die verarbeitete Informationen zu Ihrer Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="e335d-112">IIS in turn connects to the actual data source, retrieves the data, processes it in some way, and then returns the processed information to your application.</span></span>

<span data-ttu-id="e335d-p104">In diesem Beispiel wurde durch die Anwendung nie direkt eine Verbindung mit der Datenquelle hergestellt; dies erfolgte über IIS. Und durch IIS wurde mithilfe von ADO auf die Daten zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="e335d-p104">In this example, your application never directly connected to the data source; IIS did. And IIS accessed the data by means of ADO.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e335d-p105">[!HINWEIS] Die Client-/Serveranwendung muss nicht auf dem Internet oder einem Intranet basieren (d. h. webbasiert sein) - sie kann ausschließlich aus kompilierten Programmen in einem lokalen Netzwerk bestehen. Der typische Fall ist jedoch eine webbasierte Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e335d-p105">The client/server application does not have to be based on the Internet or an intranet (that is, Web-based) — it could consist solely of compiled programs on a local area network. However, the typical case is a Web-based application.</span></span></P>



<span data-ttu-id="e335d-117">Da die zurückgegebenen Informationen möglicherweise von manchen visuellen Steuerelementen, z. B. von Rastern, Kontrollkästchen oder Listen, verwendet werden, müssen die zurückgegebenen Informationen leicht durch ein visuelles Steuerelement verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="e335d-117">Because some visual control, such as a grid, check box, or list, may use the returned information, the returned information must be easily used by a visual control.</span></span>

<span data-ttu-id="e335d-p106">Sie benötigen eine einfache und effiziente Anwendungsprogrammierschnittstelle, von der dreistufige Systeme unterstützt und Informationen so einfach zurückgegeben werden, als seien sie auf einem zweistufigen System abgerufen worden. Diese Schnittstelle ist Remote Data Service (RDS).</span><span class="sxs-lookup"><span data-stu-id="e335d-p106">You want a simple and efficient application-programming interface that supports three-tier systems, and returns information as easily as if it had been retrieved on a two-tier system. Remote Data Service (RDS) is this interface.</span></span>

## <a name="the-solution"></a><span data-ttu-id="e335d-120">Die Lösung</span><span class="sxs-lookup"><span data-stu-id="e335d-120">The Solution</span></span>

<span data-ttu-id="e335d-p107">Durch RDS wird ein Programmiermodell definiert - die Reihenfolge der Aktivitäten, die notwendig sind, um auf eine Datenquelle zuzugreifen und sie zu aktualisieren -, um über einen Vermittler auf Daten zuzugreifen, z. B. über Internetinformationsdienste (Internet Information Services, IIS). Im Programmiermodell wird die gesamte Funktionalität von RDS zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="e335d-p107">RDS defines a programming model — the sequence of activities necessary to gain access to and update a data source — to gain access to data through an intermediary, such as Internet Information Services (IIS). The programming model summarizes the entire functionality of RDS.</span></span>

