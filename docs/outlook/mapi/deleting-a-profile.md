---
title: Löschen eines Profils
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fc951d5b4a031aed335181ac8534ac4eb9c6c8ba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588182"
---
# <a name="deleting-a-profile"></a>Löschen eines Profils

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So löschen Sie ein Profil**
  
- Rufen [Sie IProfAdmin::D eleteProfile](iprofadmin-deleteprofile.md)auf.
    
 **DeleteProfile** markiert das Profil zum Löschen, wenn es gerade verwendet wird, und wartet, bis es nicht mehr aktiv ist, um es zu entfernen. Das Profil wird erst dann ausgeblendet, wenn jeder Client mit einer aktiven Sitzung getrennt wurde. 
  
 **DeleteProfile** ruft die Einstiegspunktfunktion jedes Nachrichtendiensts im Profil auf, wobei der  _ulContext-Parameter_ auf MSG_SERVICE_DELETE festgelegt ist. Die Aufrufe der Einstiegspunktfunktionen erfolgen, bevor die Dienste physisch aus dem Profil entfernt werden. 
  

