---
title: Kanonische Pidtagresponsibility (-Eigenschaft
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
ms.openlocfilehash: 15bf61e71a2c230f7891c738661f839ecddb52e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330121"
---
# <a name="pidtagresponsibility-canonical-property"></a>Kanonische Pidtagresponsibility (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn ein Transportanbieter bereits die Verantwortung für die Zustellung der Nachricht an diesen Empfänger übernommen hat, und FALSE, wenn der MAPI-Spooler der Ansicht ist, dass dieser Transportanbieter die Verantwortung übernehmen soll.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RESPONSIBILITY  <br/> |
|Kennung:  <br/> |0x0E0F  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Nicht transmitable MAPI  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn der MAPI-Spooler eine ausgehende Nachricht an einen Transportanbieter über [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md), wird diese Eigenschaft auf false für alle Empfänger festgelegt, für die der MAPI-Spooler der Ansicht ist, dass der Transportanbieter zuständig ist, und true für alle andere Empfänger. Der Transportanbieter sollte versuchen, alle Empfänger zu behandeln, bei denen **PR_RESPONSIBILITY** auf false festgelegt ist. Nach dem erfolgreichen senden oder ausschließenden Senden eines Empfängers durch den Transportanbieter sollte diese Eigenschaft in der Quellnachricht auf TRUE festgelegt werden, um anzugeben, dass Sie die Verantwortung für diesen Empfänger übernommen hat. 
  
Wenn ein Transportanbieter nach der Untersuchung eines Empfängers entscheidet, dass er nicht verarbeitet werden kann oder sollte, sollte **PR_RESPONSIBILITY** auf false festgelegt bleiben. Der MAPI-Spooler sucht dann nach einem anderen Transportanbieter, der diesen Empfänger verarbeiten kann. Der MAPI-Spooler erstellt schließlich einen Unzustellbarkeitsbericht für alle Empfänger, für die kein Transportanbieter die Verantwortung übernimmt. 
  
Wenn der Transportanbieter versucht, die Nachricht zu übermitteln, muss Sie die [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) -Methode aufrufen, um MAPI die Gründe für den Fehler anzuzeigen, damit MAPI einen Unzustellbarkeitsbericht generieren kann. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Ablauf für die Datenübertragung zwischen einem Client und einem Server.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagDeleteAfterSubmit-Eigenschaft](pidtagdeleteaftersubmit-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

