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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710349"
---
# <a name="server-property-rds"></a>Server-Eigenschaft (RDS)

**Betrifft**: Access 2013, Office 2013

Gibt den Namen der Internetinformationsdienste (Internet Information Services, IIS) und des Kommunikationsprotokolls an.

Sie können die **Server** -Eigenschaft zur Entwurfszeit in den OBJECT-Tags des [RDS.DataControl](datacontrol-object-rds.md)-Objekts oder zur Laufzeit in Skriptcode festlegen.

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
|*Awebsrvr* oder *computername* |Ein **String** -Wert, der einen Internet- oder Intranetpfad enthält oder einen Computernamen, falls sich der Server auf einem Remotecomputer befindet. Ist der Server auf einem lokalen Computer, enthält der Wert eine leere Zeichenfolge.|
|*port* |Optional. Ein zur Verbindung mit einem IIS-Server verwendeter Port. Die Portnummer wird in IIS oder in Internet Explorer festgelegt (klicken Sie im Menü **Extras** auf **Internetoptionen**, und wählen Sie dann die Registerkarte **Verbindungen** aus).|
|*DataControl* |Eine Objektvariable, die ein **RDS.DataControl**-Objekt darstellt.|

## <a name="remarks"></a>Hinweise

Der Server ist der Speicherort, in dem die **RDS. DataControl** Anforderung (d. h., eine Abfrage oder Aktualisierung) verarbeitet wird. Standardmäßig werden alle Anforderungen durch das [RDSServer.DataFactory](datafactory-object-rdsserver.md) -Objekt [MSDFMAP verarbeitet. Handler](datafactory-customization.md) Komponente und [MSDFMAP. INI](understanding-the-customization-file.md) Datei auf dem angegebenen Server. 

Denken Sie daran, die beim Ändern von Servern, um die Einstellungen in das alte und neue **MSDFMAP abstimmen. INI** Dateien. Inkompatibilitäten möglicherweise Anfragen, die erfolgreich auf einem Server auf einem anderen ein Fehler auftritt. Wenn die Server-Eigenschaft festgelegt ist, "", diese Objekte auf dem lokalen Computer verwendet werden.

