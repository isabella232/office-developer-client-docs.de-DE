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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383611"
---
# <a name="pidlidsharingflavor-canonical-property"></a>PidLidSharingFlavor (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt fest, wie eine eine Freigabenachricht-Eigenschaft.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidSharingFlavor  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Sharing  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008A18  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Freigabe  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Wert dieser Eigenschaft muss eine der folgenden sein:
  
|**Wert**|**Art der Freigabe Message-Objekt**|
|:-----|:-----|
|0x00020310  <br/> |Eine freigabeeinladung für einen Ordner mit Sonderfunktion.  <br/> |
|0x00000310  <br/> |Eine freigabeeinladung für einen Ordner, der nicht auf einen Ordner mit Sonderfunktion ist.  <br/> |
|0x00020500  <br/> |Eine Freigabeanfrage.  <br/> |
|0x00020710  <br/> |Sowohl eine freigabeeinladung für einen Ordner mit Sonderfunktion und eine Freigabeanfrage für entsprechende Spezialordner des Empfängers.  <br/> |
|0x00025100  <br/> |Eine Freigabeantwort eine Anforderung zu verweigern.  <br/> |
|0x00023310  <br/> |Eine Freigabeantwort akzeptieren einer Anforderung (auch eine Art der Einladung zur Freigabe).  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Teilt Postfachordner zwischen Clients.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

