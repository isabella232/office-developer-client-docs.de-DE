---
title: PidTagAddressBookHierarchicalRootDepartment
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAddressBookHierarchicalRootDepartment
api_type:
- HeaderDef
ms.assetid: c611640b-1a70-4a76-b7ff-c8ad8d320892
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 22a1a62f4ee6ff492f36eb18e2d92c8d70febd72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326124"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a>PidTagAddressBookHierarchicalRootDepartment

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 Enthält den Distinguished Name (DN) des hierarchischen Adressstamms (HAB). 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A  <br/> |
|Eigenschaftensatz:  <br/> |Adressbuch  <br/> |
|Lange ID (LID):  <br/> |0x8C98  <br/> |
|Datentyp:  <br/> |PT_STRING8  <br/> |
|Bereich:  <br/> |Exchange-Adressbuch  <br/> |
   
## <a name="remarks"></a>Hinweise

Dies ist eine Eigenschaft im Globalen Adresslistencontainer (GAL) und stellt den Distinguished Name des hierarchischen Adressstamms dar. Diese Eigenschaft ist nur im Offlineadressbuch und niemals in Active Directory Domain Services (AD DS) vorhanden. Anrufer sollten MAPI_CACHE_ONLY an den GetProps-Aufruf übergeben, um einen Remoteprozeduraufruf zu vermeiden. Wenn dies nicht der Fall ist, sollten Anrufer die PR_EMS_AB_HAB_ROOT_DEPARTMENT, die vom Typ PT_OBJECT ist, verwenden, um die Stammabteilung zu finden. 
  
Sobald die Stammabteilung erhalten wurde, kann sie einen Objekttyp MAPI_MAILUSER oder MAPI_DISTLIST. Wenn der Objekttyp MAPI_DISTLIST wird das neue Schema verwendet. Wenn der Objekttyp MAPI_MAILUSER, wird das vorherige Schema verwendet. 
  
- Microsoft Office Outlook 2007 Service Pack 2 unterstützt beide Schemas. 
    
- Microsoft Outlook 2010 und Microsoft Outlook 2013 unterstützen das neue Schema.
    
Im neuen Schema sind alle Abteilungsgruppen auch Verteilerlisten und vom Typ MAPI_DISTLIST. Mitglieder von Abteilungsgruppen und Abteilungen innerhalb von Abteilungsgruppen werden mithilfe von PR_EMS_AB_MEMBER, genau wie Verteilerlistenmitglieder.
  
Sobald die Stammabteilung erhalten wurde, kann sie einen Objekttyp MAPI_MAILUSER oder MAPI_DISTLIST. Wenn der Objekttyp MAPI_DISTLIST wird das neue Schema verwendet. Wenn der Objekttyp MAPI_MAILUSER wird das alte Schema verwendet. 
  
Im neuen Schema sind alle Abteilungsgruppen auch DLs und vom Typ MAPI_DISTLIST.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Microsoft Exchange Server zur Verfügung.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

