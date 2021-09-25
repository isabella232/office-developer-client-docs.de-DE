---
title: Kanonische PidLidFileUnderId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidFileUnderId
api_type:
- COM
ms.assetid: 917431a9-fd90-4b4d-b042-886e3dbf47c0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 216f927629349b482da874adb07a470b45dd1242
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575106"
---
# <a name="pidlidfileunderid-canonical-property"></a>Kanonische PidLidFileUnderId-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, wie der Wert der **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) -Eigenschaft generiert und neu kompiliert wird, wenn sich andere Kontaktnameneigenschaften ändern.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidFileUnderId  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x00008006  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn diese Eigenschaft fehlt oder auf einen Wert festgelegt ist, der in der folgenden Tabelle oder in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)nicht detailliert angegeben ist, kann die Anwendung eine eigene Logik auswählen, um den Wert von **dispidFileUnder** neu zu komputieren, wenn sich andere Kontaktnameneigenschaften ändern. 
  
In der folgenden Tabelle wird die Notation <PropertyName> verwendet, um "den Wert von PropertyName" anzugeben. Wenn beispielsweise der Wert der **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) -Eigenschaft "Smith" ist und der Wert der **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) -Eigenschaft "Ben" ist, <PidTagGivenName> <PidTagSurname> gibt " " die Zeichenfolge "Ben Smith". In der Tabelle gibt "\r" ein Wagenrücklaufzeichen, "\n" ein Zeilenvorschubzeichen und <space> ein Leerzeichen an.
  
|**Wert der **dispidFileUnderId-Eigenschaft****|**Beschreibung der **dispidFileUnder-Eigenschaft****|
|:-----|:-----|
|0x00000000  <br/> |Leere PT_UNICODE.  <br/> |
|0x00003001  <br/> |"\<PidTagDisplayName\>"  <br/> |
|0x00003A06  <br/> |"\<PidTagGivenName\>"  <br/> |
|0x00003A11  <br/> |"\<PidTagSurname\>"  <br/> |
|0x00003A16  <br/> |"\<PidTagCompanyName\>"  <br/> |
|0x00008017  <br/> |"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"  <br/> |
|0x00008018  <br/> |" \<PidTagCompanyName\>\r\n\<PidTagSurname\> , \<space\> \<PidTagGivenName\> \<space\> \<PidTagMiddleName\> "  <br/> |
|0x00008019  <br/> |" \<PidTagSurname\> , \<space\> \<PidTagGivenName\> \<space\> \<PidTagMiddleName\>\r\n\<PidTagCompanyName\> "  <br/> |
|0x00008030  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"  <br/> |
|0x00008031  <br/> |"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"  <br/> |
|0x00008032  <br/> |" \<PidTagCompanyName\>\r\n\<PidTagSurname\> \<PidTagGivenName\> \<space\> \<PidTagMiddleName\> "  <br/> |
|0x00008033  <br/> |" \<PidTagCompanyName\>\r\n\<PidTagSurname\> \<space\> \<PidTagGivenName\> \<space\> \<PidTagMiddleName\> "  <br/> |
|0x00008034  <br/> |" \<PidTagSurname\> \<PidTagGivenName\> \<space\> \<PidTagMiddleName\>\r\n\<PidTagCompanyName\> "  <br/> |
|0x00008035  <br/> |" \<PidTagSurname\> \<space\> \<PidTagGivenName\> \<space\> \<PidTagMiddleName\>\r\n\<PidTagCompanyName\> "  <br/> |
|0x00008036  <br/> |"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"  <br/> |
|0x00008037  <br/> |"\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagSurname\>\<space\>\<PidTagGeneration\>"  <br/> |
|0x00008038  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"  <br/> |
|0xfffffffd  <br/> |Gibt an, dass die Anwendung beim Anzeigen des Kontakts versuchen soll, den aktuellen Wert von **dispidFileUnder** und anderen Kontakteigenschaften zu verwenden, um eine "beste Übereinstimmung" für **dispidFileUnderId** mit einem der vorherigen Werte in dieser Tabelle zu finden.  <br/> |
|0xfffffffe  <br/> |Gibt an, dass die Anwendung beim Anzeigen des Kontakts die entsprechenden Standardwerte (gemäß dem Gebietsschema der Sprache) für **dispidFileUnderId** auswählen und **dispidFileUnder** entsprechend der Auswahl aktualisieren soll.  <br/> |
|0xffffffff  <br/> |**dispidFileUnder** ist eine vom Benutzer bereitgestellte PT_UNICODE und sollte nicht geändert werden, wenn sich eine andere Kontaktnameneigenschaft ändert.  <br/> |
   
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

