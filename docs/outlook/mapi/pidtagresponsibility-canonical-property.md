---
title: Kanonische PidTagResponsibility-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagResponsibility
api_type:
- COM
ms.assetid: 1e8ccef1-db0a-4230-9bd0-87540b53e890
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bae0e9ac805e0d95f70db164e517db1434c5431c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591507"
---
# <a name="pidtagresponsibility-canonical-property"></a>Kanonische PidTagResponsibility-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn einige Transportanbieter bereits die Verantwortung für die Zustellung der Nachricht an diesen Empfänger akzeptiert haben, und FALSE, wenn der MAPI-Spooler der Ansicht ist, dass dieser Transportanbieter die Verantwortung übernehmen sollte.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RESPONSIBILITY  <br/> |
|Kennung:  <br/> |0x0E0F  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |MAPI nicht datenübertragungsfähig  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn der MAPI-Spooler einem Transportanbieter über [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)eine ausgehende Nachricht anzeigt, wird diese Eigenschaft für alle Empfänger, für die der MAPI-Spooler den verantwortlichen Transportanbieter betrachtet, auf FALSE und für alle anderen Empfänger auf TRUE festgelegt. Der Transportanbieter sollte versuchen, alle Empfänger zu **behandeln, wobei PR_RESPONSIBILITY** auf FALSE festgelegt ist. Nach dem erfolgreichen Senden an einen Empfänger oder dem erfolgreichen Senden an einen Empfänger sollte der Transportanbieter diese Eigenschaft in der Quellnachricht auf TRUE festlegen, um anzugeben, dass er die Verantwortung für diesen Empfänger akzeptiert hat. 
  
Wenn ein Transportanbieter nach der Untersuchung eines Empfängers entscheidet, dass er ihn nicht verarbeiten kann oder soll, sollte der Transportanbieter **PR_RESPONSIBILITY** auf FALSE festgelegt lassen. Der MAPI-Spooler sucht dann nach einem anderen Transportanbieter, der diesen Empfänger verarbeiten kann. Der MAPI-Spooler erstellt letztendlich einen Nicht-Empfängerbericht, für den kein Transportanbieter verantwortlich ist. 
  
Wenn der Transportanbieter versucht und die Nachricht nicht zuzustellen versucht, sollte er die [IMAPISupport::StatusRecips-Methode](imapisupport-statusrecips.md) aufrufen, um der MAPI die Gründe für den Fehler anzugeben, sodass die MAPI einen Nichtzustellbarkeitsbericht generieren kann. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagDeleteAfterSubmit-Eigenschaft](pidtagdeleteaftersubmit-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

