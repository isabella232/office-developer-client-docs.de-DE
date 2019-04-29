---
title: Kanonische Pidlidremotetransport (-Eigenschaft
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
# <a name="pidlidremotetransport-canonical-property"></a>Kanonische Pidlidremotetransport (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, mit welchem Konto das Kopfzeilenelement verknüpft ist, und zwar in erster Linie für die Implementierung der Funktion "POP-Leave auf dem Server". 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften  <br/> |dispidRemoteXP  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Remote  <br/> |
|Long-ID (Deckel):  <br/> |0x00008F03  <br/> |
|Datentyp:  <br/> |PT_STRING8  <br/> |
|Bereich:  <br/> |Remote Nachricht  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist nur für Nachrichten relevant, die über eine Nachrichtenklasse von IPM verfügen. Remote. In Microsoft Outlook werden verschiedene Konten, die in einen bestimmten Informationsspeicher heruntergeladen werden, in einer FAI-Nachricht (Folder Associated Information) aufbewahrt, aber diese Informationen können auch in der Registrierung aufbewahrt werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]] 
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

