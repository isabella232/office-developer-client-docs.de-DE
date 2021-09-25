---
title: PidTagMessageDownloadTime (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMessageDownloadTime
api_type:
- HeaderDef
ms.assetid: f0d34dd6-7ddb-4843-b848-c89923ff80cc
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: efd60e712176188a42894a3c43bc5313fa53e3c9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555328"
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
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft wird in Sekunden ausgedrückt und stellt die beste Schätzung der Zeit dar, die ein Remote-Transportanbieter benötigen würde, um eine bestimmte Nachricht vom aktuellen Speicherort in einen Nachrichtenspeicher auf dem Client herunterzuladen, der den Headerordner anzeigt. Der Remotetransportanbieter berechnet in der Regel den Wert für diese Eigenschaft, indem der Wert der **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) -Eigenschaft durch die Geschwindigkeit der Kommunikationsverbindung in Bytes pro Sekunde geteilt wird. Wenn der Anbieter die Downloadzeit nicht berechnen kann, z. B. wenn er die Linkgeschwindigkeit nicht kennt, sollte er einen **PT_ERROR** Wert bereitstellen, z. **B. MAPI_E_NO_SUPPORT** für diese Spalte im Inhaltsverzeichnis des Kopfzeilenordners. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

