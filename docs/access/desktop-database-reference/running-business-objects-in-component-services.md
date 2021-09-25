---
title: Ausführen von Geschäftsobjekten in Komponentendiensten
TOCTitle: Running business objects in component services
ms:assetid: 12103458-b1dd-10fc-37e8-883fd6c6b9d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248893(v=office.15)
ms:contentKeyID: 48543328
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c3b3b189f97cfc7aa338614d06c75437eb3b24df
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601835"
---
# <a name="running-business-objects-in-component-services"></a>Ausführen von Geschäftsobjekten in Komponentendiensten

**Gilt für**: Access 2013, Office 2013

Bei Geschäftsobjekten kann es sich um ausführbare Dateien (EXE) oder um Dynamic Link Libraries (DLL) handeln. Die für die Ausführung eines Geschäftsobjekts verwendete Konfiguration hängt davon ab, ob das Objekt eine DLL- oder eine EXE-Datei ist:

- Als EXE-Dateien erstellte Geschäftsobjekte können über DCOM aufgerufen werden. Wenn diese Geschäftobjekte mit Internetinformationsdienste (Internet Information Services, IIS) verwendet werden, unterliegen sie einem zusätzlichen Marshalling der Daten. Dadurch wird die Leistung des Clients verringert.

- Als DLL-Dateien erstellte Geschäftsobjekte können über IIS (und damit über HTTP ) verwendet werden. Über DCOM können sie nur mithilfe der Komponentendienste (oder Microsoft Transaction Server unter Windows NT) verwendet werden. Geschäftobjekt-DLLs müssen auf dem IIS-Servercomputer registriert werden, damit ein Zugriff über IIS möglich ist. (Schritte zum Konfigurieren einer DLL für die Ausführung mit DCOM finden Sie im Abschnitt [Aktivieren einer DLL für die Ausführung mit DCOM](enabling-a-dll-to-run-on-dcom.md).)


> [!NOTE]
> Wenn Geschäftsobjekte auf der mittleren Ebene als Komponenten der Komponenten der Komponenten für komponenten (mit **GetObjectContext,** **SetComplete** und **SetAbort)** implementiert werden, können sie Component Services (oder MTS, wenn Sie Windows NT)-Kontextobjekte verwenden, um ihren Status über mehrere Clientaufrufe hinweg aufrechtzuerhalten. Dieses Szenario ist mit DCOM möglich, das üblicherweise zwischen vertrauenswürdigen Clients und Servern (ein Intranet) implementiert wird. 
>
> In diesem Fall werden das [RDS.DataSpace](dataspace-object-rds.md)-Objekt und die [CreateObject](createobject-method-rds.md)-Methode auf dem Client durch das Transaktionskontextobjekt und die **CreateInstance** -Methode ersetzt (bereitgestellt von der **ITransactionContext** -Schnittstelle), die von den Komponentendiensten implementiert wird.


## <a name="see-also"></a>Siehe auch

- [Ausführen von Geschäftsobjekten in Komponentendiensten (SQL Server)](https://docs.microsoft.com/sql/ado/guide/remote-data-service/running-business-objects-in-component-services?view=sql-server-2017)
