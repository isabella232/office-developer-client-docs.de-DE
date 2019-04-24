---
title: DataControl-Objekt (RDS)
TOCTitle: DataControl object (RDS)
ms:assetid: ac430669-7628-696c-c036-b5d35405d788
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249801(v=office.15)
ms:contentKeyID: 48547001
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2ffe674f3aa02e5cc8b1f89375ca66b4efa623f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294519"
---
# <a name="datacontrol-object-rds"></a>DataControl-Objekt (RDS)

**Gilt für**: Access 2013, Office 2013

Bindet ein Datenabfrage- [Recordset](recordset-object-ado.md) -Objekt an ein oder mehrere Steuerelemente (beispielsweise ein Textfeld, ein Rastersteuerelement oder ein Kombinationsfeld), um die **Recordset** -Daten auf einer Webseite anzuzeigen.

## <a name="syntax"></a>Syntax

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
    </OBJECT>
```

## <a name="remarks"></a>Bemerkungen

Die Klassen-ID für das **RDS.DataControl** -Objekt lautet BD96C556-65A3-11D0-983A-00C04FC29E33.

> [!NOTE]
> [!HINWEIS] Wenn Sie einen Fehler darüber erhalten, dass ein [RDS.DataSpace](dataspace-object-rds.md)- oder **RDS.DataControl** -Objekt nicht geladen werden kann, sollten Sie sicherstellen, dass Sie die richtige Klassen-ID verwenden. Die Klassen-IDs für diese Objekte wurden seit den Versionen 1.0 und 1.1 geändert.

Für ein Basisszenario müssen Sie nur die Eigenschaften **SQL**, **Connect** und **Server** des **RDS.DataControl** -Objekts festlegen. Damit wird automatisch das Standard-Geschäftsobjekt namens [RDSServer.DataFactory](datafactory-object-rdsserver.md) aufgerufen.

Alle Eigenschaften im **RDS.DataControl** -Objekt sind optional, da benutzerdefinierte Geschäftsobjekte ihre Funktionalität ersetzen können.

> [!NOTE]
> [!HINWEIS] Wenn Sie mehrere Ergebnisse abfragen, wird nur das erste [Recordset](recordset-object-ado.md)-Objekt zurückgegeben. Wenn mehrere Ergebnismengen erforderlich sind, weisen Sie jeder ein eigenes **DataControl** -Objekt zu. 
> 
> Ein Beispiel für eine Abfrage für mehrere Ergebnisse kann Folgendes sein: `"Select * from Authors, Select * from Topics"`.

Wenn Sie das **RDS-DataControl** -Objekt verwenden und der Verbindungsreihenfolge "DFMode=20;" hinzufügen, kann sich die Leistung des Servers beim Aktualisieren von Daten verbessern. Bei dieser Einstellung verwendet das **RDSServer.DataFactory** -Objekt auf dem Server einen weniger ressourcenintensiven Modus. In dieser Konfiguration sind die folgenden Features jedoch nicht verfügbar:

  - Verwenden parametrisierter Abfragen.

  - Abrufen von Parameter- oder Spalteninformationen vor dem Aufrufen der **Execute**-Methode.

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

  - Fügen Sie zwei **RDS hinzu. DataControl** -Objekte für Ihre Webseite.

  - Write two queries, one for each **SQL** property of the two **RDS.DataControl** objects. One **RDS.DataControl** object will contain an SQL query requesting customer information; the second will contain a query requesting a list of merchandise the customer has purchased.

  - Geben Sie im OBJECT-Tag der beiden gebundenen Steuerelemente den DATAFLD-Wert an, um die Werte für die Daten festzulegen, die in den einzelnen visuellen Steuerelementen angezeigt werden sollen.

Es gibt keine Anzahl von Einschränkungen für die Anzahl der **RDS. DataControl** -Objekte, die Sie über Objekttags auf einer einzelnen Webseite einbetten können.

Beim Definieren des **RDS. DataControl** -Objekt auf einer Webseite verwenden Sie die Werte für **Höhe** und **Breite** ungleich NULL, wie etwa 1 (um die Aufnahme von zusätzlichem Leerraum zu vermeiden).

Clientkomponenten von Remote Data Service sind bereits in Internet Explorer 4.0 enthalten. Aus diesem Grund ist es nicht erforderlich, einen CODEBASE-Parameter in das **RDS.DataControl** -Objekttag einzubeziehen.

Mit Internet Explorer 4,0 oder höher können Sie Daten nur mithilfe von HTML-Steuerelementen und ActiveX-Steuerelementen binden, wenn Sie als Apartmentmodell-Steuerelemente markiert sind.

**Microsoft Visual Basic-Benutzer** **RDS. DataControl** wird nur in webbasierten Anwendungen verwendet. Eine Visual Basic-Clientanwendung benötigt das Objekt nicht.

