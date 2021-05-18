---
title: Excel Clusterconnectorfunktionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 41a5cf1ecb7c8f38f4aa5b62a493b3f45c2fe090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408586"
---
# <a name="excel-cluster-connector-functions"></a>Excel Clusterconnectorfunktionen

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel 2013 Clusterconnector-DLLs müssen die in diesem Abschnitt beschriebenen Funktionen implementieren.
  
Die in den Referenzthemen in diesem Abschnitt erwähnten Rückgabewerte sind in der SDK-Includedatei xlcall.h definiert.
  
## <a name="cluster-connector-architecture"></a>Clusterconnectorarchitektur

Excel aufruft Einstiegspunkte in einem Clusterconnector, um benutzerdefinierte Funktionsaufrufe an einen Hochleistungs-Computecluster und für die Clustersitzungsverwaltung zu übertragen.
  
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

