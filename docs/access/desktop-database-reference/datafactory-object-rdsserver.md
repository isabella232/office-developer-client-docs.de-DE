---
title: DataFactory-Objekt (RDSServer)
TOCTitle: DataFactory Object (RDSServer)
ms:assetid: 1de76cdd-34dc-8547-29aa-48ad6067bdea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248971(v=office.15)
ms:contentKeyID: 48543605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2249ea154ac40b9114dd3dab8006a6d26539adff
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605660"
---
# <a name="datafactory-object-rdsserver"></a><span data-ttu-id="c1a85-102">DataFactory-Objekt (RDSServer)</span><span class="sxs-lookup"><span data-stu-id="c1a85-102">DataFactory Object (RDSServer)</span></span>


<span data-ttu-id="c1a85-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c1a85-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c1a85-104">Dieses serverseitige Standardgeschäftsobjekt implementiert Methoden, die Lese-/Schreibzugriff auf festgelegte Datenquellen für clientseitige Anwendungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c1a85-104">This default server-side business object implements methods that provide read/write data access to specified data sources for client-side applications.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1a85-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c1a85-105">Remarks</span></span>

<span data-ttu-id="c1a85-106"><<<<<<< HEAD **RDSServer.DataFactory** -Objekt dient als serverseitigen Automatisierungsobjekt, das Clientanforderungen empfängt.</span><span class="sxs-lookup"><span data-stu-id="c1a85-106"><<<<<<< HEAD The **RDSServer.DataFactory** object is designed as a server-side Automation object that receives client requests.</span></span> <span data-ttu-id="c1a85-107">In einer Internet-Implementierung befindet es sich auf einem Webserver und wird von der ADISAPI-Komponente instanziiert.</span><span class="sxs-lookup"><span data-stu-id="c1a85-107">In an Internet implementation, it resides on a Web server and is instantiated by the ADISAPI component.</span></span> <span data-ttu-id="c1a85-108">Das **RDSServer.DataFactory** -Objekt bietet Lese-/Schreibzugriff auf angegebene Datenquellen, enthält aber keine Gültigkeitsprüfung oder Logik für Geschäftsregeln.</span><span class="sxs-lookup"><span data-stu-id="c1a85-108">The **RDSServer.DataFactory** object provides read and write access to specified data sources, but doesn't contain any validation or business rules logic.</span></span>

<span data-ttu-id="c1a85-p102">Wenn Sie eine Methode verwenden, die sowohl im **RDSServer.DataFactory** - als auch im [RDS.DataControl](datacontrol-object-rds.md)-Objekt verfügbar ist, verwendet Remote Data Service standardmäßig die **RDS.DataControl** -Version. Der Standard geht von einem grundlegenden Programmierszenario aus, bei dem das **RDSServer.DataFactory** -Objekt als generisches serverseitiges Geschäftsobjekt dient.</span><span class="sxs-lookup"><span data-stu-id="c1a85-p102">If you use a method that is available in both the **RDSServer.DataFactory** and [RDS.DataControl](datacontrol-object-rds.md) objects, Remote Data Service uses the **RDS.DataControl** version by default. The default assumes a basic programming scenario, where the **RDSServer.DataFactory** serves as a generic server-side business object.</span></span>

<a name="if-you-want-your-web-application-to-handle-task-specific-server-side-processing-you-can-replace-the-rdsserverdatafactory-with-a-custom-business-object"></a><span data-ttu-id="c1a85-111">Wenn die Webanwendung eine aufgabenspezifische serverseitige Verarbeitung erfordert, können Sie das **RDSServer.DataFactory** -Objekt durch ein angepasstes Geschäftsobjekt ersetzen.</span><span class="sxs-lookup"><span data-stu-id="c1a85-111">If you want your Web application to handle task-specific server-side processing, you can replace the **RDSServer.DataFactory** with a custom business object.</span></span>
=======
<span data-ttu-id="c1a85-112">Das **RDSServer.DataFactory** -Objekt ist als serverseitiges Automatisierungsobjekt konzipiert, das Clientanforderungen empfängt.</span><span class="sxs-lookup"><span data-stu-id="c1a85-112">The **RDSServer.DataFactory** object is designed as a server-side Automation object that receives client requests.</span></span> <span data-ttu-id="c1a85-113">In einer Internet-Implementierung befindet sich auf einem Webserver, und es wird von der Komponente ADISAPI instanziiert.</span><span class="sxs-lookup"><span data-stu-id="c1a85-113">In an Internet implementation, it resides on a web server and is instantiated by the ADISAPI component.</span></span> <span data-ttu-id="c1a85-114">Das **RDSServer.DataFactory** -Objekt bietet Lese-/Schreibzugriff auf angegebene Datenquellen, enthält aber keine Gültigkeitsprüfung oder Logik für Geschäftsregeln.</span><span class="sxs-lookup"><span data-stu-id="c1a85-114">The **RDSServer.DataFactory** object provides read and write access to specified data sources, but doesn't contain any validation or business rules logic.</span></span>

<span data-ttu-id="c1a85-p104">Wenn Sie eine Methode verwenden, die sowohl im **RDSServer.DataFactory** - als auch im [RDS.DataControl](datacontrol-object-rds.md)-Objekt verfügbar ist, verwendet Remote Data Service standardmäßig die **RDS.DataControl** -Version. Der Standard geht von einem grundlegenden Programmierszenario aus, bei dem das **RDSServer.DataFactory** -Objekt als generisches serverseitiges Geschäftsobjekt dient.</span><span class="sxs-lookup"><span data-stu-id="c1a85-p104">If you use a method that is available in both the **RDSServer.DataFactory** and [RDS.DataControl](datacontrol-object-rds.md) objects, Remote Data Service uses the **RDS.DataControl** version by default. The default assumes a basic programming scenario, where the **RDSServer.DataFactory** serves as a generic server-side business object.</span></span>

<span data-ttu-id="c1a85-117">Wenn Sie die Webanwendung aufgabenspezifische serverseitige Verarbeitung behandeln möchten, können Sie das **RDSServer.DataFactory-Objekts** mit einem benutzerdefinierten Geschäftsobjekt ersetzen.</span><span class="sxs-lookup"><span data-stu-id="c1a85-117">If you want your web application to handle task-specific server-side processing, you can replace the **RDSServer.DataFactory** with a custom business object.</span></span>
>>>>>>> <span data-ttu-id="c1a85-118">master</span><span class="sxs-lookup"><span data-stu-id="c1a85-118">master</span></span>

<span data-ttu-id="c1a85-p105">Sie können serverseitige Geschäftsobjekte erstellen, die die **RDSServer.DataFactory** -Methoden aufrufen, wie etwa [Query](query-method-rds.md) und [CreateRecordset](createrecordset-method-rds.md). Dies ist nützlich, wenn Sie den Geschäftsobjekten eine bestimmte Funktionalität hinzufügen und gleichzeitig vorhandene Remote Data Service-Technologien nutzen wollen.</span><span class="sxs-lookup"><span data-stu-id="c1a85-p105">You can create server-side business objects that call the **RDSServer.DataFactory** methods, such as [Query](query-method-rds.md) and [CreateRecordset](createrecordset-method-rds.md). This is helpful if you want to add functionality to your business objects, but take advantage of existing Remote Data Service technologies.</span></span>

<span data-ttu-id="c1a85-121">Die Klassen-ID für das **RDSServer.DataFactory** -Objekt lautet 9381D8F5-0288-11D0-9501-00AA00B911A5.</span><span class="sxs-lookup"><span data-stu-id="c1a85-121">The class ID for the **RDSServer.DataFactory** object is 9381D8F5-0288-11D0-9501-00AA00B911A5.</span></span>

