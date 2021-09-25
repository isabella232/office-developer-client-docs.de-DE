---
title: PidTagAttachTransportName (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachTransportName
api_type:
- HeaderDef
ms.assetid: 701fca52-0f96-4019-80cd-c0ccd059ff9b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: caf42a8d83442e40ee03b0ecbff9a4759b802793
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600442"
---
# <a name="pidtagattachtransportname-canonical-property"></a>PidTagAttachTransportName (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Namen einer Anlagendatei, die geändert wurde, damit sie TNEF-Nachrichten zugeordnet werden kann. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W  <br/> |
|Kennung:  <br/> |0x370C  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |Nachrichtenanlage  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

TNEF und der Transportanbieter verwenden diese Eigenschaften. Sie sind in der Regel nicht für Clientanwendungen verfügbar. 
  
Diese Eigenschaften werden häufig von TNEF verwendet, wenn das zugrunde liegende Messagingsystem die angegebenen Dateinamen nicht unterstützt. Sie werden beispielsweise verwendet, wenn der Benutzer mehrere Dateien mit demselben Namen anfügt, z. B. fünf Dateien mit dem Namen CONFIG.SYS. Der Transportanbieter muss die Namen ändern, um sicherzustellen, dass sie eindeutig sind. Jeder geänderte Name wird in **den PR_ATTACH_TRANSPORT_NAME** und den zugehörigen Eigenschaften der Anlage angezeigt. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

