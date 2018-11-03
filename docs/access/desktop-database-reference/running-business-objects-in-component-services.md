---
title: Ausführen von Geschäftsobjekten in Komponentendiensten
TOCTitle: Running business objects in component services
ms:assetid: 12103458-b1dd-10fc-37e8-883fd6c6b9d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248893(v=office.15)
ms:contentKeyID: 48543328
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3dbf3c88f140210228a1bb3d6d0341d6bde42aa2
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944116"
---
# <a name="running-business-objects-in-component-services"></a><span data-ttu-id="95c8a-102">Ausführen von Geschäftsobjekten in Komponentendiensten</span><span class="sxs-lookup"><span data-stu-id="95c8a-102">Running business objects in component services</span></span>

<span data-ttu-id="95c8a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="95c8a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="95c8a-p101">Bei Geschäftsobjekten kann es sich um ausführbare Dateien (EXE) oder um Dynamic Link Libraries (DLL) handeln. Die für die Ausführung eines Geschäftsobjekts verwendete Konfiguration hängt davon ab, ob das Objekt eine DLL- oder eine EXE-Datei ist:</span><span class="sxs-lookup"><span data-stu-id="95c8a-p101">Business objects can be executable files (.exe) or dynamic-link libraries (.dll). The configuration you use to run the business object depends on whether the object is a .dll or .exe file:</span></span>

  - <span data-ttu-id="95c8a-p102">Als EXE-Dateien erstellte Geschäftsobjekte können über DCOM aufgerufen werden. Wenn diese Geschäftobjekte mit Internetinformationsdienste (Internet Information Services, IIS) verwendet werden, unterliegen sie einem zusätzlichen Marshalling der Daten. Dadurch wird die Leistung des Clients verringert.</span><span class="sxs-lookup"><span data-stu-id="95c8a-p102">Business objects created as .exe files can be called through DCOM. If these business objects are used through Internet Information Services (IIS), they are subject to additional marshalingof data, which will slow client performance.</span></span>

  - <span data-ttu-id="95c8a-p103">Als DLL-Dateien erstellte Geschäftsobjekte können über IIS (und damit über HTTP ) verwendet werden. Über DCOM können sie nur mithilfe der Komponentendienste (oder Microsoft Transaction Server unter Windows NT) verwendet werden. Geschäftobjekt-DLLs müssen auf dem IIS-Servercomputer registriert werden, damit ein Zugriff über IIS möglich ist. (Schritte zum Konfigurieren einer DLL für die Ausführung mit DCOM finden Sie im Abschnitt [Aktivieren einer DLL für die Ausführung mit DCOM](enabling-a-dll-to-run-on-dcom.md).)</span><span class="sxs-lookup"><span data-stu-id="95c8a-p103">Business objects created as .dll files can be used via IIS (and therefore HTTP). They can also be used over DCOM only via Component Services (or Microsoft Transaction Server, if you are using Windows NT). Business object DLLs will need to be registered on the IIS server computer to give you accessibility via IIS. (For steps on how to configure a DLL to run on DCOM, see the section, "[Enabling a DLL to Run on DCOM](enabling-a-dll-to-run-on-dcom.md).")</span></span>


> [!NOTE]
> <span data-ttu-id="95c8a-112">Wenn von Geschäftsobjekten auf der mittleren Ebene als Komponenten der Komponentendienste (mit **GetObjectContext**, **SetComplete**und **SetAbort**) implementiert werden, können sie Komponentendienste (oder MTS, bei Verwendung der Windows NT)-Objekte Kontext Verwalten von deren Status über mehrere Client-Anrufe.</span><span class="sxs-lookup"><span data-stu-id="95c8a-112">When business objects on the middle tier are implemented as Component Services components (using **GetObjectContext**, **SetComplete**, and **SetAbort**), they can use Component Services (or MTS, if you are using Windows NT) context objects to maintain their state across multiple client calls.</span></span> <span data-ttu-id="95c8a-113">Dieses Szenario ist mit DCOM möglich, das üblicherweise zwischen vertrauenswürdigen Clients und Servern (ein Intranet) implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="95c8a-113">This scenario is possible with DCOM, which is typically implemented between trusted clients and servers (an intranet).</span></span> 
>
> <span data-ttu-id="95c8a-114">In diesem Fall werden das [RDS.DataSpace](dataspace-object-rds.md)-Objekt und die [CreateObject](createobject-method-rds.md)-Methode auf dem Client durch das Transaktionskontextobjekt und die **CreateInstance** -Methode ersetzt (bereitgestellt von der **ITransactionContext** -Schnittstelle), die von den Komponentendiensten implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="95c8a-114">In this case, the [RDS.DataSpace](dataspace-object-rds.md) object and [CreateObject](createobject-method-rds.md) method on the client side are replaced by the transaction context object and **CreateInstance** method (provided by the **ITransactionContext** interface), implemented by Component Services.</span></span>


## <a name="see-also"></a><span data-ttu-id="95c8a-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95c8a-115">See also</span></span>

- [<span data-ttu-id="95c8a-116">Ausführen von Geschäftsobjekten in Komponentendiensten (SQLServer)</span><span class="sxs-lookup"><span data-stu-id="95c8a-116">Running Business Objects in Component Services (SQL Server)</span></span>](https://docs.microsoft.com/sql/ado/guide/remote-data-service/running-business-objects-in-component-services?view=sql-server-2017)