---
title: PidTagViewDescriptorName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagViewDescriptorName
api_type:
- COM
ms.assetid: 1e689ee4-9e89-4328-beb9-05c80a6544a0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ab906d83ae4ad46747fd9037728620db1d656d25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360725"
---
# <a name="pidtagviewdescriptorname-canonical-property"></a>PidTagViewDescriptorName (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Namen eines Ansichtsdeskriptors.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_VD_NAME, PR_VD_NAME_A, PR_VD_NAME_W  <br/> |
|Kennung:  <br/> |0x7006  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Durch nachrichtenklassendefinierte übertragungsfähige Nachrichten  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaften müssen auf eine nicht leere Zeichenfolge für eine Folder Associate Information (FAI)-Nachricht festgelegt werden, die Ansichtsdefinitionen enthält.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Gibt den Speicherort und die Eigenschaften von Client- und Serverkonfigurationsdaten an, z. B. freigegebene Kategorielisten und Arbeitszeiten.
    
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

