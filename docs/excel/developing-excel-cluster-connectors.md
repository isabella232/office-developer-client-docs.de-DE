---
title: Entwickeln von Excel-Clusterconnectoren
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b538ae44-37d2-496b-b6e7-b0e39f6e38cb
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8c9a166ac06685c0a450e1e0bd60b2fbef67d336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790386"
---
# <a name="developing-excel-cluster-connectors"></a>Entwickeln von Excel-Clusterconnectoren

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel-clusterconnectoren bieten eine Möglichkeit zum Aufrufen der clustersichere benutzerdefinierte Funktion in einer XLL für einen gruppierten Server automatisch verlagern. Eine Beschreibung der benutzerdefinierten Funktionen clustersichere finden Sie unter [Clustersichere Funktionen](cluster-safe-functions.md). Diese Verschiebung kann Leistung verbessern, indem Sie weitere Netzwerke-Ressourcen verwendet werden. Ein Clusterconnector wird in der Regel durch eine hohe Leistung Compute Cluster Hersteller entwickelt.
  
## <a name="cluster-connectors"></a>Clusterconnectoren

Ein Clusterconnector ist, dass eine DLL, die definierten Einstiegspunkte, um Excel bietet wird verwendet, um benutzerdefinierte Funktion clustersichere Anrufe zu koordinieren. Dient als Schnittstelle zwischen Excel und leistungsfähige Computerclusters für Sitzung Management, zum Beschleunigen des Funktion aufruft (durch das übergeben den Namen der Funktion voll qualifizierte und den Anruf übergebene Argumente) und für die Rückgabe der Ergebnisse nach Excel über eine Rückrufmechanismus.
  
Um einen Clusterconnector zu erstellen, erstellen Sie eine DLL, die die Einstiegspunkte aufgeführt, die in [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)verfügbar macht.
  
## <a name="installing-a-cluster-connector"></a>Installieren eines Clusterconnectors

Der Setupcode der Verbindung muss einen Clusterconnector in Excel zur Verfügung zu stellen, die DLL der Verbindung auf dem Computer installieren, auf dem Excel installiert ist. Darüber hinaus muss der Setup-Code der Verbindung einen Eintrag für den Connector unter den folgenden Registrierungsschlüssel hinzufügen:
  
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\Excel\Excel Cluster Connectors\
  
Fügen Sie einen Knoten auf diesen Schlüssel für den Clusterconnector, der angibt, die in der folgenden Zeichenfolgen:
  
-  `Name`– der Name, der in der Liste der clusterconnectoren in Excel angezeigt wird.
    
-  `Filename`– der vollständige Pfad für die DLL.
    

