---
title: PidTagAddressBookHierarchicalRootDepartment
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAddressBookHierarchicalRootDepartment
api_type:
- HeaderDef
ms.assetid: c611640b-1a70-4a76-b7ff-c8ad8d320892
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 81205bd9e65708f11a562ec777b592ec1b15f2a4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629879"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a>PidTagAddressBookHierarchicalRootDepartment

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 Enthält den Distinguished Name (DN) des hierarchischen Adressstamms (HIERARCHISCHE). 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A  <br/> |
|Eigenschaftensatz:  <br/> |Adressbuch  <br/> |
|Long ID (LID):  <br/> |0x8C98  <br/> |
|Datentyp:  <br/> |PT_STRING8  <br/> |
|Bereich:  <br/> |Exchange-Adressbuch  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dies ist eine Eigenschaft im Globalen Adresslistencontainer (GAL) und stellt den Distinguished Name des hierarchischen Adressstamms dar. Diese Eigenschaft ist nur im Offlineadressbuch und nie in Active Directory Domain Services (AD DS) vorhanden. Aufrufer sollten MAPI_CACHE_ONLY an den GetProps-Aufruf übergeben, um einen Remoteprozeduraufruf zu vermeiden. Wenn dies nicht vorhanden ist, sollten Anrufer PR_EMS_AB_HAB_ROOT_DEPARTMENT verwenden, die vom Typ PT_OBJECT ist, um die Stammabteilung zu suchen. 
  
Sobald die Stammabteilung abgerufen wurde, kann sie über einen Objekttyp MAPI_MAILUSER oder MAPI_DISTLIST verfügen. Wenn der Objekttyp MAPI_DISTLIST ist, wird das neue Schema verwendet. Wenn der Objekttyp MAPI_MAILUSER ist, wird das vorherige Schema verwendet. 
  
- Microsoft Office Outlook 2007 Service Pack 2 unterstützt beide Schemas. 
    
- Microsoft Outlook 2010 und Microsoft Outlook 2013 unterstützen das neue Schema.
    
Im neuen Schema sind alle Abteilungsgruppen auch Verteilerlisten und vom Typ MAPI_DISTLIST. Mitglieder von Abteilungsgruppen und Abteilungen innerhalb von Abteilungsgruppen werden mithilfe von PR_EMS_AB_MEMBER abgerufen, genau wie Mitglieder der Verteilerliste.
  
Sobald die Stammabteilung abgerufen wurde, kann sie über einen Objekttyp MAPI_MAILUSER oder MAPI_DISTLIST verfügen. Wenn der Objekttyp MAPI_DISTLIST ist, wird das neue Schema verwendet. Wenn der Objekttyp MAPI_MAILUSER ist, wird das alte Schema verwendet. 
  
Im neuen Schema sind alle Abteilungsgruppen auch DLs und vom Typ MAPI_DISTLIST.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Microsoft Exchange Server Protokollspezifikationen bereit.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

