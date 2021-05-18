---
title: PidLidSharingFlavor (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingFlavor
api_type:
- COM
ms.assetid: c91ab5c7-82ac-4895-bf54-2863ca5e2410
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 21144af15e7a36f54af3032f735c391b3038305b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327482"
---
# <a name="pidlidsharingflavor-canonical-property"></a>PidLidSharingFlavor (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wird als Eigenschaft einer Freigabenachricht bestimmt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidSharingFlavor  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Sharing  <br/> |
|Lange ID (LID):  <br/> |0x00008A18  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Freigabe  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Wert dieser Eigenschaft muss einer der folgenden Sein:
  
|**Wert**|**Typ des Sharing Message-Objekts**|
|:-----|:-----|
|0x00020310  <br/> |Eine Freigabeeinladung für einen speziellen Ordner.  <br/> |
|0x00000310  <br/> |Eine Freigabeeinladung für einen Ordner, der kein spezieller Ordner ist.  <br/> |
|0x00020500  <br/> |Eine Freigabeanforderung.  <br/> |
|0x00020710  <br/> |Sowohl eine Freigabeeinladung für einen speziellen Ordner als auch eine Freigabeanforderung für den entsprechenden speziellen Ordner des Empfängers.  <br/> |
|0x00025100  <br/> |Eine Freigabeantwort, die eine Anforderung verweigert.  <br/> |
|0x00023310  <br/> |Eine Freigabeantwort, die eine Anforderung akzeptiert (auch eine Art von Freigabeeinladung).  <br/> |
   
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

