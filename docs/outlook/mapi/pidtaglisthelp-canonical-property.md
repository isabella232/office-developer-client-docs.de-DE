---
title: Kanonische Pidtaglisthelp (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListHelp
api_type:
- HeaderDef
ms.assetid: 403324b8-c992-4823-aa0f-0414b283debc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 588747205ee3922fef7b107dc024f074a6ee527e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279629"
---
# <a name="pidtaglisthelp-canonical-property"></a>Kanonische Pidtaglisthelp (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Wert des Listen Hilfe-Headerfelds für MIME-Nachrichten (Multipurpose Internet Mail Extensions).
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W  <br/> |
|Kennung:  <br/> |0x1043  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Sonstiges  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Um ein Listen Hilfe-Kopfzeilenfeld zu generieren, müssen Clients den Wert von **PR_LIST_HELP** oder eine zugeordnete Eigenschaft auf den gewünschten Wert festlegen. MIME-Writer müssen diesen Wert in das Kopfzeilenfeld List-Help kopieren. 
  
Um den Wert dieser Listenserver bezogenen Eigenschaften festzulegen, müssen MIME-Clients die Kopfzeilenfelder wie in der folgenden Tabelle angegeben schreiben:
  
|**Eigenschaft**|**Bevorzugter Kopfzeilen Feldname**|**Name des alternativen Kopfzeilenfelds**|
|:-----|:-----|:-----|
|**PR_LIST_HELP** <br/> |List-Hilfe  <br/> |X-List-Hilfe  <br/> |
   
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internet Standard-e-Mail-Konventionen in Nachrichtenobjekte.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

