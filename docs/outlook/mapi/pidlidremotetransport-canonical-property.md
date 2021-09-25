---
title: Kanonische PidLidRemoteTransport-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidRemoteTransport
api_type:
- COM
ms.assetid: b3b30d6a-05cd-4dd1-a162-20768f12e680
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 22b497aea3510e7bd2f54b2fd32bbf7dd6f6a16c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591745"
---
# <a name="pidlidremotetransport-canonical-property"></a>Kanonische PidLidRemoteTransport-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, mit welchem Konto das Kopfzeilenelement verknüpft ist, in erster Linie, um die POP Leave on Server-Funktionalität zu implementieren. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften  <br/> |dispidRemoteXP  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Remote  <br/> |
|Long ID (LID):  <br/> |0x00008F03  <br/> |
|Datentyp:  <br/> |PT_STRING8  <br/> |
|Bereich:  <br/> |Remotenachricht  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft ist nur für Nachrichten relevant, die eine Nachrichtenklasse von IPM haben. Remote. Microsoft Outlook behält eine Zuordnung verschiedener Konten bei, die in einer FaI-Nachricht (Folder Associated Information) zu einem bestimmten Speicher heruntergeladen werden, kann diese Informationen aber auch in der Registrierung speichern.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]] 
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

