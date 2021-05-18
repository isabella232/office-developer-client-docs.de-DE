---
title: PidTagMessageDownloadTime (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8078d31af497a437c983da7447a0aebbdfb643fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407928"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a>PidTagMessageDownloadTime (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die geschätzte Zeit zum Herunterladen einer Nachricht von einem Remoteserver in einen lokalen Nachrichtenspeicher. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MESSAGE_DOWNLOAD_TIME  <br/> |
|Kennung:  <br/> |0x0E18  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird in Sekunden ausgedrückt und stellt die beste Schätzung der Zeit dar, die ein Remotetransportanbieter zum Herunterladen einer bestimmten Nachricht vom aktuellen Speicherort in einen lokalen Nachrichtenspeicher für den Client, der den Kopfzeilenordner anzeigen würde, in Kauf nehmen würde. Der Remotetransportanbieter berechnet in der Regel den Wert für diese Eigenschaft, indem er den Wert der **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))-Eigenschaft durch die Geschwindigkeit der Kommunikationsverbindung in Bytes pro Sekunde dividiert. Wenn der Anbieter die Downloadzeit nicht berechnen kann, z. B. wenn er die Verbindungsgeschwindigkeit nicht kennt, sollte er einen **PT_ERROR-Wert** wie **MAPI_E_NO_SUPPORT** für diese Spalte in der Inhaltstabelle des Kopfzeilenordners zur Verfügung stellt. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

