---
title: Kanonische Pidtagproviderparentitemid (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderParentItemId
api_type:
- COM
ms.assetid: 6adb8e85-ae56-4542-8b19-ed3cfe7fe522
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0f99cf38e65c75ce1ba74bf72d88e19f4fbfa03a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286446"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a>Kanonische Pidtagproviderparentitemid (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Bezeichner für das übergeordnete Element eines Ordners oder eines Elements in einem Speicher an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PROVIDER_PARENT_ITEMID  <br/> |
|Kennung:  <br/> |0x0EA4  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Nicht transmitable MAPI  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Speicheranbieter können einen Wert für diese Eigenschaft für ein übergeordnetes Element eines Ordners oder eines Elements angeben, aber den Wert zwischen den Sitzungen beibehalten. Speicheranbieter verwenden Sie diese Eigenschaft, um Suchergebnisse zu identifizieren, die von einer Suchmaschine zurückgegeben werden.
  
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

