---
title: PidLidValidFlagStringProof (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidValidFlagStringProof
api_type:
- COM
ms.assetid: e5a94968-7e84-4faf-8104-9ea36d35fa1a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: dfe3b57c246e247eda365bed46af2e0f35f0e54b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315386"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a>PidLidValidFlagStringProof (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft, ob der Wert der **eigenschaft dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) von einem Agent festgelegt wurde, der den Wert der **eigenschaft PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) kannte.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidValidFlagStringProof  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Lange ID (LID):  <br/> |0x000085BF  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Hinweise

Bei objekten, die nicht gesendet werden können (empfangene E-Mails und  Nicht-E-Mail-Objekte), sollten Clients diesen Wert auf den Wert PR_MESSAGE_DELIVERY_TIME, wenn **dispidRequest geändert wird.**
  
Da der Wert von **PR_MESSAGE_DELIVERY_TIME** vom Absender nicht vorhergesagt werden kann, wenn der Wert dieser Eigenschaft dem Wert von **PR_MESSAGE_DELIVERY_TIME** entspricht, ist es vernünftigerweise sicher, dass der Wert von **dispidRequest** nicht vom Absender der Nachricht stammt. Ein Client kann entscheiden, wie der Wert von **dispidRequest** dem Endbenutzer basierend auf dem Ergebnis dieses Vergleichs in Übereinstimmung mit der spezifischen Sicherheitsrichtlinie des Clients angezeigt wird. Wenn der Wert **von dispidRequest** aufgrund des Vorhandenseins eines Werts für **dispidFlagStringEnum** ([PidLidFlagString)](pidlidflagstring-canonical-property.md)ignoriert wird, muss diese Eigenschaft ignoriert werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[PidTagMessageDeliveryTime (kanonische Eigenschaft)](pidtagmessagedeliverytime-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

