---
title: PidTagTemplateid (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTemplateid
api_type:
- COM
ms.assetid: 1a418c76-ebc7-47f2-ac91-797162e6e099
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7672c18f18d39ed1e4e8b4664ba7990563419a20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795253"
---
# <a name="pidtagtemplateid-canonical-property"></a>PidTagTemplateid (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), ausgedrückt als Format permanente Eintrags-ID an.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_TEMPLATEID  <br/> |
|Bezeichner:  <br/> |0x3902  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Adressbuch  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieser Wert muss für alle Address Book-Objekte auf einem Server (NSPI = Name Service Provider Interface) vorhanden sein, den distinguished Name (DN) gleich dem Wert für **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) und der DN muss das DN-Format folgen die Spezifikation für den Typ des Objekts. 
  
Diese Eigenschaft ist nicht für Objekte, die in einem offline-Adressbuch vorhanden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

