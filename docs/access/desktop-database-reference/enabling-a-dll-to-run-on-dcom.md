---
title: Aktivieren einer DLL für die Ausführung mit DCOM
TOCTitle: Enabling a DLL to Run on DCOM
ms:assetid: b405f767-91f0-c869-d34e-7a953de49106
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249859(v=office.15)
ms:contentKeyID: 48547211
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 750848ce0e787506085899f4717730e1ca0a8f13
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868693"
---
# <a name="enabling-a-dll-to-run-on-dcom"></a>Aktivieren einer DLL für die Ausführung mit DCOM


**Betrifft**: Access 2013, Office 2013

In den folgenden Schritten wird skizziert, wie für Geschäftsobjekt-DLLs (Dynamic Link Libraries) ermöglicht wird, dass sie sowohl DCOM als auch Microsoft® Internetinformationsdienste (Internet Information Services, IIS) (HTTP) über Komponentendienste verwenden können.

1.  Erstellen Sie ein neues leeres Paket im MMC-Snap-In Komponentendienste. Mit dem MMC-Snap-In Komponentendienste erstellen Sie ein Paket und fügen dem Paket die DLL hinzu. Dadurch kann auf die DLL über DCOM zugegriffen werden, aber nicht mehr über IIS. (Wenn Sie die Registrierung für die DLL überprüfen, stellen Sie fest, dass der **Inproc** -Schlüssel jetzt leer ist. Durch Festlegen des Aktivierungsattributs wird dem **Inproc** -Schlüssel ein Wert hinzugefügt. Dies wird weiter unten in diesem Thema erläutert.)

2.  Installieren Sie ein Geschäftsobjekt in dem Paket. -oder- Importieren Sie das [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekt in das Paket.

3.  Legen Sie das Aktivierungsattribut für das Paket auf **Im Prozess des Erstellers** (Bibliotheksanwendung) fest. Damit auf die DLL über DCOM und IIS auf dem gleichen Computer zugegriffen werden kann, müssen Sie das Aktivierungsattribut der Komponente im MMC-Snap-In Komponentendienste festlegen. Nachdem Sie das Attribute auf **Im Prozess des Erstellers** festgelegt haben, werden Sie feststellen, dass in der Registrierung ein **Inproc** -Serverschlüssel hinzugefügt wurde, der auf eine Ersatz-DLL der Komponentendienste verweist.

