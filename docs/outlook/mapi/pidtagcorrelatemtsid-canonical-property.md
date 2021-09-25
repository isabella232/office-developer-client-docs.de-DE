---
title: PidTagCorrelateMtsid (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagCorrelateMtsid
api_type:
- HeaderDef
ms.assetid: d0fc4e91-ed90-4d27-bd23-f01e99728e2d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 113fcb076d730ab63e7fbe6874a5cb4f77fb6565
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616530"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a>PidTagCorrelateMtsid (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den MTS-Bezeichner (Message Transfer System), der beim Korrelieren von Berichten mit gesendeten Nachrichten verwendet wird.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CORRELATE_MTSID  <br/> |
|Kennung:  <br/> |0x0E0D  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn ein Transportanbieter auf eine gesendete Nachricht trifft, deren Eigenschaft auf TRUE festgelegt ist, wird diese Eigenschaft auf den MTS-Bezeichner für diese Nachricht festgelegt. Nach der Übertragung wird diese Eigenschaft mit der Nachricht im Ordner "Gesendete Elemente" (Interpersonal Message, IPM) gespeichert.
  
Messagingsysteme, die die Korrelation anhand der MTS-ID unterstützen, z. B. X.400, behalten den Bezeichner als Teil des Transportumschlags der ursprünglichen Nachricht sowie aller Berichte, die als Reaktion darauf generiert werden. Wenn ein Bericht von einem solchen Messagingsystem übermittelt wird, legt der Transportanbieter diese Eigenschaft auf den ursprünglichen MTS-Bezeichner aus dem Transportumschlag des Berichts fest. Diese Eigenschaft wird dann mit dem Bericht gespeichert.
  
Eine Clientanwendung kann einen Suchergebnisordner aller Nachrichten mit dieser Eigenschaft verwalten. Wenn ein Bericht für eine solche Nachricht eingeht, kann der Client Einschränkungen auf den Suchergebnisordner anwenden, die ursprüngliche Version der Nachricht suchen und die ursprünglichen Nachrichteninformationen mit den neuen Informationen korrelieren.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

