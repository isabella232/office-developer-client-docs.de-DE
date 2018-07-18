---
title: PidLidTaskFFixOffline (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskFFixOffline
api_type:
- COM
ms.assetid: bbaf7df4-2de0-4da3-9125-eb24dfa94cd8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b8da927fe0080a83748bbb2941979dcb246222fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793839"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a>PidLidTaskFFixOffline (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Gibt die Genauigkeit der **DispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md))-Eigenschaft an.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidTaskFFixOffline  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Task  <br/> |
|Long-ID (Abdeckung):  <br/> |0x0000812C  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn die **DispidTaskFFixOffline** -Eigenschaft auf FALSE festgelegt ist oder nicht festgelegt ist, ist der Wert der Eigenschaft **DispidTaskOwner** korrekt. Wenn **DispidTaskFFixOffline** auf TRUE festgelegt ist, kann der Client einen genauen Wert für **DispidTaskOwner**nicht ermitteln. In diesem Fall kann der Client **DispidTaskOwner** auf einen generischen Besitzername, beispielsweise "Unknown" festgelegt. Wenn ein Client einen **DispidTaskFFixOffline** Wert "true trifft" und den Namen eines Besitzers genau bestimmen kann, sollte der Client jedoch **DispidTaskOwner** aktualisieren und **DispidTaskFFixOffline** auf FALSE festgelegt. 
  
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

