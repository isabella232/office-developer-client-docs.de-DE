---
title: Kanonische PidLidSharingFlavor-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidSharingFlavor
api_type:
- COM
ms.assetid: c91ab5c7-82ac-4895-bf54-2863ca5e2410
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: df5cb7fe6a45b87d7a382c6d6a928711c0f90f62
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600526"
---
# <a name="pidlidsharingflavor-canonical-property"></a>Kanonische PidLidSharingFlavor-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wird als Eigenschaft einer Freigabenachricht festgelegt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidSharingFlavor  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Sharing  <br/> |
|Long ID (LID):  <br/> |0x00008A18  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Freigabe  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Wert dieser Eigenschaft muss einer der folgenden Werte sein:
  
|**Wert**|**Typ des Sharing Message-Objekts**|
|:-----|:-----|
|0x00020310  <br/> |Eine Freigabe-Einladung für einen speziellen Ordner.  <br/> |
|0x00000310  <br/> |Eine Freigabe-Einladung für einen Ordner, der kein spezieller Ordner ist.  <br/> |
|0x00020500  <br/> |Eine Freigabeanforderung.  <br/> |
|0x00020710  <br/> |Sowohl eine Freigabe-Einladung für einen speziellen Ordner als auch eine Freigabeanforderung für den entsprechenden speziellen Ordner des Empfängers.  <br/> |
|0x00025100  <br/> |Eine Freigabeantwort, die eine Anforderung verweigert.  <br/> |
|0x00023310  <br/> |Eine Freigabeantwort, die eine Anforderung akzeptiert (auch eine Art von Freigabe-Einladung).  <br/> |
   
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

