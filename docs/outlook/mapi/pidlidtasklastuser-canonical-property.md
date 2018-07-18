---
title: PidLidTaskLastUser (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastUser
api_type:
- COM
ms.assetid: 914c55e9-cb36-46a4-b5ee-382413fa25f9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6dc2bcf2003ee16fa4a6c66689b6af79653e2d04
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793842"
---
# <a name="pidlidtasklastuser-canonical-property"></a>PidLidTaskLastUser (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Gibt den Namen des aktuelle Benutzers, der Besitzer der Aufgabe wurde.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidTaskLastUser  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Task  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008122  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Bevor ein Client eine Aufgabenanfrage sendet, wird diese Eigenschaft auf den Namen der Aufgabe delegierende Person. Bevor ein Client eine Aufgabe Annahme sendet, wird diese Eigenschaft auf den Namen der Beauftragte für die Aufgabe. Bevor ein Client eine Aufgabe Ablehnung sendet, wird diese Eigenschaft auf den Namen der Aufgabe delegierende Person.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

