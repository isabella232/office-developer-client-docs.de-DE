---
title: PidTagRecipientTrackStatus (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRecipientTrackStatus
api_type:
- COM
ms.assetid: d619b5e7-2867-44fc-9b42-123bb1bf7bde
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 26662eb83a757f798fa1117d639705d2cc3c557c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570909"
---
# <a name="pidtagrecipienttrackstatus-canonical-property"></a>PidTagRecipientTrackStatus (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Antwortstatus an, der vom Teilnehmer zurückgegeben wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RECIPIENT_TRACKSTATUS  <br/> |
|Kennung:  <br/> |0x5FFF  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Transportempfänger  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn dieser Wert nicht festgelegt ist, muss davon ausgegangen werden, dass er respNone ist. Andernfalls muss es eine der folgenden Komponenten sein:
  
|**Antwortstatus**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|respNone  <br/> |0x00000000  <br/> |Für dieses Objekt ist keine Antwort erforderlich. Dies ist bei Terminobjekten und Besprechungsantwortobjekten der Fall.  <br/> |
|respTentative  <br/> |0x00000002  <br/> |Dieser Wert für das Besprechungsobjekt des Teilnehmers gibt an, dass der Teilnehmer das Besprechungsanfrageobjekt mit Vorbehalt angenommen hat.  <br/> |
|respAccepted  <br/> |0x00000003  <br/> |Dieser Wert für das Besprechungsobjekt des Teilnehmers gibt an, dass der Teilnehmer das Besprechungsanfrageobjekt akzeptiert hat.  <br/> |
|respDeclined  <br/> |0x00000004  <br/> |Dieser Wert für das Besprechungsobjekt des Teilnehmers gibt an, dass der Teilnehmer das Besprechungsanfrageobjekt abgelehnt hat.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Termin-, Besprechungsanfrage- und Antwortnachrichten an.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
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

