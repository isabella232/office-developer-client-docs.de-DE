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
ms.openlocfilehash: 96bfc184752b6a3e15434ad67ac8c2b4b26cac4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426835"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a>PidTagCorrelateMtsid (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die ID des Nachrichtenübertragungssystems (Message Transfer System, MTS), die bei der Korrelierung von Berichten mit gesendeten Nachrichten verwendet wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CORRELATE_MTSID  <br/> |
|Kennung:  <br/> |0x0E0D  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn ein Transportanbieter eine übermittelte Nachricht mit dieser Eigenschaft auf TRUE trifft, wird diese Eigenschaft auf den MTS-Bezeichner für diese Nachricht festgelegt. Nach der Übertragung wird diese Eigenschaft mit der Nachricht im Ordner "Interpersonal Message( IPM) Gesendete Elemente" gespeichert.
  
Messagingsysteme, die die Korrelation nach MTS-Id unterstützen, z. B. X.400, behalten den Bezeichner als Teil des Transportumschlags der ursprünglichen Nachricht sowie aller berichte bei, die als Reaktion darauf generiert wurden. Wenn ein Bericht von einem solchen Messagingsystem zugestellt wird, legt der Transportanbieter diese Eigenschaft auf den ursprünglichen MTS-Bezeichner aus dem Transportumschlag des Berichts fest. Diese Eigenschaft wird dann mit dem Bericht gespeichert.
  
Eine Clientanwendung kann einen Suchergebnisordner aller Nachrichten mit dieser Eigenschaft verwalten. Wenn ein Bericht für eine solche Nachricht einkommt, kann der Client Einschränkungen auf den Suchergebnisordner anwenden, die ursprüngliche Version der Nachricht suchen und die ursprünglichen Nachrichteninformationen mit den neuen Informationen korrelieren.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

