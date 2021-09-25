---
title: PidTagResolveMethod (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagResolveMethod
api_type:
- COM
ms.assetid: 30d23c19-e0da-4511-9361-761153259216
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 618a973d117af50960c204e4d33684aa29a6dd59
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587146"
---
# <a name="pidtagresolvemethod-canonical-property"></a>PidTagResolveMethod (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Konfliktlösungswert eines Ordners.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RESOLVE_METHOD  <br/> |
|Kennung:  <br/> |0x3FE7  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft des Ordners, der die Konfliktlösungsnachricht enthält, gibt an, wie der Konflikt gelöst werden soll. Diese Eigenschaft ist nicht erforderlich. Wenn sie jedoch festgelegt ist, dürfen andere Flags als die folgenden nicht vorhanden sein:
  
|||
|:-----|:-----|
|RESOLVE_METHOD_DEFAULT (0x00000000)  <br/> |Konfliktlösungsnachricht sollte generiert werden.  <br/> |
|RESOLVE_METHOD_LAST_WRITER_WINS (0x00000001)  <br/> |Überschreiben Sie die Zielnachricht, wobei die aktuellen Änderungen angewendet werden.  <br/> |
|RESOLVE_NO_CONFLICT_NOTIFICATION (0x00000002)  <br/> |Senden Sie keine Konfliktbenachrichtigung, wenn Sie eine Konfliktlösungsnachricht in einem öffentlichen Ordner generieren.  <br/> |
   
Ein Client oder Server darf keine Konfliktlösungsnachricht für zugeordnete Nachrichten generieren. Diese Nachrichten müssen **mithilfe** RESOLVE_METHOD_LAST_WRITER_WINS Semantik aufgelöst werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCSYNC]](https://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)
  
> Behandelt die Synchronisierung von Nachrichtenobjektdaten zwischen einem Server und einem Client.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Definiert die grundlegenden Datenstrukturen, die in Remotevorgängen verwendet werden.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

