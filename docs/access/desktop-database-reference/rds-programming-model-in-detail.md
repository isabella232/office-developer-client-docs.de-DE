---
title: RDS-Programmierungsmodell im Detail
TOCTitle: RDS programming model in detail
ms:assetid: 133fc059-9b51-52e2-2e61-339716d8d965
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248906(v=office.15)
ms:contentKeyID: 48543364
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a3144f3f981d42868dfe2841ba9fd93dbb73c564
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597037"
---
# <a name="rds-programming-model-in-detail"></a>RDS-Programmierungsmodell im Detail

**Gilt für**: Access 2013, Office 2013

Die wichtigsten Elemente des RDS-Programmiermodells:

- RDS. Dataspace
- RDSServer.DataFactory
- RDS. DataControl
- Ereignis

## <a name="rdsdataspace"></a>RDS. Dataspace

Durch die Clientanwendung müssen der Server und das aufzurufende Serverprogramm angegeben werden. Dafür empfängt die Anwendung einen Verweis auf das Serverprogramm, und der Verweis kann von der Anwendung behandelt werden wie das Serverprogramm selbst.

Im RDS-Objektmodell wird diese Funktionalität durch das [RDS.DataSpace](dataspace-object-rds.md)-Objekt verkörpert.

Das Serverprogramm wird mit einem Programmbezeichner oder einer *ProgID* angegeben. Vom Server werden die *ProgID* und die Registrierung des Servercomputers zum Suchen von Informationen zu dem eigentlichen zu initiierenden Programm verwendet.

Die Unterscheidung erfolgt in RDS intern abhängig davon, ob sich das Serverprogramm auf einem Remoteserver im Internet oder Intranet, auf einem Server in einem lokalen Netzwerk oder überhaupt nicht auf einem Server, sondern in einer Dynamic Link Library (DLL) befindet. Durch diese Unterscheidung wird bestimmt, wie Informationen zwischen dem Client und dem Server ausgetauscht werden, und es werden deutlich andere Verweise an die Clientanwendung zurückgegeben. Aus Ihrer Sicht hat diese Unterscheidung jedoch keine besondere Bedeutung. Wichtig ist nur, dass Sie einen verwendbaren Programmverweis empfangen.

## <a name="rdsserverdatafactory"></a>RDSServer.DataFactory

Durch RDS wird ein Standardserverprogramm bereitgestellt, mit dem eine SQL-Abfrage für die Datenquelle ausgeführt und ein [Recordset](recordset-object-ado.md)-Objekt zurückgegeben oder ein **Recordset**-Objekt akzeptiert und die Datenquelle aktualisiert werden kann.

Im RDS-Objektmodell wird diese Funktionalität durch das [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekt verkörpert.

Darüber hinaus verfügt dieses Objekt über eine Methode zum Erstellen eines leeren **Recordset-Objekts,** das Sie programmgesteuert ausfüllen können ([CreateRecordset](createrecordset-method-rds.md)), und eine weitere Methode zum Konvertieren eines **Recordset-Objekts** in eine Textzeichenfolge zum Erstellen einer Webseite ([ConvertToString](converttostring-method-rds.md)).

Mit ADO können Sie einige standardmäßige Verbindungs- und Befehlsverhaltensweisen von **RDSServer.DataFactory** mit einem **DataFactory**-Handler und einer Anpassungsdatei, die Verbindungs-, Befehls- und Sicherheitsparameter enthält, außer Kraft setzen.

Das Serverprogramm wird manchmal als *Geschäftsobjekt* bezeichnet. Sie können ein eigenes benutzerdefiniertes Geschäftsobjekt schreiben, durch das komplizierte Datenzugriffe, Gültigkeitsüberprüfungen usw. ausgeführt werden können. Auch beim Schreiben eines benutzerdefinierten Geschäftsobjekts können Sie eine Instanz eines **RDSServer.DataFactory**-Objekts schreiben und einige seiner Methoden zum Ausführen Ihrer eigenen Aufgaben verwenden.

## <a name="rdsdatacontrol"></a>RDS. DataControl

Durch RDS wird eine Möglichkeit bereitgestellt, die Funktionalität von **RDS.DataSpace** und **RDSServer.DataFactory** zu kombinieren und außerdem die einfache Verwendung des durch eine Abfrage aus einer Datenquelle zurückgegebenen **Recordset** -Objekts durch visuelle Steuerelemente zu ermöglichen. Für den häufigsten Fall wird versucht, so weit wie möglich automatisch Zugriff auf Informationen auf einem Server zu erhalten und diese in einem visuellen Steuerelement anzuzeigen.

Im RDS-Objektmodell wird diese Funktionalität durch das [RDS.DataControl](datacontrol-object-rds.md)-Objekt verkörpert.

Das **RDS.DataControl** -Objekt hat zwei Aspekte. Ein Aspekt bezieht sich auf die Datenquelle. Wenn Sie die Befehls- und Verbindungsinformationen mithilfe der Eigenschaften **Connect** und **SQL** von **RDS.DataControl** festlegen, wird automatisch **RDS.DataSpace** zum Erstellen eines Verweises auf das standardmäßige **RDSServer.DataFactory** -Objekt verwendet. Dann wird von **RDSServer.DataFactory** der Wert der **Connect** -Eigenschaft zum Herstellen einer Verbindung mit der Datenquelle verwendet, mithilfe des Werts der **SQL** -Eigenschaft ein **Recordset** -Objekt aus der Datenquelle abgerufen und das **Recordset** -Objekt an **RDS.DataControl** zurückgegeben.

Der zweite Aspekt bezieht sich auf die Anzeige zurückgegebener **Recordset**-Informationen in einem visuellen Steuerelement. Sie können dem RDS ein visuelles Steuerelement **zuordnen. DataControl** (in einem als Bindung bezeichneten Prozess) und erhalten Zugriff auf die Informationen im zugeordneten **Recordset-Objekt,** wobei Abfrageergebnisse auf einer Webseite in Microsoft Internet Explorer angezeigt werden. Durch jedes **RDS.DataControl**-Objekt wird ein **Recordset**-Objekt, das die Ergebnisse einer einzelnen Abfrage darstellt, an mindestens ein visuelles Steuerelement gebunden (z. B. ein Textfeld, Kombinationsfeld, Rastersteuerelement usw.). Auf jeder Seite kann mehr als ein **RDS.DataControl**-Objekt vorhanden sein. Jedes **RDS.DataControl**-Objekt kann mit einer anderen Datenquelle verbunden sein und die Ergebnisse einer separaten Abfrage enthalten.

Das **RDS.DataControl** -Objekt verfügt außerdem über eigene Methoden für das Navigieren, Sortieren und Filtern der Zeilen des zugeordneten **Recordset** -Objekts. Diese Methoden sind vergleichbar, jedoch nicht identisch mit den Methoden des **Recordset** -ADO-Objekts.

## <a name="events"></a>Ereignisse

Von RDS werden zwei eigene Ereignisse unterstützt, die vom ADO-Ereignismodell unabhängig sind. Das [onReadyStateChange-Ereignis](onreadystatechange-event-rds.md) wird immer dann aufgerufen, wenn der **RDS ausgeführt wird. Die DataControl** [ReadyState-Eigenschaft](readystate-property-rds.md) ändert sich und benachrichtigt Sie, wenn ein asynchroner Vorgang erfolgreich abgeschlossen, beendet oder ein Fehler aufgetreten ist. Das [onError](onerror-event-rds.md)-Ereignis wird bei jedem Auftreten eines Fehlers aufgerufen, selbst wenn der Fehler während einer asynchronen Operation auftritt.

> [!NOTE]
> [!HINWEIS] Durch Microsoft Internet Explorer werden zwei zusätzliche Ereignisse für RDS bereitgestellt - **onDataSetChanged** (das **Recordset** -Objekt ist funktionsfähig, es werden aber dennoch Zeilen abgerufen) und **onDataSetComplete** (das Abrufen von Zeilen durch das **Recordset** ist beendet).


