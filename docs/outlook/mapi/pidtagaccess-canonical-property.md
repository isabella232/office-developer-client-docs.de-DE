---
title: PidTagAccess (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 8c8a882e-62c1-4c57-8c63-ee5849f656b0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b453a7b0cfa04dd94da01089573427a931fb4d4f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398339"
---
# <a name="pidtagaccess-canonical-property"></a>PidTagAccess (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske aus Flags, die angibt, die Vorgänge, die an den Client für das Objekt verfügbar sind.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ACCESS  <br/> |
|Kennung:  <br/> |0x0FF4  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Access-Steuerelementeigenschaften  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist schreibgeschützt für den Client. Es muss ein bitweises **oder** von NULL oder mehrere Werte aus der folgenden Tabelle. 
  
|**Name**|**Wert**|**Beschreibung**|
|:-----|:-----|:-----|
|MAPI_ACCESS_MODIFY  <br/> |0x00000001  <br/> |Schreiben  <br/> |
|MAPI_ACCESS_READ  <br/> |0x00000002  <br/> |Lesen  <br/> |
|MAPI_ACCESS_DELETE  <br/> |0 x 00000004  <br/> |Löschen  <br/> |
|MAPI_ACCESS_CREATE_HIERARCHY  <br/> |0 x 00000008  <br/> |Erstellen von Unterordnern im Ordner-Hierarchie  <br/> |
|MAPI_ACCESS_CREATE_CONTENTS  <br/> |0 x 00000010  <br/> |Erstellen von Nachrichten  <br/> |
|MAPI_ACCESS_CREATE_ASSOCIATED  <br/> |0 x 00000020  <br/> |Erstellen der zugeordnete von Nachrichten  <br/> |
   
Die Flags MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY und MAPI_ACCESS_READ werden für Ordner und Message-Objekten und in der Spalte **PR_ACCESS** in Inhalt und Inhalt der zugeordneten Tabellen gefunden. Die Flags MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS und MAPI_ACCESS_CREATE_HIERARCHY befinden sich auf nur Folder-Objekten. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
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

