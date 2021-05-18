---
title: PidTagResponsibility (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 15bf61e71a2c230f7891c738661f839ecddb52e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330121"
---
# <a name="pidtagresponsibility-canonical-property"></a>PidTagResponsibility (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält TRUE, wenn ein Transportanbieter bereits die Verantwortung für die Zusende der Nachricht an diesen Empfänger übernommen hat, und FALSE, wenn der MAPI-Spooler der Meinung ist, dass dieser Transportanbieter die Verantwortung übernehmen sollte.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RESPONSIBILITY  <br/> |
|Kennung:  <br/> |0x0E0F  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |MAPI nicht durchlässig  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn der MAPI-Spooler über [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)eine ausgehende Nachricht an einen Transportanbieter sendet, wird diese Eigenschaft für alle Empfänger, für die der MAPI-Spooler diesen Transportanbieter als verantwortlich erachtet, auf FALSE und auf TRUE für alle anderen Empfänger gesetzt. Der Transportanbieter sollte versuchen, alle Empfänger mit PR_RESPONSIBILITY **FALSE** zu behandeln. Nachdem der Transportanbieter erfolgreich an einen Empfänger gesendet hat oder dies nicht erfolgreich war, sollte er diese Eigenschaft in der Quellnachricht auf TRUE festlegen, um anzugeben, dass er die Verantwortung für diesen Empfänger übernommen hat. 
  
Wenn ein Transportanbieter nach der Prüfung eines Empfängers entscheidet, dass er ihn nicht verarbeiten kann oder nicht, sollte der Transportanbieter PR_RESPONSIBILITY **FALSE** festlegen. Der MAPI-Spooler sucht dann nach einem anderen Transportanbieter, der diesen Empfänger verarbeiten kann. Der MAPI-Spooler erstellt schließlich einen Nichtverdienstbericht für alle Empfänger, für die kein Transportanbieter die Verantwortung übernimmt. 
  
Wenn der Transportanbieter versucht, die Nachricht zu senden, sollte er die [IMAPISupport::StatusRecips-Methode](imapisupport-statusrecips.md) aufrufen, um MAPI die Gründe für den Fehler anzugeben, damit MAPI einen Nicht-Lieferbericht generieren kann. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagDeleteAfterSubmit-Eigenschaft](pidtagdeleteaftersubmit-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

