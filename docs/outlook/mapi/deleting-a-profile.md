---
title: Löschen eines Profils
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1cd87b92a9d289f06e466f4e44ce757c93074336
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410203"
---
# <a name="deleting-a-profile"></a>Löschen eines Profils

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So löschen Sie ein Profil**
  
- Rufen Sie [IProfAdmin auf::D eleteprofile](iprofadmin-deleteprofile.md).
    
 **DeleteProfile** kennzeichnet das Profil zum Löschen, wenn es derzeit verwendet wird, und wartet, bis es nicht mehr aktiv ist, um es zu entfernen. Das Profil wird nicht tatsächlich ausgeblendet, bis jeder Client mit einer aktiven Sitzung die Verbindung getrennt hat. 
  
 **DeleteProfile** Ruft die Einstiegspunktfunktion jedes Nachrichtendiensts im Profil auf, wobei der Parameter _ulContext_ auf MSG_SERVICE_DELETE festgelegt ist. Die Aufrufe der Einstiegspunktfunktionen treten auf, bevor die Dienste physisch aus dem Profil entfernt werden. 
  

