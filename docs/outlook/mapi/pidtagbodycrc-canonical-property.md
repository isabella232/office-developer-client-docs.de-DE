---
title: Kanonische Pidtagbodycrc (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyCrc
api_type:
- HeaderDef
ms.assetid: 6efe9dc3-e988-4042-ab02-2863b5e0f294
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 416486c3b06c485a1fa6525b54c37a6e0d23f56c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415180"
---
# <a name="pidtagbodycrc-canonical-property"></a>Kanonische Pidtagbodycrc (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen CRC-Wert (zyklische Redundanzprüfung) für den Nachrichtentext.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_BODY_CRC  <br/> |
|Kennung:  <br/> |0x0E1C  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Nachrichtenspeicher kann einen beliebigen CRC-Algorithmus verwenden, der einen PT_LONG-Wert generiert. Diese Eigenschaft muss als Teil der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode berechnet werden, wenn die **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md))-Eigenschaft zum ersten Mal festgelegt wurde und wenn Sie anschließend geändert wurde.
  
Eine Clientanwendung verwendet **PR_BODY_CRC** , um die in **PR_BODY** -Eigenschaften oder deren Varianten enthaltenen Nachrichtentext Zeichenfolgen zu vergleichen. Mit dieser Eigenschaft kann der Client schnell und einfach erkennen, wann der Nachrichtentext geändert wurde. Mithilfe von **PR_BODY_CRC** können Sie beträchtliche Leistungssteigerungen erzielen, statt **PR_BODY** aus dem Nachrichtenspeicher abzurufen und mit einer lokalen Version zu vergleichen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

