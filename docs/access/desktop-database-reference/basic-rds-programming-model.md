---
title: Grundlegende RDS-Programmiermodell
TOCTitle: Basic RDS programming model
ms:assetid: a8dd22b0-ac9b-b5c3-4e31-d2990d36230a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249781(v=office.15)
ms:contentKeyID: 48546911
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ad7a6d31fa973ffd8d04b4478d73a88312d52073
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944811"
---
# <a name="basic-rds-programming-model"></a>Grundlegende RDS-Programmiermodell

**Betrifft**: Access 2013, Office 2013

RDS ist für Anwendungen in der folgenden Umgebung gedacht: Durch eine Clientanwendung werden ein auf einem Server ausgeführtes Programm und die erforderlichen Parameter zum Rückgeben der gewünschten Informationen angegeben. Das auf dem Server aufgerufene Programm erhält Zugriff auf die angegebene Datenquelle, ruft die Informationen ab, verarbeitet optional die Daten und gibt dann die resultierenden Informationen in einer einfach zu verwendenden Form an die Clientanwendung zurück. Durch RDS werden die Mittel bereitgestellt, die Sie zum Ausführen der folgenden Aktionssequenz benötigen:

- Geben Sie das auf dem Server aufzurufende Programm an, und ermitteln Sie eine Möglichkeit, vom Client darauf zu verweisen. (Dieser Verweis wird manchmal als *Proxy* bezeichnet. Er stellt das Remoteserverprogramm dar. Durch die Clientanwendung wird der Proxy wie ein lokales Programm "aufgerufen", obwohl tatsächlich das Remoteserverprogramm aufgerufen wird.)

- Rufen Sie das Serverprogramm auf. Übergeben Sie dem Serverprogramm Parameter, durch die die Datenquelle und der auszugebende Befehl identifiziert werden. (Vom Serverprogramm wird tatsächlich ADO für den Zugriff auf die Datenquelle verwendet. Durch ADO wird eine Verbindung mit einem der angegebenen Parameter hergestellt, und dann wird der im anderen Parameter angegebene Befehl ausgegeben.)

- Das Serverprogramm erhält ein [Recordset](recordset-object-ado.md)-Objekt aus der Datenquelle. Optional wird das **Recordset** -Objekt auf dem Server verarbeitet.

- Vom Serverprogramm wird das endgültige **Recordset** -Objekt an die Clientanwendung zurückgegeben.

- Auf dem Client wird das **Recordset** -Objekt in eine Form umgewandelt, die von visuellen Steuerelementen problemlos verwendet werden kann.

- Alle Änderungen am **Recordset** -Objekt werden zurück an das Serverprogramm gesendet, von dem sie zum Aktualisieren der Datenquelle verwendet werden.

Dieses Programmiermodell enthält bestimmte Komfortfeatures. Wenn Sie für den Zugriff auf die Datenquelle kein komplexes Serverprogramm benötigen und wenn Sie die erforderliche Verbindung und die erforderlichen Befehlsparameter bereitstellen, werden die angegebenen Daten von RDS automatisch mit einem einfachen Standardserverprogramm abgerufen.

Wenn Sie eine komplexere Verarbeitung benötigen, können Sie ein eigenes benutzerdefiniertes Serverprogramm angeben. Da ein benutzerdefiniertes Serverprogramm über die volle Leistungsfähigkeit von ADO verfügt, kann damit eine Verbindung mit mehreren anderen Datenquellen hergestellt werden, die Daten können auf komplexe Weise kombiniert werden, und dann kann ein einfaches verarbeitetes Ergebnis an die Clientanwendung zurückgegeben werden.

Wenn Ihre Anforderungen irgendwo dazwischen liegen, wird von ADO jetzt das Anpassen des Verhaltens des Standardserverprogramms unterstützt.

