---
title: PidTagCorrelateMtsid (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelateMtsid
api_type:
- HeaderDef
ms.assetid: d0fc4e91-ed90-4d27-bd23-f01e99728e2d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 468cda97398bc393b1c0a65e2c13df5ba3ade3aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568910"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a>PidTagCorrelateMtsid (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält die Nachricht Transfer System (MTS)-ID in Korrelation Berichte mit gesendete Nachrichten verwendet.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CORRELATE_MTSID  <br/> |
|Kennung:  <br/> |0x0E0D  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn ein Transportdienstes eine gesendete Nachricht mit dieser Eigenschaft auf true fest, erkennt, wird diese Eigenschaft die MTS-ID für diese Nachricht. Nach der Übermittlung wird diese Eigenschaft mit der Nachricht im Ordner Gesendete Elemente zwischen Personen Nachricht (IPM) gespeichert.
  
Behalten Sie den Bezeichner als Teil des Umschlags Transport die ursprüngliche Nachricht wird und Berichte, die als Reaktion auf es generiert Messaging-Systeme, die Korrelations-ID MTS unterstützen, beispielsweise x. 400. Wenn ein Bericht aus einem solchen messaging System übermittelt werden, wird der Adressbuchhierarchie diese Eigenschaft auf den ursprünglichen MTS Bezeichner aus den Bericht Transport Umschlag an. Diese Eigenschaft wird mit dem Bericht gespeichert.
  
Eine Clientanwendung kann alle Nachrichten, die mit dieser Eigenschaft einen Suchergebnisse Ordner verwalten. Wenn ein Bericht für diese Meldung eingeht, kann der Client gelten Beschränkungen in den Suchergebnissen Ordner, suchen Sie nach der ursprünglichen Version der Nachricht und korrelieren die ursprünglichen Nachrichteninformationen mit den neuen Informationen.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

