---
title: Aktivieren einer DLL zur Ausführung auf DCOM
TOCTitle: Enabling a DLL to run on DCOM
ms:assetid: b405f767-91f0-c869-d34e-7a953de49106
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249859(v=office.15)
ms:contentKeyID: 48547211
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 07d22fb6af644e81af6ec7b82f71b4b2cbeaf69e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562657"
---
# <a name="enabling-a-dll-to-run-on-dcom"></a>Aktivieren einer DLL zur Ausführung auf DCOM


**Gilt für**: Access 2013, Office 2013

In den folgenden Schritten wird beschrieben, wie Sie einem Geschäftsobjekt Dynamic Link Libraries die Verwendung von DCOM und Microsoft-Internetinformationsdienste (HTTP) über Component Services ermöglichen.

1.  Erstellen Sie ein neues leeres Paket im MMC-Snap-In Komponentendienste. Mit dem MMC-Snap-In Komponentendienste erstellen Sie ein Paket und fügen dem Paket die DLL hinzu. Dadurch kann auf die DLL über DCOM zugegriffen werden, aber nicht mehr über IIS. (Wenn Sie die Registrierung für die DLL überprüfen, stellen Sie fest, dass der **Inproc** -Schlüssel jetzt leer ist. Durch Festlegen des Aktivierungsattributs wird dem **Inproc** -Schlüssel ein Wert hinzugefügt. Dies wird weiter unten in diesem Thema erläutert.)

2.  Installieren Sie ein Geschäftsobjekt in dem Paket. -oder- Importieren Sie das [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekt in das Paket.

3.  Legen Sie das Aktivierungsattribut für das Paket auf **Im Prozess des Erstellers** (Bibliotheksanwendung) fest. Damit auf die DLL über DCOM und IIS auf dem gleichen Computer zugegriffen werden kann, müssen Sie das Aktivierungsattribut der Komponente im MMC-Snap-In Komponentendienste festlegen. Nachdem Sie das Attribute auf **Im Prozess des Erstellers** festgelegt haben, werden Sie feststellen, dass in der Registrierung ein **Inproc** -Serverschlüssel hinzugefügt wurde, der auf eine Ersatz-DLL der Komponentendienste verweist.

