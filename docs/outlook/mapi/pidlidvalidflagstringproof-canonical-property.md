---
title: PidLidValidFlagStringProof (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidValidFlagStringProof
api_type:
- COM
ms.assetid: e5a94968-7e84-4faf-8104-9ea36d35fa1a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 28f405493b919fb1e8a49a39575e0a75767a98be
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604397"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a>PidLidValidFlagStringProof (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft, ob der Wert der **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) -Eigenschaft von einem Agent festgelegt wurde, der den Wert der **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) -Eigenschaft erkannt hat.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidValidFlagStringProof  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x000085BF  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Vorgang  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Bei nicht sendenden Objekten (empfangene E-Mails und Nicht-E-Mail-Objekte) sollten Clients diesen Wert auf den Wert **von PR_MESSAGE_DELIVERY_TIME** festlegen, wenn **sie dispidRequest** ändern.
  
Da der Wert von **PR_MESSAGE_DELIVERY_TIME** vom Absender nicht prognostiziert werden kann und der Wert dieser Eigenschaft dem Wert von **PR_MESSAGE_DELIVERY_TIME** entspricht, ist es einigermaßen sicher, dass der Wert von **dispidRequest** nicht vom Absender der Nachricht stammt. Ein Client kann entscheiden, wie der Wert von **dispidRequest** für den Endbenutzer basierend auf dem Ergebnis dieses Vergleichs in Übereinstimmung mit der spezifischen Sicherheitsrichtlinie des Clients dargestellt werden soll. Wenn der Wert von **dispidRequest** aufgrund des Vorhandenseins eines Werts für **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) ignoriert wird, muss diese Eigenschaft ignoriert werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[PidTagMessageDeliveryTime (kanonische Eigenschaft)](pidtagmessagedeliverytime-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

