---
title: Lösungen für Remotedatenzugriff
TOCTitle: Solutions for Remote Data Access
ms:assetid: ae84c05a-cf9b-2b4c-4d7a-e6c9dcd120c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249825(v=office.15)
ms:contentKeyID: 48547072
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef617f91aa6f36969932a4d8f2914df2de935787
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998161"
---
# <a name="solutions-for-remote-data-access"></a><span data-ttu-id="721e6-102">Lösungen für Remotedatenzugriff</span><span class="sxs-lookup"><span data-stu-id="721e6-102">Solutions for Remote Data Access</span></span>

<span data-ttu-id="721e6-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="721e6-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="the-issue"></a><span data-ttu-id="721e6-104">Das Problem</span><span class="sxs-lookup"><span data-stu-id="721e6-104">The issue</span></span>

<span data-ttu-id="721e6-p101">Mit ADO ist es möglich, über die Anwendung direkt auf Datenquellen zuzugreifen und sie zu ändern (wird manchmal als zweistufiges System bezeichnet). Wenn die Verbindung z. B. mit der Datenquelle hergestellt wird, die die Daten enthält, handelt es sich um eine direkte Verbindung in einem zweistufigen System.</span><span class="sxs-lookup"><span data-stu-id="721e6-p101">ADO enables your application to directly gain access to and modify data sources (sometimes called a two-tier system). For example, if your connection is to the data source that contains your data, that is a direct connection in a two-tier system.</span></span>

<span data-ttu-id="721e6-107">Sie möchten jedoch indirekt Zugriff auf Datenquellen über die Vermittlung wie beispielsweise Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="721e6-107">However, you may want to access data sources indirectly through an intermediary such as Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="721e6-108">Diese Anordnung wird manchmal als dreistufiges System bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="721e6-108">This arrangement is sometimes called a three-tier system.</span></span> <span data-ttu-id="721e6-109">IIS ist ein Client-/Server-System, durch das eine effiziente Möglichkeit bereitgestellt wird, mit einer lokalen Anwendung oder Clientanwendung ein Remoteprogramm oder Serverprogramm über das Internet oder ein Intranet aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="721e6-109">IIS is a client/server system that provides an efficient way for a local, or client, application to invoke a remote, or server, program across the Internet or an intranet.</span></span> <span data-ttu-id="721e6-110">Durch das Serverprogramm wird auf die Datenquelle zugegriffen, und optional werden die erfassten Daten verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="721e6-110">The server program gains access to the data source and optionally processes the acquired data.</span></span>

<span data-ttu-id="721e6-111">Beispielsweise enthält Ihre Intranet-Webseite eine Anwendung in Microsoft Visual Basic Scripting Edition (VBScript), das mit IIS verbindet geschrieben.</span><span class="sxs-lookup"><span data-stu-id="721e6-111">For example, your intranet webpage contains an application written in Microsoft Visual Basic Scripting Edition (VBScript), which connects to IIS.</span></span> <span data-ttu-id="721e6-112">IIS wiederum eine Verbindung mit der tatsächlichen Datenquelle, ruft die Daten, auf irgendeine Weise verarbeitet und gibt dann die verarbeitete Informationen zu Ihrer Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="721e6-112">IIS in turn connects to the actual data source, retrieves the data, processes it in some way, and then returns the processed information to your application.</span></span>

<span data-ttu-id="721e6-p104">In diesem Beispiel wurde durch die Anwendung nie direkt eine Verbindung mit der Datenquelle hergestellt; dies erfolgte über IIS. Und durch IIS wurde mithilfe von ADO auf die Daten zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="721e6-p104">In this example, your application never directly connected to the data source; IIS did. And IIS accessed the data by means of ADO.</span></span>

> [!NOTE]
> <span data-ttu-id="721e6-115">Die Client/Server-Anwendung muss nicht auf das Internet oder Intranet basieren (d. h., webbasierte) – Es konnte bestehen kompilierte Programme auf einem lokalen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="721e6-115">The client/server application does not have to be based on the Internet or an intranet (that is, web-based)—it could consist solely of compiled programs on a local area network.</span></span> <span data-ttu-id="721e6-116">Jedoch ist der typische Fall eine webbasierte Anwendung.</span><span class="sxs-lookup"><span data-stu-id="721e6-116">However, the typical case is a web-based application.</span></span>

<span data-ttu-id="721e6-117">Da die zurückgegebenen Informationen möglicherweise von manchen visuellen Steuerelementen, z. B. von Rastern, Kontrollkästchen oder Listen, verwendet werden, müssen die zurückgegebenen Informationen leicht durch ein visuelles Steuerelement verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="721e6-117">Because some visual control, such as a grid, check box, or list, may use the returned information, the returned information must be easily used by a visual control.</span></span>

<span data-ttu-id="721e6-p106">Sie benötigen eine einfache und effiziente Anwendungsprogrammierschnittstelle, von der dreistufige Systeme unterstützt und Informationen so einfach zurückgegeben werden, als seien sie auf einem zweistufigen System abgerufen worden. Diese Schnittstelle ist Remote Data Service (RDS).</span><span class="sxs-lookup"><span data-stu-id="721e6-p106">You want a simple and efficient application-programming interface that supports three-tier systems, and returns information as easily as if it had been retrieved on a two-tier system. Remote Data Service (RDS) is this interface.</span></span>

## <a name="the-solution"></a><span data-ttu-id="721e6-120">Die Lösung</span><span class="sxs-lookup"><span data-stu-id="721e6-120">The solution</span></span>

<span data-ttu-id="721e6-121">RDS definiert ein Programmiermodell – die Reihenfolge der Aktivitäten, die erforderlich sind, um den Zugriff auf und Aktualisieren einer Datenquelle – den Zugriff auf Daten über die Vermittlung, wie Internetinformationsdienste (Internet Information Services, IIS).</span><span class="sxs-lookup"><span data-stu-id="721e6-121">RDS defines a programming model—the sequence of activities necessary to gain access to and update a data source — to gain access to data through an intermediary, such as Internet Information Services (IIS).</span></span> <span data-ttu-id="721e6-122">Das Programmiermodell zusammengefasst, die gesamte Funktionalität von RDS.</span><span class="sxs-lookup"><span data-stu-id="721e6-122">The programming model summarizes the entire functionality of RDS.</span></span>

