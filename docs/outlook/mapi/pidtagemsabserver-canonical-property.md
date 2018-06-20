---
title: Kanonische PidTagEmsAbServer-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 27e3a9687d66bd1cd3586a25a3ca5792523096c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794337"
---
# <a name="pidtagemsabserver-canonical-property"></a>Kanonische PidTagEmsAbServer-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Gibt entweder den Pfad einer Adressbuchcontainer in einem Szenario offline oder den vollqualifizierten Domänennamen des globalen Katalogservers Adressbuchcontainer sich in einem Szenario online befindet.
  
## 

|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W  <br/> |
|Bezeichner:  <br/> |0xFFFE  <br/> |
|Datentyp:  <br/> |PT_TSTRING  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft hat den Eigenschaftentyp auf **PT_UNICODE** zurückzusetzen, wenn die Kompilierung der `UNICODE` Symbol auf einer Unicode-Plattform und **PT_STRING8** bei der Kompilierung nicht mit der `UNICODE` Symbol. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen an.
    
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

