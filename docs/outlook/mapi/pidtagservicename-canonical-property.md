---
title: Kanonische PidTagServiceName-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagServiceName
api_type:
- COM
ms.assetid: 9a63d647-7504-42fc-b317-6b02b89070eb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 390a298753c0e98635c55da11a4ae28588735b4e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591416"
---
# <a name="pidtagservicename-canonical-property"></a>Kanonische PidTagServiceName-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Namen eines Nachrichtendiensts, der vom Benutzer in der Datei MapiSvc.inf festgelegt wurde.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_SERVICE_NAME, PR_SERVICE_NAME_A, PR_SERVICE_NAME_W  <br/> |
|Kennung:  <br/> |0x3D09  <br/> |
|Datentyp:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Bereich:  <br/> |MAPI-Profil  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der in diesen Eigenschaften enthaltene Name ist für den Nachrichtendienst spezifisch. Er stammt aus dem Abschnitt [Dienste] in MapiSvc.inf.
  
Diese Eigenschaften werden als Spalte in der Nachrichtendiensttabelle angezeigt und können zum Filtern von Diensten verwendet werden. Da er zum Identifizieren und Filtern von Diensten verwendet wird, sollte der Wert nicht lokalisiert werden.
  
## <a name="related-resources"></a>Verwandte Ressourcen

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

