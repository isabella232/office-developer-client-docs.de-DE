---
title: PidTagOriginCheck (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginCheck
api_type:
- COM
ms.assetid: 27e0ab2f-b373-41ae-b922-2f45f9671ac6
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bbf09cb841c633b6f13ae12ec20e120ea3fd7ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794745"
---
# <a name="pidtagorigincheck-canonical-property"></a>PidTagOriginCheck (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält einen binären Überprüfung-Wert, mit der einen Delivery Report Empfänger Ursprung der ursprünglichen Nachricht überprüfen kann.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_ORIGIN_CHECK  <br/> |
|Bezeichner:  <br/> |0 x 0027  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft bietet eine Möglichkeit für ein Drittanbieter, wie ein Message Transfer Agent (MTA) oder ein messaging-Benutzer empfangen eines Unzustellbarkeitsberichts die gesendete Nachricht Origin überprüfen. Auf einer empfangenen Nachricht vorhanden sind, sollten diese Eigenschaft auf eine beliebige Übermittlungsbericht generiert, die als Antwort auf die Nachricht kopiert werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

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

