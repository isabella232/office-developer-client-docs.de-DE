---
title: Kanonische pidlidaddressbookproviderarraytype (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderArrayType
api_type:
- COM
ms.assetid: ca4eb6c2-98e9-4dbc-9f5a-f0f257456ead
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 68396f210aab465da9cec4a74a3c24cc4e8578a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348440"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a>Kanonische pidlidaddressbookproviderarraytype (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Status der elektronischen Adressen des Kontakts an und stellt eine Gruppe von Bitflags dar.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidABPArrayType  <br/> |
|Eigenschaftengruppe:  <br/> |PSETID_Address  <br/> |
|Lange ID (LID):  <br/> |0x00008029  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Wert der **dispidABPArrayType** -Eigenschaft muss eine Kombination von Flags sein, die den Status des Contact-Objekts angeben. In der folgenden Tabelle werden einzelne Flags angegeben. Wenn diese Eigenschaft festgelegt ist, muss auch die **dispidABPEmailList** ([pidlidaddressbookprovideremaillist (](pidlidaddressbookprovideremaillist-canonical-property.md))-Eigenschaft festgelegt werden. Diese beiden Eigenschaften müssen miteinander synchronisiert bleiben. Wenn **dispidABPArrayType** beispielsweise das Bit "0x00000001 festgelegt" hat, muss einer der Werte von **dispidABPEmailList** "0x00000000" lauten. 
  
|**Bit**|**Beschreibung**|
|:-----|:-----|
|0x00000001  <br/> |Mail1 ist für den Kontakt definiert.  <br/> |
|0x00000002  <br/> |Mail2 ist für den Kontakt definiert.  <br/> |
|0x00000004  <br/> |Email3 ist für den Kontakt definiert.  <br/> |
|0x00000008  <br/> |Business Fax ist für den Kontakt definiert.  <br/> |
|0x00000010  <br/> |Home Fax ist für den Kontakt definiert.  <br/> |
|0x00000020  <br/> |Primäres Fax ist für den Kontakt definiert.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftenmengen Definitionen und Verweise auf zugehörige Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Definitionen von Datentypen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

