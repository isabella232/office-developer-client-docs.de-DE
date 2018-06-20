---
title: Kanonische PidTagAttachTransportName-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTransportName
api_type:
- HeaderDef
ms.assetid: 701fca52-0f96-4019-80cd-c0ccd059ff9b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6828a6436946de27020fa1177223955e07a08faf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794130"
---
# <a name="pidtagattachtransportname-canonical-property"></a>Kanonische PidTagAttachTransportName-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält den Namen einer Anlage-Datei geändert, sodass es TNEF-Nachrichten zugeordnet werden kann. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W  <br/> |
|Bezeichner:  <br/> |0x370C  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |E-Mail-Anlage  <br/> |
   
## <a name="remarks"></a>Hinweise

TNEF und der Adressbuchhierarchie verwenden diese Eigenschaften. Sie sind in der Regel nicht Clientanwendungen zur Verfügung. 
  
Diese Eigenschaften werden häufig von TNEF verwendet, wenn das zugrunde liegende messaging-System die angegebenen Dateinamen nicht unterstützt. Beispielsweise werden sie verwendet, wenn der Benutzer mehrere Dateien mit dem gleichen Namen, beispielsweise fünf Dateien mit dem Namen CONFIG angehängt wird. SYS. Der Transportdienst müssen Sie sicherstellen, dass sie eindeutig sind die Namen ändern. Jede geänderte Name wird in der Anlage **PR_ATTACH_TRANSPORT_NAME** und zugeordneten Eigenschaften. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
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

