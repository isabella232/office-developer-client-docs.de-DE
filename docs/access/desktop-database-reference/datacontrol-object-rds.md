---
title: DataControl-Objekt (RDS)
TOCTitle: DataControl object (RDS)
ms:assetid: ac430669-7628-696c-c036-b5d35405d788
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249801(v=office.15)
ms:contentKeyID: 48547001
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d4b622cd65cfaf71c45ac7ae8c77bdb596ebd3a
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937806"
---
# <a name="datacontrol-object-rds"></a>DataControl-Objekt (RDS)

**Betrifft**: Access 2013, Office 2013

Bindet eine Datenabfrage [Recordset-Objekt](recordset-object-ado.md) an einen oder mehrere Steuerelemente (beispielsweise ein Textfeld, Grid-Steuerelement oder Kombinationsfeld) **die Recordsetdaten** auf einer Webseite angezeigt.

## <a name="syntax"></a>Syntax

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
    </OBJECT>
```

## <a name="remarks"></a>Hinweise

Die Klassen-ID für das **RDS.DataControl** -Objekt lautet BD96C556-65A3-11D0-983A-00C04FC29E33.

> [!NOTE]
> [!HINWEIS] Wenn Sie einen Fehler darüber erhalten, dass ein [RDS.DataSpace](dataspace-object-rds.md)- oder **RDS.DataControl** -Objekt nicht geladen werden kann, sollten Sie sicherstellen, dass Sie die richtige Klassen-ID verwenden. Die Klassen-IDs für diese Objekte wurden seit den Versionen 1.0 und 1.1 geändert.

Für ein Basisszenario müssen Sie nur die Eigenschaften **SQL**, **Connect** und **Server** des **RDS.DataControl** -Objekts festlegen. Damit wird automatisch das Standard-Geschäftsobjekt namens [RDSServer.DataFactory](datafactory-object-rdsserver.md) aufgerufen.

Alle Eigenschaften im **RDS.DataControl** -Objekt sind optional, da benutzerdefinierte Geschäftsobjekte ihre Funktionalität ersetzen können.

> [!NOTE]
> [!HINWEIS] Wenn Sie mehrere Ergebnisse abfragen, wird nur das erste [Recordset](recordset-object-ado.md)-Objekt zurückgegeben. Wenn mehrere Ergebnismengen erforderlich sind, weisen Sie jeder ein eigenes **DataControl** -Objekt zu. 
> 
> Ein Beispiel für eine Abfrage für mehrere Ergebnisse folgende möglich: `"Select * from Authors, Select * from Topics"`.

Wenn Sie das **RDS-DataControl** -Objekt verwenden und der Verbindungsreihenfolge "DFMode=20;" hinzufügen, kann sich die Leistung des Servers beim Aktualisieren von Daten verbessern. Bei dieser Einstellung verwendet das **RDSServer.DataFactory** -Objekt auf dem Server einen weniger ressourcenintensiven Modus. In dieser Konfiguration sind die folgenden Features jedoch nicht verfügbar:

  - Verwenden parametrisierter Abfragen.

  - Abrufen von Parameter- oder Spalteninformationen vor dem Aufrufen der **Execute** -Methode.

  - Festlegen von **Transact Updates** auf **True**.

  - Abrufen von Zeilenstatus.

  - Aufrufen der [Resync](resync-method-ado.md)-Methode.

  - Aktualisieren (explizit oder automatisch) mithilfe der [Update Resync](update-resync-property-dynamic-ado.md)-Eigenschaft.

  - Festlegen der Eigenschaften von **Command** oder [Recordset](recordset-sourcerecordset-properties-rds.md).

  - Verwenden von **adCmdTableDirect**.

Das **RDS.DataControl** -Objekt wird standardmäßig im asynchronen Modus ausgeführt. Wenn Ihre Anwendung eine synchrone Ausführung erfordert, legen Sie den [ExecuteOptions](executeoptions-property-rds.md)-Parameter auf den Wert **adcExecSync** und den [FetchOptions](fetchoptions-property-rds.md)-Parameter auf den Wert **adcFetchUpFront** fest (siehe folgendes Beispiel).

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
        ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
       <PARAM NAME="ExecuteOptions" VALUE="1">
       <PARAM NAME="FetchOptions" VALUE="1">
    </OBJECT>
```

Verwenden Sie ein **RDS.DataControl** -Objekt, um die Ergebnisse einer einzelnen Abfrage mit einem oder mehreren visuellen Steuerelementen zu verknüpfen. Sie haben z. B. Code, in dem Sie Kundendaten abfragen, wie Namen, Wohnort, Geburtsort, Alter und Kundenprioritätsstatus. In diesem Fall können Sie den Namen, das Alter und die Region eines Kunden unter Verwendung eines einzigen **RDS.DataControl** -Objekts in drei unterschiedlichen Textfeldern, den Kundenprioritätsstatus in einem Kontrollkästchen und alle Daten in einem Rastersteuerelement anzeigen.

Verwenden Sie unterschiedliche **RDS.DataControl**-Objekte, um die Ergebnisse von Mehrfachabfragen mit verschiedenen visuellen Steuerelementen zu verknüpfen. Sie verwenden z. B. eine Abfrage, um Informationen über einen Kunden zu erhalten, und eine zweite Abfrage, um Informationen über Waren zu erhalten, die der Kunde gekauft hat. Sie möchten die Ergebnisse der ersten Abfrage in drei Textfeldern und einem Kontrollkästchen anzeigen und die Ergebnisse der zweiten Abfrage in einem Rastersteuerelement. Wenn Sie das Standardgeschäftsobjekt verwenden (**RDSServer.DataFactory**), müssen Sie folgendermaßen vorgehen:

  - Hinzufügen von zwei **RDS. DataControl** Objekte auf Ihrer Webseite.

  - Erstellen Sie zwei Abfragen, jeweils eine für die SQL-Eigenschaft der beiden RDS.DataControl-Objekte. Ein RDS.DataControl-Objekt enthält eine SQL-Abfrage, die Kundeninformationen abfragt. Das zweite RDS.DataControl-Objekt enthält eine Abfrage, mit der eine Liste der vom Kunden gekauften Waren abgefragt wird.

  - Geben Sie im OBJECT-Tag der beiden gebundenen Steuerelemente den DATAFLD-Wert an, um die Werte für die Daten festzulegen, die in den einzelnen visuellen Steuerelementen angezeigt werden sollen.

Es gibt keine Beschränkung für die Anzahl der **RDS. DataControl** -Objekten, die über OBJECT-Tags auf einer einzelnen Webseite eingebettet werden können.

Beim Definieren der **RDS. DataControl** -Objekts auf einer Webseite, verwenden Sie die Werte ungleich NULL **Höhe** und **Breite** wie etwa 1 (um die Aufnahme der leeren Platz zu vermeiden).

Clientkomponenten von Remote Data Service sind bereits in Internet Explorer 4.0 enthalten. Aus diesem Grund ist es nicht erforderlich, einen CODEBASE-Parameter in das **RDS.DataControl** -Objekttag einzubeziehen.

Mit Internet Explorer 4.0 oder höher, können Sie binden an Daten mithilfe von HTML- und ActiveX-Steuerelemente nur, wenn sie als Steuerelemente für des Apartmentthreading-Modells markiert sind.

**Microsoft Visual Basic-Benutzer** RDS **. DataControl** wird nur in webbasierten Anwendungen verwendet. Eine Visual Basic-Clientanwendung benötigt das Objekt nicht.

