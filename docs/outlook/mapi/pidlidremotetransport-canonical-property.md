---
title: PidLidRemoteTransport (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRemoteTransport
api_type:
- COM
ms.assetid: b3b30d6a-05cd-4dd1-a162-20768f12e680
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ddedc2ca0785be2fe4850ec3cfdf979d1e5f2798
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439443"
---
# <a name="pidlidremotetransport-canonical-property"></a>PidLidRemoteTransport (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, welchem Konto das Kopfzeilenelement zugeordnet ist, in erster Linie, um die POP Leave on Server-Funktionalität zu implementieren. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften  <br/> |dispidRemoteXP  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Remote  <br/> |
|Lange ID (LID):  <br/> |0x00008F03  <br/> |
|Datentyp:  <br/> |PT_STRING8  <br/> |
|Bereich:  <br/> |Remotenachricht  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist nur für Nachrichten relevant, die eine Nachrichtenklasse von IPM haben. Remote. Microsoft Outlook speichert eine Zuordnung verschiedener Konten, die in einer Folder Associated Information (FAI)-Nachricht in einen bestimmten Speicher heruntergeladen werden, kann diese Informationen jedoch auch in der Registrierung speichern.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]] 
  
> Stellt Eigenschaftensatzdefinitionen und Verweise auf verwandte Exchange Server zur Verfügung.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

