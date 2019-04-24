---
title: Kanonische Pidlidvalidflagstringproof (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: dfe3b57c246e247eda365bed46af2e0f35f0e54b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315386"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a>Kanonische Pidlidvalidflagstringproof (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Überprüft, ob der Wert der **dispidRequest** ([pidlidflagrequest (](pidlidflagrequest-canonical-property.md))-Eigenschaft von einem Agent festgelegt wurde, der den Wert der **PR_MESSAGE_DELIVERY_TIME** ([pidtagmessagedeliverytime (](pidtagmessagedeliverytime-canonical-property.md))-Eigenschaft kannte.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidValidFlagStringProof  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long-ID (Deckel):  <br/> |0x000085BF  <br/> |
|Datentyp:  <br/> |PT_SYSTIME  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Bei nicht-sendenden Objekten (empfangene e-Mails und nicht-e-Mail-Objekte) sollten Clients diesen Wert beim Ändern von **dispidRequest**auf den Wert von **PR_MESSAGE_DELIVERY_TIME** festlegen.
  
Da der Wert von **PR_MESSAGE_DELIVERY_TIME** nicht vom Absender vorhergesagt werden kann, ist der Wert dieser Eigenschaft gleich dem Wert von **PR_MESSAGE_DELIVERY_TIME**, aber es ist ziemlich sicher, dass der Wert von **dispidRequest** nicht vom Absender der Nachricht. Ein Client kann entscheiden, wie der Endbenutzer den Wert von **dispidRequest** basierend auf dem Ergebnis dieses Vergleichs gemäß der spezifischen Sicherheitsrichtlinie des Clients darstellen soll. Wenn der Wert von **dispidRequest** aufgrund des Vorhandenseins eines Werts für **dispidFlagStringEnum** ([pidlidflagstring (](pidlidflagstring-canonical-property.md)) ignoriert wird, muss diese Eigenschaft ignoriert werden.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Markierung an.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[Kanonische Pidtagmessagedeliverytime (-Eigenschaft](pidtagmessagedeliverytime-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

