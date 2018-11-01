---
title: RDS-Programmiermodell mit Objekten
TOCTitle: RDS Programming Model with Objects
ms:assetid: 207150ec-8eb5-bec5-3059-db37a0e28c19
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248987(v=office.15)
ms:contentKeyID: 48543663
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f6d28373e5d241ae9e87357187894924f27ba78c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873803"
---
# <a name="rds-programming-model-with-objects"></a>RDS-Programmiermodell mit Objekten


**Betrifft**: Access 2013, Office 2013

Das Ziel von RDS besteht darin, über einen Vermittler wie IIS (Internet Information Services, Internetinformationsdienste) Zugriff auf Datenquellen zu erhalten und diese zu aktualisieren. Durch das Programmiermodell wird die Reihenfolge der zum Erreichen dieses Ziels notwendigen Aktivitäten angegeben. Durch das Objektmodell werden die Objekte angegeben, deren Methoden und Eigenschaften sich auf das Programmiermodell auswirken.

Durch RDS werden die Mittel bereitgestellt, die zum Ausführen der folgenden Aktionssequenz benötigt werden:

  - Geben Sie das auf dem Server aufzurufende Programm an, und ermitteln Sie eine Möglichkeit (Proxy), vom Client darauf zu verweisen ([RDS.DataSpace](dataspace-object-rds.md)).

  - Rufen Sie das Serverprogramm auf. Übergeben Sie dem Serverprogramm Parameter, durch die die Datenquelle und der auszugebende Befehl identifiziert werden (Proxy oder [RDS.DataControl](datacontrol-object-rds.md)).

  - Das Serverprogramm erhält ein [Recordset](recordset-object-ado.md)-Objekt aus der Datenquelle, normalerweise mithilfe von ADO. Optional wird das **Recordset**-Objekt auf dem Server verarbeitet ([RDSServer.DataFactory](datafactory-object-rdsserver.md)).

  - Vom Serverprogramm wird das endgültige **Recordset** -Objekt an die Clientanwendung (Proxy) zurückgegeben.

  - Auf dem Client wird das **Recordset**-Objekt in eine Form umgewandelt, die von visuellen Steuerelementen (visuelles Steuerelement und **RDS.DataControl**) problemlos verwendet werden kann.

  - Änderungen am **Recordset**-Objekt werden zurück an den Server gesendet und zum Aktualisieren der Datenquelle (**RDS.DataControl** oder **RDSServer.DataFactory**) verwendet.

