---
title: DataSpace-Objekt (RDS)
TOCTitle: DataSpace Object (RDS)
ms:assetid: 7db181d5-422b-49fe-b6af-a20f5da520ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249527(v=office.15)
ms:contentKeyID: 48545862
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1715a1d1207955d47897fee8ba191117bcfaa244
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882917"
---
# <a name="dataspace-object-rds"></a>DataSpace-Objekt (RDS)

**Betrifft**: Access 2013, Office 2013

Erstellt clientseitige Proxys für angepasste Geschäftsobjekte, die sich auf der mittleren Ebene befinden.

## <a name="remarks"></a>Hinweise

Remote Data Service benötigt Proxys für Geschäftsobjekte, damit clientseitige Komponenten mit Geschäftsobjekten kommunizieren können, die sich auf der mittleren Ebene befinden. Proxys vereinfachen das Verpacken, Entpacken und Übertragen (Marshalling) der [Recordset](recordset-object-ado.md)-Daten der Anwendung über Prozess- oder Computergrenzen.

Remote Data Service verwendet die **CreateObject**-Methode des [RDS.DataSpace](createobject-method-rds.md) -Objekts, um Geschäftsobjektproxys zu erstellen. Der Geschäftsobjektproxy wird dynamisch erstellt, wenn eine Instanz eines Gegenstücks seines Geschäftsobjekts der mittleren Ebene erstellt wird. Remote Data unterstützt die folgenden Protokolle: HTTP, HTTPS (HTTP Secure Sockets), DCOM und In-Process (die Clientkomponenten und das Geschäftsobjekt befinden sich auf demselben Computer).

> [!NOTE]
> [!HINWEIS] RDS verhält sich "zustandslos", wenn das **RDS.DataSpace** -Objekt das HTTP- oder HTTPS-Protokoll verwendet. Das heißt, alle internen Informationen über eine Clientanforderung werden gelöscht, nachdem der Server eine Antwort zurückgegeben hat.

Obwohl das Geschäftsobjekt während der Lebensdauer des Geschäftsobjektproxys vorhanden zu sein scheint, ist das Geschäftsobjekt tatsächlich nur vorhanden, bis eine Antwort auf die Anforderung gesendet wird. Wenn eine Anforderung ausgegeben wird (d. h. es wird eine Methode für das Geschäftsobjekt aufgerufen), öffnet der Proxy eine neue Verbindung zum Server, und der Server erstellt eine neue Instanz des Geschäftsobjekts. Nachdem das Geschäftsobjekt auf die Anforderung geantwortet hat, löscht der Server das Geschäftsobjekt und schließt die Verbindung.

Dieses Verhalten bedeutet, dass Sie keine Daten mithilfe einer Geschäftsobjekteigenschaft oder einer Variablen von einer Anforderung an eine andere übergeben können. Sie müssen zum Speichern von Zustandsdaten ein anderes Verfahren verwenden, wie etwa eine Datei oder ein Methodenargument.

Die Klassen-ID für das **RDS.DataSpace** -Objekt lautet BD96C556-65A3-11D0-983A-00C04FC29E36.

