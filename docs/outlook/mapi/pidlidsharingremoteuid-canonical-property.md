---
title: PidLidSharingRemoteUid (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteUid
api_type:
- COM
ms.assetid: cfe3b728-317b-4871-adea-e2fdf8441da7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c3e783934367ad7c5c1a9a760aa8a24525901832
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331262"
---
# <a name="pidlidsharingremoteuid-canonical-property"></a>PidLidSharingRemoteUid (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Eintrags-ID des freigegebenen Remoteordners an. Dies ist eine Eigenschaft einer Freigabenachricht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidSharingRemoteUid  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Sharing  <br/> |
|Lange ID (LID):  <br/> |0x00008A06  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Freigabe  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft muss auf die Hexadezimalzeichenfolgendarstellung des Werts der PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft für den freigegebenen Ordner festgelegt werden. Dies ist eine Eigenschaft einer Freigabenachricht.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Gibt Postfachordner zwischen Clients zurück.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

