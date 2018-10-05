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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391955"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a>PidLidValidFlagStringProof (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft, ob **DispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) den Wert der Eigenschaft von einem Agent festgelegt wurde, die den Wert der Eigenschaft **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) bekannt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidValidFlagStringProof  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Common  <br/> |
|Long-ID (Abdeckung):  <br/> |0x000085BF  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Hinweise

Für nicht-sendable-Objekte (empfangene Nachrichten und nicht-Mail-Objekte) sollten Clients dieser Wert auf den Wert der **PR_MESSAGE_DELIVERY_TIME** festgelegt, wenn **DispidRequest**ändern.
  
Da der Wert der **PR_MESSAGE_DELIVERY_TIME** ist der Wert dieser Eigenschaft gleich dem Wert der **PR_MESSAGE_DELIVERY_TIME**vom Absender, vorhergesagt werden nicht möglich, ist es nach vernünftigem Ermessen sicher, dass der Wert der **DispidRequest** nicht der Absender der Nachricht stammen. Ein Client kann entscheiden, wie den Wert der **DispidRequest** für den Endbenutzer basierend auf dem Ergebnis des Vergleichs gemäß den spezifischen Codezugriffssicherheits-Richtlinie des Clients zu präsentieren. Wenn der Wert der **DispidRequest** aufgrund von das Vorhandensein eines Werts für **DispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) ignoriert wird, muss diese Eigenschaft ignoriert.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[PidTagMessageDeliveryTime (kanonische Eigenschaft)](pidtagmessagedeliverytime-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

