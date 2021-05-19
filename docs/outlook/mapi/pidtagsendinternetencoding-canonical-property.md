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
ms.openlocfilehash: e157fa640026d13362084b30ad73cdb66a0b35b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342672"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a>PidTagSendInternetEncoding (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske mit Codierungseinstellungen. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SEND_INTERNET_ENCODING  <br/> |
|Kennung:  <br/> |0x3A71  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Adresse  <br/> |
   
## <a name="remarks"></a>Hinweise

Legen Sie diese Eigenschaft so ein, dass die verwendeten Codierungsoptionen angegeben werden. 
  
Diese Eigenschaft enthält die folgenden Flags:
  
BODY_ENCODING_HTML 
  
> Codieren Sie den Nachrichtentext in HTML. Dieses Flag wird ignoriert, es sei denn, ENCODING_MIME festgelegt ist. 
    
BODY_ENCODING_TEXT_AND_HTML 
  
> Codieren Sie den Nachrichtentext mithilfe von Text und HTML als mehrteilige Multipartalternativen (Multipurpose Internet Mail Extensions, MIME). Dieses Flag wird ignoriert, es sei denn, ENCODING_MIME festgelegt ist. 
    
ENCODING_MIME 
  
> Codieren Sie die Nachricht mithilfe von MIME. Wenn dieses Flag nicht festgelegt ist, codiert MAPI den Nachrichtentext in Nur-Text und die Anlagen in UUENCODE. 
    
ENCODING_PREFERENCE 
  
> Verwenden Sie die anderen Flags in dieser Bitmaske, um die Codierung zu bestimmen. Wenn dieses Flag nicht festgelegt ist, überlässt MAPI es dem Messagingsystem, Codierungsentscheidungen zu treffen. 
    
MAC_ATTACH_ENCODING_APPLEDOUBLE 
  
> Codieren Sie Macintosh-Anlagen im Apple-Doppelmodus. Dieses Flag wird ignoriert, es sei denn, ENCODING_MIME festgelegt ist. 
    
MAC_ATTACH_ENCODING_APPLESINGLE 
  
> Codieren Sie Macintosh-Anlagen im Apple-Einzelmodus. Dieses Flag wird ignoriert, es sei denn, ENCODING_MIME festgelegt ist. 
    
MAC_ATTACH_ENCODING_UUENCODE 
  
> Codieren Sie Macintosh-Anlagen in UUENCODE. Wenn das ENCODING_MIME festgelegt ist, wird dieses Flag ignoriert, und stattdessen wird die BinHex-Codierung verwendet. 
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internetstandard-E-Mail-Konventionen in Nachrichtenobjekte.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

