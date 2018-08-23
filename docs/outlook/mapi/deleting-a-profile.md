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
ms.openlocfilehash: d13af3a2d0293641fd87d1065bceedfa4b62a3b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573243"
---
# <a name="deleting-a-profile"></a>Löschen eines Profils

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
 **Zum Löschen eines Profils**
  
- Rufen Sie [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).
    
 **DeleteProfile** markiert das Profil zum Löschen, wenn es derzeit warten verwendet wird, bis es nicht mehr entfernen aktiv ist. Das Profil wird nicht tatsächlich ausgeblendet, bis jeder Client mit einer aktiven Sitzung unterbrochen hat. 
  
 **DeleteProfile** Ruft die Eintrags-Funktion von jeder Nachrichtendienst im Profil mit dem _UlContext_ -Parameter auf MSG_SERVICE_DELETE festgelegt. Die Aufrufe an den Eintrag Punktfunktionen tritt auf, bevor die Dienste physisch aus dem Profil entfernt werden. 
  

