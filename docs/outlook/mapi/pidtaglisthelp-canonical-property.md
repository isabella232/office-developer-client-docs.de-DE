---
title: Kanonische PidTagListHelp-Eigenschaft
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
ms.openlocfilehash: 7a9a5d090babce8105fab43bf8401448373777cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794580"
---
# <a name="pidtaglisthelp-canonical-property"></a>Kanonische PidTagListHelp-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält den Wert der Liste-Hilfe-Header ein Feld einer Nachricht Multipurpose Internet Mail Extensions (MIME).
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W  <br/> |
|Bezeichner:  <br/> |0x1043  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Verschiedenes  <br/> |
   
## <a name="remarks"></a>Hinweise

Um eine Liste Hilfe Kopfzeilenfeld generiert werden soll, müssen die Clients den Wert **PR_LIST_HELP** oder eine zugeordnete Eigenschaft auf den gewünschten Wert festgelegt. MIME-Autoren müssen diesen Wert in der Liste Hilfe Kopfzeilenfeld kopieren. 
  
Wenn den Wert dieser Liste Server-bezogene Eigenschaften festlegen möchten, müssen MIME-Clients die Kopfzeile Felder wie in der folgenden Tabelle angegebenen schreiben:
  
|**Eigenschaft**|**Bevorzugte Header-Feldname**|**Alternative Header-Feldname**|
|:-----|:-----|:-----|
|**PR_LIST_HELP** <br/> |Liste-Hilfe  <br/> |X-Liste-Hilfe  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

