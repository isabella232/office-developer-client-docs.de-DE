---
title: DataFactory-Objekt (RDSServer)
TOCTitle: DataFactory object (RDSServer)
ms:assetid: 1de76cdd-34dc-8547-29aa-48ad6067bdea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248971(v=office.15)
ms:contentKeyID: 48543605
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77cd06992ef0062859d0a1372d115f8e65246a5d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702180"
---
# <a name="datafactory-object-rdsserver"></a><span data-ttu-id="8ba65-102">DataFactory-Objekt (RDSServer)</span><span class="sxs-lookup"><span data-stu-id="8ba65-102">DataFactory object (RDSServer)</span></span>


<span data-ttu-id="8ba65-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ba65-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8ba65-104">Dieses serverseitige Standardgeschäftsobjekt implementiert Methoden, die Lese-/Schreibzugriff auf festgelegte Datenquellen für clientseitige Anwendungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8ba65-104">This default server-side business object implements methods that provide read/write data access to specified data sources for client-side applications.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ba65-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8ba65-105">Remarks</span></span>

<span data-ttu-id="8ba65-106">Das **RDSServer.DataFactory** -Objekt ist als serverseitiges Automatisierungsobjekt konzipiert, das Clientanforderungen empfängt.</span><span class="sxs-lookup"><span data-stu-id="8ba65-106">The **RDSServer.DataFactory** object is designed as a server-side Automation object that receives client requests.</span></span> <span data-ttu-id="8ba65-107">In einer Internet-Implementierung befindet sich auf einem Webserver, und es wird von der Komponente ADISAPI instanziiert.</span><span class="sxs-lookup"><span data-stu-id="8ba65-107">In an Internet implementation, it resides on a web server and is instantiated by the ADISAPI component.</span></span> <span data-ttu-id="8ba65-108">Das **RDSServer.DataFactory** -Objekt bietet Lese-/Schreibzugriff auf angegebene Datenquellen, enthält aber keine Gültigkeitsprüfung oder Logik für Geschäftsregeln.</span><span class="sxs-lookup"><span data-stu-id="8ba65-108">The **RDSServer.DataFactory** object provides read and write access to specified data sources, but doesn't contain any validation or business rules logic.</span></span>

<span data-ttu-id="8ba65-p102">Wenn Sie eine Methode verwenden, die sowohl im **RDSServer.DataFactory** - als auch im [RDS.DataControl](datacontrol-object-rds.md)-Objekt verfügbar ist, verwendet Remote Data Service standardmäßig die **RDS.DataControl** -Version. Der Standard geht von einem grundlegenden Programmierszenario aus, bei dem das **RDSServer.DataFactory** -Objekt als generisches serverseitiges Geschäftsobjekt dient.</span><span class="sxs-lookup"><span data-stu-id="8ba65-p102">If you use a method that is available in both the **RDSServer.DataFactory** and [RDS.DataControl](datacontrol-object-rds.md) objects, Remote Data Service uses the **RDS.DataControl** version by default. The default assumes a basic programming scenario, where the **RDSServer.DataFactory** serves as a generic server-side business object.</span></span>

<span data-ttu-id="8ba65-111">Wenn Sie die Webanwendung aufgabenspezifische serverseitige Verarbeitung behandeln möchten, können Sie das **RDSServer.DataFactory-Objekts** mit einem benutzerdefinierten Geschäftsobjekt ersetzen.</span><span class="sxs-lookup"><span data-stu-id="8ba65-111">If you want your web application to handle task-specific server-side processing, you can replace the **RDSServer.DataFactory** with a custom business object.</span></span>

<span data-ttu-id="8ba65-p103">Sie können serverseitige Geschäftsobjekte erstellen, die die **RDSServer.DataFactory** -Methoden aufrufen, wie etwa [Query](query-method-rds.md) und [CreateRecordset](createrecordset-method-rds.md). Dies ist nützlich, wenn Sie den Geschäftsobjekten eine bestimmte Funktionalität hinzufügen und gleichzeitig vorhandene Remote Data Service-Technologien nutzen wollen.</span><span class="sxs-lookup"><span data-stu-id="8ba65-p103">You can create server-side business objects that call the **RDSServer.DataFactory** methods, such as [Query](query-method-rds.md) and [CreateRecordset](createrecordset-method-rds.md). This is helpful if you want to add functionality to your business objects, but take advantage of existing Remote Data Service technologies.</span></span>

<span data-ttu-id="8ba65-114">Die Klassen-ID für das **RDSServer.DataFactory** -Objekt lautet 9381D8F5-0288-11D0-9501-00AA00B911A5.</span><span class="sxs-lookup"><span data-stu-id="8ba65-114">The class ID for the **RDSServer.DataFactory** object is 9381D8F5-0288-11D0-9501-00AA00B911A5.</span></span>

