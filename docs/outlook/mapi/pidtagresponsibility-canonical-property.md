---
title: Kanonische PidTagResponsibility-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResponsibility
api_type:
- COM
ms.assetid: 1e8ccef1-db0a-4230-9bd0-87540b53e890
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9dba26ab6948d7190521ff31a8732c4b058ab7c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794985"
---
# <a name="pidtagresponsibility-canonical-property"></a>Kanonische PidTagResponsibility-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält TRUE, wenn einige Adressbuchhierarchie bereits Verantwortung zur Übermittlung der Nachricht mit dieser Empfänger, und FALSE, wenn die Warteschlange MAPI berücksichtigt, dass dieser Transportdienst Verantwortung akzeptieren sollte angenommen hat.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_RESPONSIBILITY  <br/> |
|Bezeichner:  <br/> |0x0E0F  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |MAPI Übertragungseinehit  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn die MAPI-Warteschlange eine ausgehende Nachricht zu einem Transportanbieter über [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), stellt wird diese Eigenschaft auf FALSE für alle Empfänger für die die MAPI-Warteschlange, Adressbuchhierarchie verantwortlich und TRUE für alle berücksichtigt andere Empfänger. Der Adressbuchhierarchie sollten alle Empfänger **PR_RESPONSIBILITY** auf FALSE festgelegt werden. Nach dem erfolgreichen Senden oder nicht eindeutig an einen Empfänger senden sollte der Adressbuchhierarchie legen Sie diese Eigenschaft auf true fest, in der Quellnachricht, um anzugeben, dass er die Verantwortung für diesen Empfänger angenommen hat. 
  
Wenn nach der Prüfung eines Empfängers, ein Transportdienstes entscheidet, dass es keine sollte nicht behandelt, sollte der Adressbuchhierarchie **PR_RESPONSIBILITY** Set auf false festgelegt lassen. Die MAPI-Warteschlange sieht dann für einen anderen Transportanbieter, die diesen Empfänger verarbeitet werden können. Die MAPI-Warteschlange erstellt einen Unzustellbarkeitsbericht letztlich für alle Empfänger für die keine Adressbuchhierarchie Verantwortung annimmt. 
  
Wenn der Adressbuchhierarchie versucht und die Nachricht nicht zustellen fehlschlägt, sollten sie die [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) -Methode, um die Gründe für den Fehler MAPI mit, aufrufen, damit MAPI einen Unzustellbarkeitsbericht generieren kann. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagDeleteAfterSubmit-Eigenschaft](pidtagdeleteaftersubmit-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

