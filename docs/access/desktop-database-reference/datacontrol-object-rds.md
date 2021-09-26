---
title: DataControl-Objekt (RDS)
TOCTitle: DataControl object (RDS)
ms:assetid: ac430669-7628-696c-c036-b5d35405d788
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249801(v=office.15)
ms:contentKeyID: 48547001
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ee1f446d1665682ebe7a15c7ea46d05fcc8394ac
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589743"
---
# <a name="datacontrol-object-rds"></a>DataControl-Objekt (RDS)

**Gilt für**: Access 2013, Office 2013

Bindet ein [Datenabfragerecordset](recordset-object-ado.md) an ein oder mehrere Steuerelemente (z. B. ein Textfeld, ein Rastersteuerelement oder ein Kombinationsfeld), um die **Recordset-Daten** auf einer Webseite anzuzeigen.

## <a name="syntax"></a>Syntax

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
    </OBJECT>
```

## <a name="remarks"></a>HinwBemerkungeneise

Die Klassen-ID für das **RDS.DataControl** -Objekt lautet BD96C556-65A3-11D0-983A-00C04FC29E33.

> [!NOTE]
> [!HINWEIS] Wenn Sie einen Fehler darüber erhalten, dass ein [RDS.DataSpace](dataspace-object-rds.md)- oder **RDS.DataControl** -Objekt nicht geladen werden kann, sollten Sie sicherstellen, dass Sie die richtige Klassen-ID verwenden. Die Klassen-IDs für diese Objekte wurden seit den Versionen 1.0 und 1.1 geändert.

Für ein Basisszenario müssen Sie nur die Eigenschaften **SQL**, **Connect** und **Server** des **RDS.DataControl** -Objekts festlegen. Damit wird automatisch das Standard-Geschäftsobjekt namens [RDSServer.DataFactory](datafactory-object-rdsserver.md) aufgerufen.

Alle Eigenschaften im **RDS.DataControl** -Objekt sind optional, da benutzerdefinierte Geschäftsobjekte ihre Funktionalität ersetzen können.

> [!NOTE]
> [!HINWEIS] Wenn Sie mehrere Ergebnisse abfragen, wird nur das erste [Recordset](recordset-object-ado.md)-Objekt zurückgegeben. Wenn mehrere Ergebnismengen erforderlich sind, weisen Sie jeder ein eigenes **DataControl** -Objekt zu. 
> 
> Ein Beispiel für eine Abfrage für mehrere Ergebnisse könnte folgende sein: `"Select * from Authors, Select * from Topics"` .

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

  - Fügen Sie zwei **RDS hinzu. DataControl-Objekte** für Ihre Webseite.

  - Write two queries, one for each **SQL** property of the two **RDS.DataControl** objects. One **RDS.DataControl** object will contain an SQL query requesting customer information; the second will contain a query requesting a list of merchandise the customer has purchased.

  - Geben Sie im OBJECT-Tag der beiden gebundenen Steuerelemente den DATAFLD-Wert an, um die Werte für die Daten festzulegen, die in den einzelnen visuellen Steuerelementen angezeigt werden sollen.

Es gibt keine Zählungseinschränkung für die Anzahl von **RDS. DataControl-Objekte,** die Sie über OBJECT-Tags auf einer einzelnen Webseite einbetten können.

Beim Definieren des **RDS. Verwenden** Sie für das DataControl-Objekt auf einer Webseite Werte ungleich Null **für Höhe** und **Breite** wie 1 (um zusätzlichen Speicherplatz zu vermeiden).

Clientkomponenten von Remote Data Service sind bereits in Internet Explorer 4.0 enthalten. Aus diesem Grund ist es nicht erforderlich, einen CODEBASE-Parameter in das **RDS.DataControl** -Objekttag einzubeziehen.

Mit Internet Explorer 4.0 oder höher können Sie eine Bindung an Daten nur mithilfe von HTML-Steuerelementen und ActiveX-Steuerelementen einrichten, wenn sie als Apartmentmodellsteuerelemente gekennzeichnet sind.

**Microsoft Visual Basic-Benutzer** The **RDS. DataControl** wird nur in webbasierten Anwendungen verwendet. Eine Visual Basic-Clientanwendung benötigt das Objekt nicht.

