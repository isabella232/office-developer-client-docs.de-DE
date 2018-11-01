---
title: Dienstanbieter und Komponenten
TOCTitle: Service Providers and Components
ms:assetid: e42d9c84-525a-4aca-01b2-88e3f2b0717f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250163(v=office.15)
ms:contentKeyID: 48548333
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d215c7c66c489e54d513941604b1c66c0e9094c1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881209"
---
# <a name="service-providers-and-components"></a><span data-ttu-id="dd14d-102">Dienstanbieter und Komponenten</span><span class="sxs-lookup"><span data-stu-id="dd14d-102">Service Providers and Components</span></span>


<span data-ttu-id="dd14d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dd14d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dd14d-104">Dienstanbieter sind Komponenten, die die Funktionalität von Datenprovidern erweitern, indem erweiterte Schnittstellen implementiert werden, die vom Datenspeicher systemintern nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="dd14d-104">Service providers are components that extend the functionality of data providers by implementing extended interfaces that are not natively supported by the data store.</span></span>

<span data-ttu-id="dd14d-105">Microsoft Data Access bietet eine *Komponentenarchitektur* , die einzelne, spezialisierte Komponenten implementieren diskrete können Datenbankfunktionalität oder "Dienste" auf der Basis weniger leistungsfähige Speicher-Sätze.</span><span class="sxs-lookup"><span data-stu-id="dd14d-105">Microsoft Data Access provides a *component architecture* that allows individual, specialized components to implement discrete sets of database functionality, or "services," on top of less capable stores.</span></span> <span data-ttu-id="dd14d-106">Auf diese Weise statt erzwingen jedes Datenspeicher auf eine eigenen Implementierung von erweiterten Funktionen bereit, oder erzwingen, dass generische Applications Datenbankfunktionalität intern implementieren, Dienstkomponenten eine allgemeine Implementierung bereit, die jeder Anwendung können Verwenden Sie beim Zugriff auf jeden beliebigen Datenspeicher.</span><span class="sxs-lookup"><span data-stu-id="dd14d-106">Thus, rather than forcing each data store to provide its own implementation of extended functionality or forcing generic applications to implement database functionality internally, service components provide a common implementation that any application can use when accessing any data store.</span></span> <span data-ttu-id="dd14d-107">Die Tatsache, dass einige Funktionen systemintern vom Datenspeicher und durch allgemeine Komponenten implementiert wird, ist für die Anwendung transparent.</span><span class="sxs-lookup"><span data-stu-id="dd14d-107">The fact that some functionality is implemented natively by the data store and some through generic components is transparent to the application.</span></span>

<span data-ttu-id="dd14d-p102">Beispielsweise ist ein Cursormodul wie z. B. der Microsoft Cursor Service für OLE DB eine Dienstkomponente, die Daten eines sequenziellen Vorwärtscursor-Datenspeichers verwenden kann, um Daten zu erstellen, für die ein Bildlauf ausgeführt werden kann. Weitere von ADO häufig verwendete Dienstanbieter sind der Microsoft OLE DB-Anbieter für Persistenz (zum Speichern von Daten in einer Datei), der Microsoft Data Shaping Dienst für OLE DB (für hierarchische **Recordset**-Objekte) und der Microsoft OLE DB-Anbieter für Remoting (zum Aufrufen von Datenprovidern auf einem Remotecomputer).</span><span class="sxs-lookup"><span data-stu-id="dd14d-p102">For example, a cursor engine, such as the Microsoft Cursor Service for OLE DB, is a service component that can consume data from a sequential, forward-only data store to produce scrollable data. Other service providers commonly used by ADO include the Microsoft OLE DB Persistence Provider (for saving data to a file), the Microsoft Data Shaping Service for OLE DB (for hierarchical **Recordsets**), and the Microsoft OLE DB Remoting Provider (for invoking data providers on a remote computer).</span></span>

<span data-ttu-id="dd14d-110">Weitere Informationen zu Dienstanbietern und Datenprovidern finden Sie in [Anhang A: Anbieter](appendix-a-providers.md).</span><span class="sxs-lookup"><span data-stu-id="dd14d-110">For more information about service and data providers, see [Appendix A: Providers](appendix-a-providers.md).</span></span>

