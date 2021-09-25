---
title: Excel Cluster-Connector-Funktionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: db4dec310a9c100ffba886b89c4cd82f519aa48a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552262"
---
# <a name="excel-cluster-connector-functions"></a>Excel Cluster-Connector-Funktionen

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel 2013 Clusterconnector-DLLs müssen die in diesem Abschnitt beschriebenen Funktionen implementieren.
  
Die in den Referenzthemen in diesem Abschnitt erwähnten Rückgabewerte sind in der SDK-Includedatei "xlcall.h" definiert.
  
## <a name="cluster-connector-architecture"></a>Clusterconnectorarchitektur

Excel Ruft Einstiegspunkte in einem Clusterconnector auf, um benutzerdefinierte Funktionsaufrufe an einen Hochleistungs-Computecluster und für die Clustersitzungsverwaltung zu übertragen.
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[CallUDF](calludf.md)
  
[CancelOutstandingRequests](canceloutstandingrequests.md)
  
[CloseSession](closesession.md)
  
[OpenSession](opensession.md)
  
[PingSession](pingsession.md)
  
[ShowOptions](showoptions.md)
  
## <a name="see-also"></a>Siehe auch



[Entwickeln von Excel-Clusterconnectors](developing-excel-cluster-connectors.md)
  
[Clustersichere Funktionen](cluster-safe-functions.md)

