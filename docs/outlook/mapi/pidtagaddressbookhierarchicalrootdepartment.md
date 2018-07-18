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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 49c9b0a80f9bc3b45dfafa6f4e037fe55af289d5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794106"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a>PidTagAddressBookHierarchicalRootDepartment

  
  
**Betrifft**: Outlook 
  
 Enthält den distinguished Name (DN) des Stammverzeichnisses hierarchische Adresse (eines hierarchischen Adressbuchs). 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_EMS_AB_HAB_ROOT_DEPARTMENT PR_EMS_AB_HAB_ROOT_DEPARTMENT_A  <br/> |
|-Eigenschaft festgelegt:  <br/> |Adressbuch  <br/> |
|Long-ID (Abdeckung):  <br/> |0x8C98  <br/> |
|Datentyp:  <br/> |PT_STRING8  <br/> |
|Bereich:  <br/> |Exchange-Adressbuch  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dies ist eine Eigenschaft für den Container der globalen Adressliste (GAL) Liste und den distinguished Name des Stammverzeichnisses hierarchische Adresse darstellt. Diese Eigenschaft ist nur in das Offlineadressbuch und nie in Active Directory-Domänendienste (AD DS) vorhanden. Anrufer sollten den GetProps Anruf an ein remote Procedure Call vermeiden MAPI_CACHE_ONLY übergeben. Wenn dies nicht vorhanden ist, sollte Anrufer PR_EMS_AB_HAB_ROOT_DEPARTMENT, die vom Typ PT_OBJECT ist, verwenden, um die Stamm-Abteilung suchen. 
  
Nachdem Sie die Stamm-Abteilung erhalten haben, können sie einen Objekttyp MAPI_MAILUSER oder MAPI_DISTLIST haben. Wenn der Objekttyp MAPI_DISTLIST ist, wird das neue Schema eingesetzt wird. Wenn der Objekttyp MAPI_MAILUSER ist, wird das vorherige Schema eingesetzt. 
  
- Microsoft Office Outlook 2007 Service Pack 2 unterstützt sowohl Schemas. 
    
- Microsoft Outlook 2010 und Microsoft Outlook 2013 unterstützen das neue Schema.
    
In der neuen Schema alle Gruppen auf Abteilungsebene sind auch Verteilerlisten und vom Typ MAPI_DISTLIST. Mitglieder von Gruppen auf Abteilungsebene und Abteilungen in Gruppen auf Abteilungsebene werden mit PR_EMS_AB_MEMBER, genau wie Mitglieder der Verteilerliste abgerufen.
  
Nachdem Sie die Stamm-Abteilung erhalten haben, können sie einen Objekttyp MAPI_MAILUSER oder MAPI_DISTLIST haben. Wenn der Objekttyp MAPI_DISTLIST ist, wird das neue Schema verwendet. Wenn der Objekttyp MAPI_MAILUSER ist, wird das alte Schema verwendet. 
  
In der neuen Schema alle Gruppen auf Abteilungsebene sind auch Verteilerlisten und vom Typ MAPI_DISTLIST.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Spezifikationen von Microsoft Exchange Server-Protokoll.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

