---
title: Ausführen von Geschäftsobjekten in Komponentendiensten
TOCTitle: Running Business Objects in Component Services
ms:assetid: 12103458-b1dd-10fc-37e8-883fd6c6b9d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248893(v=office.15)
ms:contentKeyID: 48543328
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0eb70a615f49ff351ec31a826abc9775558218dd
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862555"
---
# <a name="running-business-objects-in-component-services"></a>Ausführen von Geschäftsobjekten in Komponentendiensten


**Betrifft**: Access 2013 | Office 2013

Bei Geschäftsobjekten kann es sich um ausführbare Dateien (EXE) oder um Dynamic Link Libraries (DLL) handeln. Die für die Ausführung eines Geschäftsobjekts verwendete Konfiguration hängt davon ab, ob das Objekt eine DLL- oder eine EXE-Datei ist:

  - Als EXE-Dateien erstellte Geschäftsobjekte können über DCOM aufgerufen werden. Wenn diese Geschäftobjekte mit Internetinformationsdienste (Internet Information Services, IIS) verwendet werden, unterliegen sie einem zusätzlichen Marshalling der Daten. Dadurch wird die Leistung des Clients verringert.

  - Als DLL-Dateien erstellte Geschäftsobjekte können über IIS (und damit über HTTP ) verwendet werden. Über DCOM können sie nur mithilfe der Komponentendienste (oder Microsoft Transaction Server unter Windows NT) verwendet werden. Geschäftobjekt-DLLs müssen auf dem IIS-Servercomputer registriert werden, damit ein Zugriff über IIS möglich ist. (Schritte zum Konfigurieren einer DLL für die Ausführung mit DCOM finden Sie im Abschnitt [Aktivieren einer DLL für die Ausführung mit DCOM](enabling-a-dll-to-run-on-dcom.md).)


> [!NOTE]
> Wenn von Geschäftsobjekten auf der mittleren Ebene als Komponenten der Komponentendienste (mit **GetObjectContext**, **SetComplete**und **SetAbort**) implementiert werden, können sie Komponentendienste (oder MTS, bei Verwendung der Windows NT)-Objekte Kontext Verwalten von deren Status über mehrere Client-Anrufe. Dieses Szenario ist mit DCOM möglich, das üblicherweise zwischen vertrauenswürdigen Clients und Servern (ein Intranet) implementiert wird. 
>
> In diesem Fall werden das [RDS.DataSpace](dataspace-object-rds.md)-Objekt und die [CreateObject](createobject-method-rds.md)-Methode auf dem Client durch das Transaktionskontextobjekt und die **CreateInstance** -Methode ersetzt (bereitgestellt von der **ITransactionContext** -Schnittstelle), die von den Komponentendiensten implementiert wird.


## <a name="see-also"></a>Siehe auch

- [Ausführen von Geschäftsobjekten in Komponentendiensten (SQLServer)](https://docs.microsoft.com/sql/ado/guide/remote-data-service/running-business-objects-in-component-services?view=sql-server-2017)