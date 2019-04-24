---
title: Kanonische Pidtagattachtransportname (-Eigenschaft
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
ms.openlocfilehash: bd3a22bf55d03f3a9f06bf5c19650407bcc5627d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361068"
---
# <a name="pidtagattachtransportname-canonical-property"></a>Kanonische Pidtagattachtransportname (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Namen einer Anlagendatei, die so geändert wurde, dass Sie TNEF-Nachrichten zugeordnet werden kann. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W  <br/> |
|Kennung:  <br/> |0x370C  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>Bemerkungen

TNEF und der Transportanbieter verwenden diese Eigenschaften. Sie sind in der Regel nicht für Clientanwendungen verfügbar. 
  
Diese Eigenschaften werden in der Regel von TNEF verwendet, wenn das zugrunde liegende Messagingsystem die angegebenen Dateinamen nicht unterstützt. Sie werden beispielsweise verwendet, wenn der Benutzer mehrere Dateien mit demselben Namen anfügt, beispielsweise fünf Dateien mit dem Namen CONFIG. SYS. Der Transportanbieter muss die Namen ändern, um sicherzustellen, dass er eindeutig ist. Jeder geänderte Name wird in den **PR_ATTACH_TRANSPORT_NAME** -und zugehörigen Eigenschaften der Anlage angezeigt. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Verarbeitet Nachrichten-und Anlagenobjekte.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

