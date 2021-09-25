---
title: Entwickeln von Excel-Clusterconnectors
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 67fd0af130351ad48599c9e6ac82bd280eb4f561
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552269"
---
# <a name="developing-excel-cluster-connectors"></a>Entwickeln von Excel-Clusterconnectors

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel Clusterconnectors bieten eine Möglichkeit, clustersichere benutzerdefinierte Funktionsaufrufe in einer XLL automatisch an einen Clusterserver zu entladen. Eine Beschreibung der clustersicheren benutzerdefinierten Funktionen finden Sie unter [Cluster Tresor Functions](cluster-safe-functions.md). Diese Auslagerung kann die Leistung verbessern, indem mehr Computerressourcen verwendet werden können. Ein Clusterconnector wird in der Regel von einem Anbieter von Rechenclustern mit hoher Leistung entwickelt.
  
## <a name="cluster-connectors"></a>Clusterconnectors

Ein Clusterconnector ist eine DLL, die definierte Einstiegspunkte bereitstellt, die Excel zum Koordinieren von clustersicheren benutzerdefinierten Funktionsaufrufen verwendet. Es dient als Schnittstelle zwischen Excel und dem hochleistungsfähigen Computecluster, für die Sitzungsverwaltung, für Funktionsaufrufe (durch Übergeben des vollqualifizierten Funktionsnamens und der tatsächlichen Argumente des Aufrufs) und zum Zurückgeben von Anrufergebnissen an Excel über einen Rückrufmechanismus.
  
Um einen Clusterconnector zu erstellen, erstellen Sie eine DLL, die die einstiegspunkte verfügbar macht, die in [Excel Cluster Connector Functions](excel-cluster-connector-functions.md)aufgeführt sind.
  
## <a name="installing-a-cluster-connector"></a>Installieren eines Clusterconnectors

Damit ein Clusterconnector in Excel verfügbar ist, muss der Setupcode des Connectors die DLL des Connectors auf dem Computer installieren, auf dem Excel installiert ist. Darüber hinaus muss der Setupcode des Connectors einen Eintrag für den Connector unter dem folgenden Registrierungsschlüssel hinzufügen:
  
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\
  
Fügen Sie diesem Schlüssel für den Clusterconnector einen Knoten hinzu, der die folgenden Zeichenfolgen angibt:
  
-  `Name`– der Name, der in der Liste der Clusterconnectors in Excel angezeigt wird.
    
-  `Filename`– der vollständige Pfad für die DLL.
    

