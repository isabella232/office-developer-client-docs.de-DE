---
title: Excel-Cluster-Konnektorfunktionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 41a5cf1ecb7c8f38f4aa5b62a493b3f45c2fe090
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311067"
---
# <a name="excel-cluster-connector-functions"></a>Excel-Cluster-Konnektorfunktionen

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel 2013-Cluster-Connector-DLLs müssen die in diesem Abschnitt beschriebenen Funktionen implementieren.
  
Die in den Referenzthemen in diesem Abschnitt genannten Rückgabewerte sind in der SDK-Include-Datei xlcall. h definiert.
  
## <a name="cluster-connector-architecture"></a>Cluster-Connector-Architektur

Excel ruft Einstiegspunkte in einem Cluster-Konnektor auf, um benutzerdefinierte Funktionsaufrufe an einen Hochleistungs-Compute-Cluster und für die Cluster Sitzungsverwaltung zu übertragen.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[CallUDF](calludf.md)
  
[CancelOutstandingRequests](canceloutstandingrequests.md)
  
[CloseSession](closesession.md)
  
[OpenSession](opensession.md)
  
[PingSession](pingsession.md)
  
[ShowOptions](showoptions.md)
  
## <a name="see-also"></a>Siehe auch



[Entwickeln von Excel 2013-Clusterconnectoren](developing-excel-cluster-connectors.md)
  
[Clustersichere Funktionen](cluster-safe-functions.md)

