---
title: Kanonische PidLidSharingProviderUrl-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidSharingProviderUrl
api_type:
- COM
ms.assetid: d217ab33-d697-4d27-a962-08d551d301f0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3d00fd8d13311e1a390056a9cef5a915086eb972
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630178"
---
# <a name="pidlidsharingproviderurl-canonical-property"></a>Kanonische PidLidSharingProviderUrl-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die URL an, die sich auf den Freigabeanbieter bezieht und durch die **Eigenschaft dispidSharingProviderGuid** ([PidLidSharingProviderGuid](pidlidsharingproviderguid-canonical-property.md)) identifiziert wird. Dies ist eine Eigenschaft einer Freigabenachricht.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidSharingProviderUrl  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Sharing  <br/> |
|Long ID (LID):  <br/> |0x00008A03  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Freigabe  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird in der Regel verwendet, um weitere Informationen über den Freigabeanbieter bereitzustellen, sollte jedoch ignoriert werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Teilt Postfachordner zwischen Clients.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

