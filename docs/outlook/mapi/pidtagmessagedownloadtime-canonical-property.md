---
title: Kanonische PidTagMessageDownloadTime-Eigenschaft
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
ms.openlocfilehash: b47d104ade6a7d23f5630d15697b330360d027b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794603"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a>Kanonische PidTagMessageDownloadTime-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält die geschätzte Zeit bis zum Laden Sie einer Nachricht von einem Remoteserver zu einem lokalen Nachrichtenspeicher. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_MESSAGE_DOWNLOAD_TIME  <br/> |
|Bezeichner:  <br/> |0x0E18  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeine messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird in Sekunden ausgedrückt und stellt die bestmögliche Schätzung der Zeit an einen remote-Transport-Anbieter zu eine bestimmte Nachricht von seinem aktuellen Speicherort auf einen Nachrichtenspeicher herunterladen lokalen an dem Client, die das Anzeigen des Ordners Kopfzeile dauert. Der remote Adressbuchhierarchie berechnet den Wert für diese Eigenschaft in der Regel durch Dividieren des Werts der Eigenschaft **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) durch die Geschwindigkeit der Communications-Verknüpfung in Byte pro Sekunde. Wenn der Anbieter die Downloadzeit, z. B., wenn er die Übertragungsrate nicht kennt berechnen kann nicht sollte einen **PT_ERROR** -Wert wie **MAPI_E_NO_SUPPORT** für diese Spalte in der Kopfzeile Ordner Inhaltstabelle Büroplan. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

