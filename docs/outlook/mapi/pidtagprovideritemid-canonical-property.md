---
title: Kanonische Pidtagprovideritemid (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderItemId
api_type:
- COM
ms.assetid: fadbf1af-32c2-43ea-8475-15b31b2a9e68
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 48653b86d625da963b655dbd1acc01a46f4687dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412121"
---
# <a name="pidtagprovideritemid-canonical-property"></a>Kanonische Pidtagprovideritemid (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Bezeichner für einen Ordner oder ein Element in einem Speicher an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PROVIDER_ITEMID  <br/> |
|Kennung:  <br/> |0x0EA3  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MapiNonTransmittable  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Speicheranbieter können einen Wert für diese Eigenschaft für einen Ordner oder ein Element angeben, sollten den Wert jedoch zwischen den Sitzungen gleich bleiben. Speicheranbieter verwenden Sie diese Eigenschaft, um Suchergebnisse zu identifizieren, die von einer Suchmaschine zurückgegeben werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

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

