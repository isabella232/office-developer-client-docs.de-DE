---
title: PidTagRecipientFlags (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7b791d75c2a76ea1a504c0d8862dd20f5365b475
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356700"
---
# <a name="pidtagrecipientflags-canonical-property"></a>PidTagRecipientFlags (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt ein Bitfeld an, das den Empfängerstatus beschreibt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RECIPIENT_FLAGS  <br/> |
|Kennung:  <br/> |0x5FFD  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Transportempfänger  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist nicht erforderlich. Im Folgenden finden Sie die einzelnen Flags, die festgelegt werden können.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|S (recipSendable, 0x00000001)  <br/> |Der Empfänger ist ein **sendefähiger** Teilnehmer. Dieses Flag wird nur in der **eigenschaft dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)) verwendet.  <br/> |
|O (recipOrganizer, 0x0000002)  <br/> |Der **RecipientRow-Wert,** auf dem dieses Flag festgelegt ist, stellt den Besprechungsorganisator dar.  <br/> |
|ER (recipExceptionalResponse, 0x00000010)  <br/> |Gibt an, dass der Teilnehmer eine Antwort für die Ausnahme gegeben hat, in der sich dieses **RecipientRow** befindet. Dieses Flag wird nur in einem **RecipientRow-Objekt eines** eingebetteten Nachrichtenobjekts der Ausnahme des Besprechungsobjekts des Organisators verwendet.  <br/> |
|ED (recipExceptionalDeleted, 0x00000020)  <br/> |Gibt an, dass **der RecipientRow** zwar vorhanden ist, aber so behandelt werden sollte, als ob der entsprechende Empfänger dies nicht tut. Dieses Flag wird nur in einem **RecipientRow-Objekt eines** eingebetteten Nachrichtenobjekts der Ausnahme des Besprechungsobjekts des Organisators verwendet.  <br/> |
|X (reserviert, 0x00000040)  <br/> |Darf nicht festgelegt werden.  <br/> |
|X (reserviert, 0x00000080)  <br/> |Darf nicht festgelegt werden.  <br/> |
|G (recipOriginal, 0x00000100)  <br/> |Gibt an, dass der Empfänger ein ursprünglicher Teilnehmer ist. Dieses Flag wird nur in der **eigenschaft dispidApptUnsendableRecips** verwendet.  <br/> |
|X (reserviert, 0x00000200)  <br/> |Reserviert.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungs- und Antwortnachrichten an.
    
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

