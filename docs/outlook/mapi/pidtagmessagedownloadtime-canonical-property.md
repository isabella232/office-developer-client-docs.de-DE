---
title: Kanonische Pidtagmessagedownloadtime (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageDownloadTime
api_type:
- HeaderDef
ms.assetid: f0d34dd6-7ddb-4843-b848-c89923ff80cc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8078d31af497a437c983da7447a0aebbdfb643fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325676"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a>Kanonische Pidtagmessagedownloadtime (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die geschätzte Zeit zum Herunterladen einer Nachricht von einem Remoteserver zu einem lokalen Nachrichtenspeicher. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MESSAGE_DOWNLOAD_TIME  <br/> |
|Kennung:  <br/> |0x0E18  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeine Nachrichtenübermittlung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird in Sekunden ausgedrückt und stellt die beste Schätzung der Zeit dar, die ein Remote Transportanbieter zum Herunterladen einer bestimmten Nachricht vom aktuellen Speicherort zum lokalen Nachrichtenspeicher des Clients zum Anzeigen des Kopfzeilen Ordners benötigen würde. Der Remote Transportanbieter berechnet in der Regel den Wert für diese Eigenschaft, indem der Wert der **PR_MESSAGE_SIZE** ([pidtagmessagesize (](pidtagmessagesize-canonical-property.md))-Eigenschaft durch die Geschwindigkeit der Kommunikationsverbindung in Bytes pro Sekunde geteilt wird. Wenn der Anbieter die Downloadzeit nicht berechnen kann, beispielsweise wenn er die Verbindungsgeschwindigkeit nicht kennt, sollte er einen **PT_ERROR** -Wert wie **MAPI_E_NO_SUPPORT** für diese Spalte in der Tabelle mit den Kopfzeilen Ordnern liefern. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

