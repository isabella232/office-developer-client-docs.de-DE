---
title: Server-Eigenschaft (RDS)
TOCTitle: Server property (RDS)
ms:assetid: 17519dbe-a43a-1d0d-22c1-dc0def2f63ab
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248926(v=office.15)
ms:contentKeyID: 48543448
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 062a4a319073ccf8f2810205973c11a845e2cc6f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925233"
---
# <a name="server-property-rds"></a><span data-ttu-id="10ebf-102">Server-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="10ebf-102">Server property (RDS)</span></span>


<span data-ttu-id="10ebf-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="10ebf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="10ebf-104">Gibt den Namen der Internetinformationsdienste (Internet Information Services, IIS) und des Kommunikationsprotokolls an.</span><span class="sxs-lookup"><span data-stu-id="10ebf-104">Indicates the Internet Information Services (IIS) name and communication protocol.</span></span>

<span data-ttu-id="10ebf-105">Sie können die **Server** -Eigenschaft zur Entwurfszeit in den OBJECT-Tags des [RDS.DataControl](datacontrol-object-rds.md)-Objekts oder zur Laufzeit in Skriptcode festlegen.</span><span class="sxs-lookup"><span data-stu-id="10ebf-105">You can set the **Server** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="10ebf-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="10ebf-106">Syntax</span></span>

|<span data-ttu-id="10ebf-107">Protokoll</span><span class="sxs-lookup"><span data-stu-id="10ebf-107">Protocol</span></span>|<span data-ttu-id="10ebf-108">Entwurfszeitsyntax</span><span class="sxs-lookup"><span data-stu-id="10ebf-108">Design-time syntax</span></span>|
|:-------|:-----------------|
|<span data-ttu-id="10ebf-109">HTTP</span><span class="sxs-lookup"><span data-stu-id="10ebf-109">HTTP</span></span>|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|<span data-ttu-id="10ebf-110">HTTPS</span><span class="sxs-lookup"><span data-stu-id="10ebf-110">HTTPS</span></span>|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|<span data-ttu-id="10ebf-111">DCOM</span><span class="sxs-lookup"><span data-stu-id="10ebf-111">DCOM</span></span>|`<PARAM NAME="Server" VALUE="computername">`|
|<span data-ttu-id="10ebf-112">In-Process</span><span class="sxs-lookup"><span data-stu-id="10ebf-112">In-process</span></span>|`<PARAM NAME="Server" VALUE="">`|


|<span data-ttu-id="10ebf-113">Protokoll</span><span class="sxs-lookup"><span data-stu-id="10ebf-113">Protocol</span></span>|<span data-ttu-id="10ebf-114">Laufzeitsyntax</span><span class="sxs-lookup"><span data-stu-id="10ebf-114">Run-time syntax</span></span>|
|:-------|:--------------|
|<span data-ttu-id="10ebf-115">HTTP</span><span class="sxs-lookup"><span data-stu-id="10ebf-115">HTTP</span></span>|`DataControl.Server="https://awebsrvr:port"`|
|<span data-ttu-id="10ebf-116">HTTPS</span><span class="sxs-lookup"><span data-stu-id="10ebf-116">HTTPS</span></span>|`DataControl.Server="https://awebsrvr:port"`|
|<span data-ttu-id="10ebf-117">DCOM</span><span class="sxs-lookup"><span data-stu-id="10ebf-117">DCOM</span></span>|`DataControl.Server="computername"`|
|<span data-ttu-id="10ebf-118">In-Process</span><span class="sxs-lookup"><span data-stu-id="10ebf-118">In-process</span></span>|`DataControl.Server=""`|


## <a name="parameters"></a><span data-ttu-id="10ebf-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="10ebf-119">Parameters</span></span>

<span data-ttu-id="10ebf-120">*Awebsrvr* oder *computername*</span><span class="sxs-lookup"><span data-stu-id="10ebf-120">*awebsrvr* or *computername*</span></span>

- <span data-ttu-id="10ebf-121">Ein **String** -Wert, der einen Internet- oder Intranetpfad enthält oder einen Computernamen, falls sich der Server auf einem Remotecomputer befindet. Ist der Server auf einem lokalen Computer, enthält der Wert eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="10ebf-121">A **String** value that contains an Internet or intranet path, or computer name, if the server is on a remote computer; or, an empty string if the server is on the local computer.</span></span>

<span data-ttu-id="10ebf-122">*port*</span><span class="sxs-lookup"><span data-stu-id="10ebf-122">*port*</span></span>

- <span data-ttu-id="10ebf-p101">Optional. Ein zur Verbindung mit einem IIS-Server verwendeter Port. Die Portnummer wird in IIS oder in Internet Explorer festgelegt (klicken Sie im Menü **Extras** auf **Internetoptionen**, und wählen Sie dann die Registerkarte **Verbindungen** aus).</span><span class="sxs-lookup"><span data-stu-id="10ebf-p101">Optional. A port that is used to connect to an IIS server. The port number is set in Internet Explorer (on the **Tools** menu, click **Internet Options**, and then select the **Connection** tab) or in IIS.</span></span>

<span data-ttu-id="10ebf-126">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="10ebf-126">*DataControl*</span></span>

- <span data-ttu-id="10ebf-127">Eine Objektvariable, die ein **RDS.DataControl**-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="10ebf-127">An object variable that represents an **RDS.DataControl** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="10ebf-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="10ebf-128">Remarks</span></span>

<span data-ttu-id="10ebf-129">Der Server ist der Speicherort, in dem die **RDS. DataControl** Anforderung (d. h., eine Abfrage oder Aktualisierung) verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="10ebf-129">The server is the location where the **RDS.DataControl** request (that is, a query or update) is processed.</span></span> <span data-ttu-id="10ebf-130">Standardmäßig werden alle Anforderungen durch das [RDSServer.DataFactory](datafactory-object-rdsserver.md) -Objekt [MSDFMAP verarbeitet. Handler](datafactory-customization.md) Komponente und [MSDFMAP. INI](understanding-the-customization-file.md) Datei auf dem angegebenen Server.</span><span class="sxs-lookup"><span data-stu-id="10ebf-130">By default, all requests are processed by the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, [MSDFMAP.Handler](datafactory-customization.md) component, and [MSDFMAP.INI](understanding-the-customization-file.md) file on the specified server.</span></span> 

<span data-ttu-id="10ebf-131">Denken Sie daran, die beim Ändern von Servern, um die Einstellungen in das alte und neue **MSDFMAP abstimmen. INI** Dateien.</span><span class="sxs-lookup"><span data-stu-id="10ebf-131">Remember that when changing servers to reconcile settings in the old and new **MSDFMAP.INI** files.</span></span> <span data-ttu-id="10ebf-132">Inkompatibilitäten möglicherweise Anfragen, die erfolgreich auf einem Server auf einem anderen ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="10ebf-132">Incompatibilities may cause requests that succeed on one server to fail on another.</span></span> <span data-ttu-id="10ebf-133">Wenn die Server-Eigenschaft festgelegt ist, "", diese Objekte auf dem lokalen Computer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10ebf-133">If the Server property is set to "", these objects will be used on the local machine.</span></span>

