---
title: PidLidAddressBookProviderArrayType (kanonische Eigenschaft)
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3515d0f751cb6d8d0d427079691456519bac97dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793332"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a>PidLidAddressBookProviderArrayType (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Gibt den Status des Kontakts elektronische Adressen und stellt einen Satz von Bit-Flags dar.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidABPArrayType  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Address  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008029  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert der **DispidABPArrayType** -Eigenschaft muss eine Kombination von Flags, die den Zustand des Kontaktobjekts angeben. Einzelne Flags werden in der folgenden Tabelle angegeben. Wenn diese Eigenschaft festgelegt ist, muss die Eigenschaft **DispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)), auch festgelegt werden. Diese beiden Eigenschaften müssen miteinander synchronisiert werden. Wenn **DispidABPArrayType** das Bit "0 x 00000001 Set" aufweist, muss einer der Werte der **DispidABPEmailList** "0 x 00000000" sein. 
  
|**Bit**|**Beschreibung**|
|:-----|:-----|
|0x00000001  <br/> |Email1 ist für den Kontakt definiert.  <br/> |
|0x00000002  <br/> |Email2 ist für den Kontakt definiert.  <br/> |
|0 x 00000004  <br/> |Email3 ist für den Kontakt definiert.  <br/> |
|0 x 00000008  <br/> |Fax (geschäftlich) ist für den Kontakt definiert.  <br/> |
|0 x 00000010  <br/> |Fax privat ist für den Kontakt definiert.  <br/> |
|0 x 00000020  <br/> |Primäre Faxnummer ist für den Kontakt definiert.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

