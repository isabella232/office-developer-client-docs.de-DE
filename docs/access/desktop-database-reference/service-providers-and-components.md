---
title: Dienstanbieter und Komponenten
TOCTitle: Service Providers and Components
ms:assetid: e42d9c84-525a-4aca-01b2-88e3f2b0717f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250163(v=office.15)
ms:contentKeyID: 48548333
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 03447b9977c74484eb7455a75fc2255c33c5e4c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308701"
---
# <a name="service-providers-and-components"></a><span data-ttu-id="9712c-102">Dienstanbieter und Komponenten</span><span class="sxs-lookup"><span data-stu-id="9712c-102">Service providers and components</span></span>


<span data-ttu-id="9712c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9712c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9712c-104">Dienstanbieter sind Komponenten, die die Funktionalität von Datenprovidern erweitern, indem erweiterte Schnittstellen implementiert werden, die vom Datenspeicher systemintern nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="9712c-104">Service providers are components that extend the functionality of data providers by implementing extended interfaces that are not natively supported by the data store.</span></span>

<span data-ttu-id="9712c-p101">Microsoft Data Access stellt eine *Komponentenarchitektur* bereit, mit der einzelne, spezialisierte Komponenten für weniger leistungsfähige Datenspeicher eigenständige Datenbankfunktionalität oder "Dienste" implementieren können. Anstatt also für jeden Datenspeicher eine eigene Implementierung erweiterter Funktionalität bzw. für einfache Anwendungen die interne Implementierung von Datenbankfunktionalität zu erzwingen, stellen Dienstkomponenten eine allgemeine Implementierung bereit, die von jeder Anwendung beim Zugriff auf einen beliebigen Datenspeicher verwendet werden kann. Die Tatsache, dass bestimmte Funktionen systemintern durch den Datenspeicher sowie durch allgemeine Komponenten implementiert werden, ist im Hinblick auf die Anwendung transparent.</span><span class="sxs-lookup"><span data-stu-id="9712c-p101">Microsoft Data Access provides a *component architecture* that allows individual, specialized components to implement discrete sets of database functionality, or "services," on top of less capable stores. Thus, rather than forcing each data store to provide its own implementation of extended functionality or forcing generic applications to implement database functionality internally, service components provide a common implementation that any application can use when accessing any data store. The fact that some functionality is implemented natively by the data store and some through generic components is transparent to the application.</span></span>

<span data-ttu-id="9712c-p102">Beispielsweise ist ein Cursormodul wie z. B. der Microsoft Cursor Service für OLE DB eine Dienstkomponente, die Daten eines sequenziellen Vorwärtscursor-Datenspeichers verwenden kann, um Daten zu erstellen, für die ein Bildlauf ausgeführt werden kann. Weitere von ADO häufig verwendete Dienstanbieter sind der Microsoft OLE DB-Anbieter für Persistenz (zum Speichern von Daten in einer Datei), der Microsoft Data Shaping Dienst für OLE DB (für hierarchische **Recordset**-Objekte) und der Microsoft OLE DB-Anbieter für Remoting (zum Aufrufen von Datenprovidern auf einem Remotecomputer).</span><span class="sxs-lookup"><span data-stu-id="9712c-p102">For example, a cursor engine, such as the Microsoft Cursor Service for OLE DB, is a service component that can consume data from a sequential, forward-only data store to produce scrollable data. Other service providers commonly used by ADO include the Microsoft OLE DB Persistence Provider (for saving data to a file), the Microsoft Data Shaping Service for OLE DB (for hierarchical **Recordsets**), and the Microsoft OLE DB Remoting Provider (for invoking data providers on a remote computer).</span></span>

<span data-ttu-id="9712c-110">Weitere Informationen zu Dienstanbietern und Datenprovidern finden Sie in [Anhang A: Anbieter](appendix-a-providers.md).</span><span class="sxs-lookup"><span data-stu-id="9712c-110">For more information about service and data providers, see [Appendix A: Providers](appendix-a-providers.md).</span></span>

