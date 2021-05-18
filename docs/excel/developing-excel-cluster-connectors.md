---
title: Entwickeln Excel Clusterconnectors
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e1c70713586a7a143f119a2c3e9d34b982dcedba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412597"
---
# <a name="developing-excel-cluster-connectors"></a>Entwickeln Excel Clusterconnectors

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel Clusterconnectors bieten eine Möglichkeit zum automatischen Ausladen von clustersicheren benutzerdefinierten Funktionsaufrufen in einer XLL an einen gruppierten Server. Eine Beschreibung der clustersicheren benutzerdefinierten Funktionen finden Sie unter [Cluster Safe Functions](cluster-safe-functions.md). Dieses Offloading kann die Leistung verbessern, indem mehr Rechenressourcen verwendet werden können. Ein Clusterconnector wird in der Regel von einem Anbieter von Hochleistungs-Computeclustern entwickelt.
  
## <a name="cluster-connectors"></a>Clusterconnectors

Ein Clusterconnector ist eine DLL, die definierte Einstiegspunkte Excel, die zum Koordinieren von clustersicheren benutzerdefinierten Funktionsaufrufen verwendet werden. Sie dient als Schnittstelle zwischen Excel und dem Hochleistungs-Computecluster, für die Sitzungsverwaltung, für Funktionsaufrufe (durch Übergeben des vollqualifizierten Funktionsnamens und der tatsächlichen Argumente des Aufrufs) und zum Zurückgeben von Anrufergebnissen an Excel über einen Rückrufmechanismus.
  
Um einen Clusterconnector zu erstellen, erstellen Sie eine DLL, die die einstiegspunkte verfügbar macht, die in Excel [Clusterconnectorfunktionen aufgeführt sind.](excel-cluster-connector-functions.md)
  
## <a name="installing-a-cluster-connector"></a>Installieren eines Clusterconnector

Um einen Clusterconnector in Excel verfügbar zu machen, muss der Setupcode des Connectors die DLL des Connectors auf dem Computer installieren, auf dem Excel installiert ist. Darüber hinaus muss der Setupcode des Connectors einen Eintrag für den Connector unter dem folgenden Registrierungsschlüssel hinzufügen:
  
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\
  
Fügen Sie diesem Schlüssel für den Clusterconnector einen Knoten hinzu, der die folgenden Zeichenfolgen angibt:
  
-  `Name`– der Name, der in der Liste der Clusterconnectors in Excel.
    
-  `Filename`– der vollständige Pfad für die DLL.
    

