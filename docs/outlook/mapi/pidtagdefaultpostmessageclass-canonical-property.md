---
title: Kanonische PidTagDefaultPostMessageClass-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultPostMessageClass
api_type:
- HeaderDef
ms.assetid: 231c288f-547b-4463-9442-1499661b925e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0ab904625d3a23462a4fedf3b64f49c54b34ad28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357904"
---
# <a name="pidtagdefaultpostmessageclass-canonical-property"></a>Kanonische PidTagDefaultPostMessageClass-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Namen einer benutzerdefinierten Formular Nachrichtenklasse.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DEF_POST_MSGCLASS  <br/> |
|Kennung:  <br/> |0x36E5  <br/> |
|Datentyp:  <br/> |PT_STRING8  <br/> |
|Bereich:  <br/> |MAPI-Container  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft für einen Ordner festgelegt ist, muss der Wert entweder genau die Basisnachrichtenklasse enthalten (beispielsweise "IPM. Kontakt "für einen Kontakteordner oder" IPM. Termin "für einen Kalenderordner) oder beginnen Sie mit der Basisnachrichtenklasse (beispielsweise" IPM. Contact. myContact ").
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs-und Antwortnachrichten an.
    
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

