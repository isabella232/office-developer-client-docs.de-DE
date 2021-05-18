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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 226e59ef6aa88bc290cf5aeb4d620979f926e1eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303038"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a>PidLidTaskFFixOffline (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Genauigkeit der **eigenschaft dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)) an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidTaskFFixOffline  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Task  <br/> |
|Lange ID (LID):  <br/> |0x0000812C  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn die **dispidTaskFFixOffline-Eigenschaft** auf FALSE festgelegt oder nicht festgelegt ist, ist der Wert für die **dispidTaskOwner-Eigenschaft** richtig. Wenn **dispidTaskFFixOffline** auf TRUE festgelegt ist, kann der Client keinen genauen Wert für **dispidTaskOwner ermitteln.** In diesem Fall kann der Client **dispidTaskOwner** auf einen generischen Besitzernamen festlegen, z. B. "Unbekannt". Wenn ein Client jedoch auf den **dispidTaskFFixOffline-Wert** TRUE trifft und einen genauen Besitzernamen bestimmen kann, sollte der Client **dispidTaskOwner** aktualisieren und **dispidTaskFFixOffline** auf FALSE festlegen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Definiert mehrere Objekte, die das elektronische Äquivalent von Vorgängen, Vorgangszuordnungen und Vorgangsaktualisierungen modellieren. 
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

