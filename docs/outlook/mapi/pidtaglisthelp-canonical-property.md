---
title: PidTagListHelp (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 588747205ee3922fef7b107dc024f074a6ee527e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279629"
---
# <a name="pidtaglisthelp-canonical-property"></a>PidTagListHelp (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Wert einer MIME-Nachricht (Multipurpose Internet Mail Extensions) List-Help Kopfzeilenfeld.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W  <br/> |
|Kennung:  <br/> |0x1043  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Sonstiges  <br/> |
   
## <a name="remarks"></a>Hinweise

Um ein List-Help zu generieren, müssen Clients  den Wert einer PR_LIST_HELP oder einer zugeordneten Eigenschaft auf den gewünschten Wert festlegen. MIME-Writer müssen diesen Wert in das List-Help kopieren. 
  
Um den Wert dieser listenserverbezogenen Eigenschaften festlegen zu können, müssen MIME-Clients die Kopfzeilenfelder wie in der folgenden Tabelle angegeben schreiben:
  
|**Eigenschaft**|**Name des bevorzugten Kopfzeilenfelds**|**Alternativer Kopfzeilenfeldname**|
|:-----|:-----|:-----|
|**PR_LIST_HELP** <br/> |List-Help  <br/> |X-List-Help  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

