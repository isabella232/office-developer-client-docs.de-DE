---
title: PidLidTaskFFixOffline (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTaskFFixOffline
api_type:
- COM
ms.assetid: bbaf7df4-2de0-4da3-9125-eb24dfa94cd8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 44852bbdbbd3d742e8cc81082765fe4320b81c46
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595462"
---
# <a name="pidlidtaskffixoffline-canonical-property"></a>PidLidTaskFFixOffline (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Genauigkeit der **Eigenschaft dispidTaskOwner** ([PidLidTaskOwner](pidlidtaskowner-canonical-property.md)) an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidTaskFFixOffline  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x0000812C  <br/> |
|Datentyp:  <br/> |PT_BOOLEAN  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn die **dispidTaskFFixOffline-Eigenschaft** auf FALSE festgelegt oder nicht festgelegt ist, ist der Wert für die **dispidTaskOwner-Eigenschaft** richtig. Wenn **dispidTaskFFixOffline** auf TRUE festgelegt ist, kann der Client keinen genauen Wert für **dispidTaskOwner** ermitteln. In diesem Fall kann der Client **dispidTaskOwner** auf einen generischen Besitzernamen festlegen, z. B. "Unknown". Wenn ein Client jedoch auf einen **dispidTaskFFixOffline-Wert** von TRUE trifft und einen genauen Besitzernamen ermitteln kann, sollte der Client **dispidTaskOwner** aktualisieren und **dispidTaskFFixOffline** auf FALSE festlegen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Definiert mehrere Objekte, die das elektronische Äquivalent von Aufgaben, Aufgabenzuweisungen und Aufgabenaktualisierungen modellieren. 
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

