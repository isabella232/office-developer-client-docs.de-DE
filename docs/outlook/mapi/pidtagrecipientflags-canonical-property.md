---
title: Kanonische PidTagRecipientFlags-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientFlags
api_type:
- COM
ms.assetid: 9fbe537f-b5fe-48a2-803c-653c50c82efd
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7b791d75c2a76ea1a504c0d8862dd20f5365b475
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356700"
---
# <a name="pidtagrecipientflags-canonical-property"></a>Kanonische PidTagRecipientFlags-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt ein Bitfeld an, in dem der Empfängerstatus beschrieben wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RECIPIENT_FLAGS  <br/> |
|Kennung:  <br/> |0x5FFD  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Transport Empfänger  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist nicht erforderlich. Es folgen die einzelnen Flags, die festgelegt werden können.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|S (recipSendable, 0x00000001)  <br/> |Der Empfänger ist ein **sendender** Teilnehmer. Dieses Flag wird nur in der **dispidApptUnsendableRecips** ([pidlidappointmentunsendablerecipients (](pidlidappointmentunsendablerecipients-canonical-property.md))-Eigenschaft verwendet.  <br/> |
|O (recipOrganizer, 0x0000002)  <br/> |Der **RecipientRow** , auf dem dieses Flag festgelegt ist, stellt den Besprechungsorganisator dar.  <br/> |
|ER (recipExceptionalResponse, 0x00000010)  <br/> |Gibt an, dass der Teilnehmer eine Antwort auf die Ausnahme gegeben hat, in der sich diese **RecipientRow** befindet. Dieses Flag wird nur in einem **RecipientRow** -Objekt des Meeting-Objekts des Organisators verwendet.  <br/> |
|ED (recipExceptionalDeleted, 0x00000020)  <br/> |Gibt an, dass, obwohl das **RecipientRow** vorhanden ist, es behandelt werden sollte, als ob der entsprechende Empfänger nicht. Dieses Flag wird nur in einem **RecipientRow** -Objekt des Meeting-Objekts des Organisators verwendet.  <br/> |
|X (reserviert, 0x00000040)  <br/> |Darf nicht festgelegt werden.  <br/> |
|X (reserviert, 0x00000080)  <br/> |Darf nicht festgelegt werden.  <br/> |
|G (recipOriginal, 0x00000100)  <br/> |Gibt an, dass der Empfänger ein ursprünglicher Teilnehmer ist. Dieses Flag wird nur in der **dispidApptUnsendableRecips** -Eigenschaft verwendet.  <br/> |
|X (reserviert, 0x00000200)  <br/> |Reserviert.  <br/> |
   
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

