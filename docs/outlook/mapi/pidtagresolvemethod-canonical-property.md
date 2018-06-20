---
title: Kanonische PidTagResolveMethod-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResolveMethod
api_type:
- COM
ms.assetid: 30d23c19-e0da-4511-9361-761153259216
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7f55b85e21f007be7c1b9d42d42473e3a8d2becb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794984"
---
# <a name="pidtagresolvemethod-canonical-property"></a>Kanonische PidTagResolveMethod-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält einen Ordner Konflikt Lösung Wert.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_RESOLVE_METHOD  <br/> |
|Bezeichner:  <br/> |0x3FE7  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-status  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft auf den Ordner mit den Konflikt Lösung Nachricht wird anzugeben, wie den Konflikt zu lösen. Diese Eigenschaft ist nicht erforderlich. Jedoch ist festgelegt, müssen als den folgenden Kennzeichen nicht vorhanden sein:
  
|||
|:-----|:-----|
|RESOLVE_METHOD_DEFAULT (0 X 00000000)  <br/> |Konflikt zu lösen, dass die Nachricht generiert werden soll.  <br/> |
|RESOLVE_METHOD_LAST_WRITER_WINS (0 X 00000001)  <br/> |Überschreiben Sie Zielnachricht mit aktuellen Änderungen angewendet wird.  <br/> |
|RESOLVE_NO_CONFLICT_NOTIFICATION (0 X 00000002)  <br/> |Senden Sie Conflict-Benachrichtigung nicht beim Generieren von Konflikt beheben Nachricht im öffentlichen Ordner.  <br/> |
   
Ein Client oder Server muss eine Nachricht an Konflikt auflösen zugeordneten Nachrichten nicht generiert werden. Diese Nachrichten müssen mit **RESOLVE_METHOD_LAST_WRITER_WINS** Semantik aufgelöst werden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCSYNC]](http://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)
  
> Synchronisieren von messaging Objektdaten zwischen einem Server und einem Client behandelt.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Definiert die grundlegende Datenstrukturen, die verwendet werden remote-Vorgängen.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

