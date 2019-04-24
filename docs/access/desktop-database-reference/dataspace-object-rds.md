---
title: DataSpace-Objekt (RDS)
TOCTitle: DataSpace object (RDS)
ms:assetid: 7db181d5-422b-49fe-b6af-a20f5da520ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249527(v=office.15)
ms:contentKeyID: 48545862
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f77617d4ddfb0160b8a418f55582a380067fde70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294463"
---
# <a name="dataspace-object-rds"></a>DataSpace-Objekt (RDS)

**Gilt für**: Access 2013, Office 2013

Es werden clientseitige Proxys für benutzerdefinierte Geschäftsobjekte der mittleren Ebene erstellt.

## <a name="remarks"></a>Bemerkungen

Remote Data Service benötigt Proxys für Geschäftsobjekte, damit clientseitige Komponenten mit Geschäftsobjekten kommunizieren können, die sich auf der mittleren Ebene befinden. Proxys vereinfachen das Verpacken, Entpacken und Übertragen (Marshalling) der [Recordset](recordset-object-ado.md)-Daten der Anwendung über Prozess- oder Computergrenzen.

Remote Data Service verwendet die **CreateObject**-Methode des [RDS.DataSpace](createobject-method-rds.md) -Objekts, um Geschäftsobjektproxys zu erstellen. Der Geschäftsobjektproxy wird dynamisch erstellt, wenn eine Instanz eines Gegenstücks seines Geschäftsobjekts der mittleren Ebene erstellt wird. Remote Data unterstützt die folgenden Protokolle: HTTP, HTTPS (HTTP Secure Sockets), DCOM und In-Process (die Clientkomponenten und das Geschäftsobjekt befinden sich auf demselben Computer).

> [!NOTE]
> [!HINWEIS] RDS verhält sich "zustandslos", wenn das **RDS.DataSpace** -Objekt das HTTP- oder HTTPS-Protokoll verwendet. Das heißt, alle internen Informationen über eine Clientanforderung werden gelöscht, nachdem der Server eine Antwort zurückgegeben hat.

Obwohl das Geschäftsobjekt während der Lebensdauer des Geschäftsobjektproxys vorhanden zu sein scheint, ist das Geschäftsobjekt tatsächlich nur vorhanden, bis eine Antwort auf die Anforderung gesendet wird. Wenn eine Anforderung ausgegeben wird (d. h. es wird eine Methode für das Geschäftsobjekt aufgerufen), öffnet der Proxy eine neue Verbindung zum Server, und der Server erstellt eine neue Instanz des Geschäftsobjekts. Nachdem das Geschäftsobjekt auf die Anforderung geantwortet hat, löscht der Server das Geschäftsobjekt und schließt die Verbindung.

Dieses Verhalten bedeutet, dass Sie keine Daten mithilfe einer Geschäftsobjekteigenschaft oder einer Variablen von einer Anforderung an eine andere übergeben können. Sie müssen zum Speichern von Zustandsdaten ein anderes Verfahren verwenden, wie etwa eine Datei oder ein Methodenargument.

Die Klassen-ID für das **RDS.DataSpace** -Objekt lautet BD96C556-65A3-11D0-983A-00C04FC29E36.

