---
title: Server-Eigenschaft (RDS)
TOCTitle: Server property (RDS)
ms:assetid: 17519dbe-a43a-1d0d-22c1-dc0def2f63ab
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248926(v=office.15)
ms:contentKeyID: 48543448
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f35910591d86e0e5a2b92d680be3c5f64504088
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308687"
---
# <a name="server-property-rds"></a><span data-ttu-id="863e8-102">Server-Eigenschaft (RDS)</span><span class="sxs-lookup"><span data-stu-id="863e8-102">Server property (RDS)</span></span>

<span data-ttu-id="863e8-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="863e8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="863e8-104">Gibt den Namen der Internetinformationsdienste (Internet Information Services, IIS) und des Kommunikationsprotokolls an.</span><span class="sxs-lookup"><span data-stu-id="863e8-104">Indicates the Internet Information Services (IIS) name and communication protocol.</span></span>

<span data-ttu-id="863e8-105">Sie können die **Server**-Eigenschaft zur Entwurfszeit in den OBJECT-Tags des [RDS.DataControl](datacontrol-object-rds.md)-Objekts oder zur Laufzeit in Skriptcode festlegen.</span><span class="sxs-lookup"><span data-stu-id="863e8-105">You can set the **Server** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="863e8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="863e8-106">Syntax</span></span>

|<span data-ttu-id="863e8-107">Protokoll</span><span class="sxs-lookup"><span data-stu-id="863e8-107">Protocol</span></span>|<span data-ttu-id="863e8-108">Entwurfszeitsyntax</span><span class="sxs-lookup"><span data-stu-id="863e8-108">Design-time syntax</span></span>|
|:-------|:-----------------|
|<span data-ttu-id="863e8-109">HTTP</span><span class="sxs-lookup"><span data-stu-id="863e8-109">HTTP</span></span>|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|<span data-ttu-id="863e8-110">HTTPS</span><span class="sxs-lookup"><span data-stu-id="863e8-110">HTTPS</span></span>|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|<span data-ttu-id="863e8-111">DCOM</span><span class="sxs-lookup"><span data-stu-id="863e8-111">DCOM</span></span>|`<PARAM NAME="Server" VALUE="computername">`|
|<span data-ttu-id="863e8-112">In-Process</span><span class="sxs-lookup"><span data-stu-id="863e8-112">In-process</span></span>|`<PARAM NAME="Server" VALUE="">`|


|<span data-ttu-id="863e8-113">Protokoll</span><span class="sxs-lookup"><span data-stu-id="863e8-113">Protocol</span></span>|<span data-ttu-id="863e8-114">Laufzeitsyntax</span><span class="sxs-lookup"><span data-stu-id="863e8-114">Run-time syntax</span></span>|
|:-------|:--------------|
|<span data-ttu-id="863e8-115">HTTP</span><span class="sxs-lookup"><span data-stu-id="863e8-115">HTTP</span></span>|`DataControl.Server="https://awebsrvr:port"`|
|<span data-ttu-id="863e8-116">HTTPS</span><span class="sxs-lookup"><span data-stu-id="863e8-116">HTTPS</span></span>|`DataControl.Server="https://awebsrvr:port"`|
|<span data-ttu-id="863e8-117">DCOM</span><span class="sxs-lookup"><span data-stu-id="863e8-117">DCOM</span></span>|`DataControl.Server="computername"`|
|<span data-ttu-id="863e8-118">In-Process</span><span class="sxs-lookup"><span data-stu-id="863e8-118">In-process</span></span>|`DataControl.Server=""`|


## <a name="parameters"></a><span data-ttu-id="863e8-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="863e8-119">Parameters</span></span>

|<span data-ttu-id="863e8-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="863e8-120">Parameter</span></span>|<span data-ttu-id="863e8-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="863e8-121">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="863e8-122">*awebsrvr* oder *computername*</span><span class="sxs-lookup"><span data-stu-id="863e8-122">*awebsrvr* or *computername*</span></span> |<span data-ttu-id="863e8-123">Ein **String**-Wert, der einen Internet- oder Intranetpfad enthält oder einen Computernamen, falls sich der Server auf einem Remotecomputer befindet. Ist der Server auf einem lokalen Computer, enthält der Wert eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="863e8-123">A **String** value that contains an Internet or intranet path, or computer name, if the server is on a remote computer; or, an empty string if the server is on the local computer.</span></span>|
|<span data-ttu-id="863e8-124">*port*</span><span class="sxs-lookup"><span data-stu-id="863e8-124">*port*</span></span> |<span data-ttu-id="863e8-p101">Optional. Ein zur Verbindung mit einem IIS-Server verwendeter Port. Die Portnummer wird in IIS oder in Internet Explorer festgelegt (klicken Sie im Menü **Extras** auf **Internetoptionen**, und wählen Sie dann die Registerkarte **Verbindungen** aus).</span><span class="sxs-lookup"><span data-stu-id="863e8-p101">Optional. A port that is used to connect to an IIS server. The port number is set in Internet Explorer (on the **Tools** menu, click **Internet Options**, and then select the **Connection** tab) or in IIS.</span></span>|
|<span data-ttu-id="863e8-128">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="863e8-128">*DataControl*</span></span> |<span data-ttu-id="863e8-129">Eine Objektvariable, die ein **RDS.DataControl**-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="863e8-129">An object variable that represents an **RDS.DataControl** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="863e8-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="863e8-130">Remarks</span></span>

<span data-ttu-id="863e8-131">The server is the location where the **RDS.DataControl** request (that is, a query or update) is processed.</span><span class="sxs-lookup"><span data-stu-id="863e8-131">The server is the location where the **RDS.DataControl** request (that is, a query or update) is processed.</span></span> <span data-ttu-id="863e8-132">By default, all requests are processed by the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, [MSDFMAP.Handler](datafactory-customization.md) component, and [MSDFMAP.INI](understanding-the-customization-file.md) file on the specified server.</span><span class="sxs-lookup"><span data-stu-id="863e8-132">By default, all requests are processed by the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, [MSDFMAP.Handler](datafactory-customization.md) component, and [MSDFMAP.INI](understanding-the-customization-file.md) file on the specified server.</span></span> 

<span data-ttu-id="863e8-133">Remember that when changing servers to reconcile settings in the old and new **MSDFMAP.INI** files.</span><span class="sxs-lookup"><span data-stu-id="863e8-133">Remember that when changing servers to reconcile settings in the old and new **MSDFMAP.INI** files.</span></span> <span data-ttu-id="863e8-134">Incompatibilities may cause requests that succeed on one server to fail on another.</span><span class="sxs-lookup"><span data-stu-id="863e8-134">Incompatibilities may cause requests that succeed on one server to fail on another.</span></span> <span data-ttu-id="863e8-135">If the Server property is set to "", these objects will be used on the local machine.</span><span class="sxs-lookup"><span data-stu-id="863e8-135">If the Server property is set to "", these objects will be used on the local machine.</span></span>

