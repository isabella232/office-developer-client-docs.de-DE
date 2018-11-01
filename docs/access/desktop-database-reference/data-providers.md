---
title: Datenanbieter (Access PC-Datenbank-Referenz)
TOCTitle: Data Providers
ms:assetid: c1e36245-4ece-4986-db30-dc4be3daa794
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249946(v=office.15)
ms:contentKeyID: 48547540
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b4b3497493627f5446055d50e525882e5187807
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886158"
---
# <a name="data-providers"></a><span data-ttu-id="0fb6d-102">Data Providers</span><span class="sxs-lookup"><span data-stu-id="0fb6d-102">Data Providers</span></span>


<span data-ttu-id="0fb6d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0fb6d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0fb6d-p101">Datenprovider stellen unterschiedliche Datenquellen wie SQL-Datenbanken, indiziert-sequenzielle Dateien, Kalkulationstabellen, Dokumentspeicher und E-Mail-Dateien dar. Datenprovider machen Daten mithilfe eines so genannten Rowsets einheitlich verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0fb6d-p101">Data providers represent diverse sources of data such as SQL databases, indexed-sequential files, spreadsheets, document stores, and mail files. Providers expose data uniformly using a common abstraction called the rowset.</span></span>

<span data-ttu-id="0fb6d-p102">ADO ist leistungsfähig und flexibel, weil damit auf mehrere verschiedene Datenprovider zugegriffen und dennoch dasselbe Programmiermodell verfügbar gemacht werden kann, unabhängig von den jeweiligen Features eines bestimmten Datenproviders. Da sich jedoch jeder Datenprovider unterscheidet, hängt die Interaktionsweise der Anwendung mit ADO vom jeweiligen Datenprovider ab.</span><span class="sxs-lookup"><span data-stu-id="0fb6d-p102">ADO is powerful and flexible because it can connect to any of several different data providers and still expose the same programming model, regardless of the specific features of any given provider. However, because each data provider is unique, how your application interacts with ADO will vary by data provider.</span></span>

<span data-ttu-id="0fb6d-108">Beispielsweise sind die Funktionen und Features von den OLE DB-Anbieter für SQL Server, die Zugriff auf Microsoft SQL Server-Datenbanken verwendet wird, erheblich sich von denen des Microsoft OLE DB-Anbieter für Internet Publishing, mit dem Datei Zugriff auf verwendet wird speichert auf einem Webserver.</span><span class="sxs-lookup"><span data-stu-id="0fb6d-108">For example, the capabilities and features of the OLE DB Provider for SQL Server, which is used to access Microsoft SQL Server databases, are considerably different from those of the Microsoft OLE DB Provider for Internet Publishing, which is used to access file stores on a web server.</span></span>

