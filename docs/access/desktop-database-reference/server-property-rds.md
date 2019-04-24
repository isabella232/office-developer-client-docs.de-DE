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
# <a name="server-property-rds"></a>Server-Eigenschaft (RDS)

**Gilt für**: Access 2013, Office 2013

Gibt den Namen der Internetinformationsdienste (Internet Information Services, IIS) und des Kommunikationsprotokolls an.

Sie können die **Server**-Eigenschaft zur Entwurfszeit in den OBJECT-Tags des [RDS.DataControl](datacontrol-object-rds.md)-Objekts oder zur Laufzeit in Skriptcode festlegen.

## <a name="syntax"></a>Syntax

|Protokoll|Entwurfszeitsyntax|
|:-------|:-----------------|
|HTTP|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|HTTPS|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|DCOM|`<PARAM NAME="Server" VALUE="computername">`|
|In-Process|`<PARAM NAME="Server" VALUE="">`|


|Protokoll|Laufzeitsyntax|
|:-------|:--------------|
|HTTP|`DataControl.Server="https://awebsrvr:port"`|
|HTTPS|`DataControl.Server="https://awebsrvr:port"`|
|DCOM|`DataControl.Server="computername"`|
|In-Process|`DataControl.Server=""`|


## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*awebsrvr* oder *computername* |Ein **String**-Wert, der einen Internet- oder Intranetpfad enthält oder einen Computernamen, falls sich der Server auf einem Remotecomputer befindet. Ist der Server auf einem lokalen Computer, enthält der Wert eine leere Zeichenfolge.|
|*port* |Optional. Ein zur Verbindung mit einem IIS-Server verwendeter Port. Die Portnummer wird in IIS oder in Internet Explorer festgelegt (klicken Sie im Menü **Extras** auf **Internetoptionen**, und wählen Sie dann die Registerkarte **Verbindungen** aus).|
|*DataControl* |Eine Objektvariable, die ein **RDS.DataControl**-Objekt darstellt.|

## <a name="remarks"></a>Bemerkungen

The server is the location where the **RDS.DataControl** request (that is, a query or update) is processed. By default, all requests are processed by the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, [MSDFMAP.Handler](datafactory-customization.md) component, and [MSDFMAP.INI](understanding-the-customization-file.md) file on the specified server. 

Remember that when changing servers to reconcile settings in the old and new **MSDFMAP.INI** files. Incompatibilities may cause requests that succeed on one server to fail on another. If the Server property is set to "", these objects will be used on the local machine.

