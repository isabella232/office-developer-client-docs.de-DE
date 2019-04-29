---
title: Entwickeln von Excel-Cluster-Konnektoren
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
# <a name="developing-excel-cluster-connectors"></a>Entwickeln von Excel-Cluster-Konnektoren

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel-Cluster-Konnektoren bieten eine Möglichkeit, Cluster sichere benutzerdefinierte Funktionsaufrufe in einer XLL automatisch an einen gruppierten Server zu verschieben. Eine Beschreibung der Cluster sicheren benutzerdefinierten Funktionen finden Sie unter [Cluster Safe Functions](cluster-safe-functions.md). Diese Verschiebung kann die Leistung verbessern, indem mehr Computerressourcen verwendet werden können. Ein Cluster-Konnektor wird in der Regel von einem Hochleistungs-Compute-Cluster-Anbieter entwickelt.
  
## <a name="cluster-connectors"></a>Cluster-Konnektoren

Ein Cluster-Konnektor ist eine DLL, die definierte Einstiegspunkte bereitstellt, die Excel zum Koordinieren von Cluster sicheren benutzerdefinierten Funktionsaufrufen verwendet. Sie dient als Schnittstelle zwischen Excel und dem Hochleistungs-Compute-Cluster, für die Sitzungsverwaltung, für Funktionsaufrufe (durch Übergeben des vollqualifizierten Funktionsnamens und der tatsächlichen Argumente des Aufrufs) sowie für das Zurückgeben von Anruf Ergebnissen an Excel über eine Callback-Mechanismus.
  
Erstellen Sie zum Erstellen eines Cluster-Konnektors eine DLL, die die in den [Excel-Cluster](excel-cluster-connector-functions.md)-konnektorfunktionen aufgeführten Einstiegspunkte verfügbar macht.
  
## <a name="installing-a-cluster-connector"></a>Installieren eines Cluster-Konnektors

Damit ein Cluster-Konnektor in Excel verfügbar ist, muss der Setup-Code des Connectors die DLL des Connectors auf dem Computer installieren, auf dem Excel installiert ist. Darüber hinaus muss der Setup-Code des Connectors einen Eintrag für den Connector unter dem folgenden Registrierungsschlüssel hinzufügen:
  
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel-Cluster-Connectors \
  
Fügen Sie diesem Schlüssel einen Knoten für den Cluster-Konnektor hinzu, der die folgenden Zeichenfolgen angibt:
  
-  `Name`– der Name, der in der Liste der Cluster-Konnektoren in Excel angezeigt wird.
    
-  `Filename`– der vollständige Pfad für die DLL.
    

