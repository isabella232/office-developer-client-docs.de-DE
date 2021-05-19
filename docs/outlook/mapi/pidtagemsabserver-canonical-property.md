---
title: PidTagEmsAbServer (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEmsAbServer
api_type:
- HeaderDef
ms.assetid: de942619-2507-8fe0-bc81-f9da9ef7266f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fba49b052a51bd498f61fc115f630d08fc6c8926
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335798"
---
# <a name="pidtagemsabserver-canonical-property"></a>PidTagEmsAbServer (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt entweder den Pfad eines Adressbuchcontainers in einem Offlineszenario oder den vollqualifizierten Domänennamen des globalen Katalogservers an, auf dem sich der Adressbuchcontainer in einem Onlineszenario befindet.
  
## 

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W  <br/> |
|Kennung:  <br/> |0xFFFE  <br/> |
|Datentyp:  <br/> |PT_TSTRING  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft hat den  Eigenschaftstyp auf PT_UNICODE zurückgesetzt, wenn sie mit dem Symbol auf einer Unicode-Plattform kompiliert wird, und auf PT_STRING8, wenn sie nicht mit dem Symbol kompiliert `UNICODE`  `UNICODE` wird. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen zur Verfügung.
    
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

