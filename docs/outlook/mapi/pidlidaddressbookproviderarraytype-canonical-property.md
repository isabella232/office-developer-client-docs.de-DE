---
title: Kanonische PidLidAddressBookProviderArrayType-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAddressBookProviderArrayType
api_type:
- COM
ms.assetid: ca4eb6c2-98e9-4dbc-9f5a-f0f257456ead
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bcbfe2a09d91f1f6c43ec6ddf1dfdec6592994dd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583992"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a>Kanonische PidLidAddressBookProviderArrayType-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Status der elektronischen Adressen des Kontakts an und stellt eine Reihe von Bit-Flags dar.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidABPArrayType  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x00008029  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Wert der **dispidABPArrayType-Eigenschaft** muss eine Kombination aus Flags sein, die den Status des Kontaktobjekts angeben. Einzelne Flags werden in der folgenden Tabelle angegeben. Wenn diese Eigenschaft festgelegt ist, muss auch die Eigenschaft **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) festgelegt werden. Diese beiden Eigenschaften müssen miteinander synchronisiert werden. Wenn z. B. **dispidABPArrayType** das Bit "0x00000001 festgelegt" aufweist, muss einer der Werte von **dispidABPEmailList** "0x00000000" sein. 
  
|**Bit**|**Beschreibung**|
|:-----|:-----|
|0x00000001  <br/> |E-Mail1 ist für den Kontakt definiert.  <br/> |
|0x00000002  <br/> |E-Mail2 ist für den Kontakt definiert.  <br/> |
|0x00000004  <br/> |E-Mail3 ist für den Kontakt definiert.  <br/> |
|0x00000008  <br/> |Geschäftsfax ist für den Kontakt definiert.  <br/> |
|0x00000010  <br/> |Home fax is defined for the contact.  <br/> |
|0x00000020  <br/> |Primäres Fax ist für den Kontakt definiert.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

