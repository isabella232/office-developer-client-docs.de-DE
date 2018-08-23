---
title: PidTagSendInternetEncoding (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSendInternetEncoding
api_type:
- COM
ms.assetid: ae408b4f-dee3-484b-a19c-f472cfa95996
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 33b9931a269eb4b5ee0429287d60fa1962b0e4f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584233"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a>PidTagSendInternetEncoding (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske der Voreinstellungen-Codierung. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SEND_INTERNET_ENCODING  <br/> |
|Kennung:  <br/> |0x3A71  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Adresse  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Legen Sie diese Eigenschaft an, dass die Codierungsoptionen verwendet. 
  
Diese Eigenschaft enthält die folgenden Kennzeichen:
  
BODY_ENCODING_HTML 
  
> Codieren Sie den Nachrichtentext im HTML-Format. Dieses Kennzeichen werden ignoriert, es sei denn, das Flag ENCODING_MIME festgelegt ist. 
    
BODY_ENCODING_TEXT_AND_HTML 
  
> Codieren Sie den Nachrichtentext mit Text und HTML als mehrteiligen alternativen Multipurpose Internet Mail Extensions (MIME). Dieses Kennzeichen werden ignoriert, es sei denn, das Flag ENCODING_MIME festgelegt ist. 
    
ENCODING_MIME 
  
> Codieren Sie die Nachricht mithilfe von MIME. Wenn dieses Flag nicht festgelegt ist, werden MAPI den Nachrichtentext in nur-Text und die Anlagen in UUENCODE codiert. 
    
ENCODING_PREFERENCE 
  
> Verwenden Sie die anderen Flags in dieser Bitmaske, um die Codierung zu bestimmen. Wenn dieses Flag nicht festgelegt ist, bleibt MAPI an die messaging-System Codierung Entscheidungen treffen. 
    
MAC_ATTACH_ENCODING_APPLEDOUBLE 
  
> Codieren von Anlagen in doppelte Modus Apple Macintosh. Dieses Kennzeichen werden ignoriert, es sei denn, das Flag ENCODING_MIME festgelegt ist. 
    
MAC_ATTACH_ENCODING_APPLESINGLE 
  
> Codieren von Anlagen in einzelnen Modus Apple Macintosh. Dieses Kennzeichen werden ignoriert, es sei denn, das Flag ENCODING_MIME festgelegt ist. 
    
MAC_ATTACH_ENCODING_UUENCODE 
  
> Codieren Sie Macintosh-Anlagen in UUENCODE. Wenn das Flag ENCODING_MIME festgelegt ist, dieses Flag wird ignoriert, und wird stattdessen BinHex-Codierung verwendet. 
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.
    
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

